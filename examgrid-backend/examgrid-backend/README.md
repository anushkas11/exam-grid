# ExamGrid - Backend (Spring Boot + MySQL)

## Requirements
- Java 21, Maven (or use `./mvnw`)
- MySQL 8+

## Setup
1. Make sure MySQL is running. The database `examgrid` is created automatically
   (or create it yourself):
   ```sql
   CREATE DATABASE examgrid CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci;
   ```
2. Set your credentials, either by editing `src/main/resources/application.properties`
   or with environment variables:
   ```
   DB_URL=jdbc:mysql://localhost:3306/examgrid
   DB_USERNAME=root
   DB_PASSWORD=your_password
   ```
3. Run:
   ```
   ./mvnw spring-boot:run
   ```
   The API starts on http://localhost:8081 and tables are created by Hibernate on first run.

## Notes
- Default programs (1001-1004) are seeded only when the `program` table is empty.
- Tests use in-memory H2 (`src/test/resources/application.properties`), no MySQL needed.
