---
description: Java Spring Boot Best Practices for Copilot
globs: 
---

# Java Spring Boot Best Practices (for Copilot)

Copilot must always adhere to SOLID, DRY, KISS, and YAGNI principles, and follow OWASP best practices. Tasks should be broken down into the smallest units and solved step by step.

## Technology Stack

- Java Spring Boot 3
- Maven with Java 17
- Spring Web, Spring Data JPA, Thymeleaf, Lombok, PostgreSQL driver

## Application Logic Design

1. All request and response handling must be done only in RestController.
2. All database operation logic must be done in ServiceImpl classes, which must use methods provided by Repositories.
3. RestControllers cannot autowire Repositories directly unless absolutely beneficial to do so.
4. ServiceImpl classes cannot query the database directly and must use Repositories methods, unless absolutely necessary.
5. Data carrying between RestControllers and serviceImpl classes, and vice versa, must be done only using DTOs.
6. Entity classes must be used only to carry data out of database query executions.

## Entities

1. Annotate entity classes with @Entity.
2. Annotate entity classes with @Data (from Lombok), unless specified otherwise.
3. Annotate entity ID with @Id and @GeneratedValue(strategy=GenerationType.IDENTITY).
4. Use FetchType.LAZY for relationships, unless specified otherwise.
5. Annotate entity properties properly according to best practices, e.g., @Size, @NotEmpty, @Email, etc.

## Repository (DAO)

1. Annotate repository classes with @Repository.
2. Repository classes must be of type interface.
3. Extend JpaRepository with the entity and entity ID as parameters, unless specified otherwise.
4. Use JPQL for all @Query type methods, unless specified otherwise.
5. Use @EntityGraph(attributePaths={"relatedEntity"}) in relationship queries to avoid the N+1 problem.
6. Use a DTO as the data container for multi-join queries with @Query.

## Service

1. Service classes must be of type interface.
2. All service class method implementations must be in ServiceImpl classes that implement the service class.
3. All ServiceImpl classes must be annotated with @Service.
4. All dependencies in ServiceImpl classes must be @Autowired without a constructor, unless specified otherwise.
5. Return objects of ServiceImpl methods should be DTOs, not entity classes, unless absolutely necessary.
6. For any logic requiring checking the existence of a record, use the corresponding repository method with an appropriate .orElseThrow lambda method.
7. For any multiple sequential database executions, use @Transactional or transactionTemplate, whichever is appropriate.

## Data Transfer Object (DTO)

1. Must be of type record, unless specified otherwise.
2. Specify a compact canonical constructor to validate input parameter data (not null, blank, etc., as appropriate).

## RestController

1. Annotate controller classes with @RestController.
2. Specify class-level API routes with @RequestMapping, e.g. ("/api/user").
3. Class methods must use best practice HTTP method annotations, e.g, create = @PostMapping("/create"), etc.
4. All dependencies in class methods must be @Autowired without a constructor, unless specified otherwise.
5. Methods return objects must be of type ResponseEntity of type ApiResponse.
6. All class method logic must be implemented in try..catch block(s).
7. Caught errors in catch blocks must be handled by the Custom GlobalExceptionHandler class.

## ApiResponse Class

```java
@Data
@NoArgsConstructor
@AllArgsConstructor
public class ApiResponse<T> {
  private String result;    // SUCCESS or ERROR
  private String message;   // success or error message
  private T data;           // return object from service class, if successful
}
```

## GlobalExceptionHandler Class

```java
@RestControllerAdvice
public class GlobalExceptionHandler {

    public static ResponseEntity<ApiResponse<?>> errorResponseEntity(String message, HttpStatus status) {
      ApiResponse<?> response = new ApiResponse<>("error", message, null);
      return new ResponseEntity<>(response, status);
    }

    @ExceptionHandler(IllegalArgumentException.class)
    public ResponseEntity<ApiResponse<?>> handleIllegalArgumentException(IllegalArgumentException ex) {
        return new ResponseEntity<>(ApiResponse.error(400, ex.getMessage()), HttpStatus.BAD_REQUEST);
    }
}
```

