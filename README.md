# EcoBazaarX

EcoBazaarX is a sustainability‑focused ecommerce platform built with a React frontend and a Spring Boot backend. It blends standard shopping flows with a carbon‑impact lens so users can make greener choices while they shop.

**Highlights**

- Auth flow with OTP‑based password recovery
- Product catalog, detail pages, and search
- Cart, wishlist, and order management
- Address management at checkout
- Carbon footprint summary for cart/checkout
- Admin and insights screens (UI present; backend APIs may be evolving)

**Tech Stack**

- Frontend: React, React Router, Axios, CRA (`react-scripts`)
- Backend: Spring Boot, Spring Security, Spring Data JPA, JWT, Java Mail
- Database: MySQL

**Project Structure**

- `Frontend/` React app
- `Backend/SignupForm/SignupForm/` Spring Boot app
- `scripts/` helper scripts

**Quick Start**

Frontend

1. `cd Frontend`
2. `npm install`
3. `npm start`

Backend (Windows)

1. `cd Backend/SignupForm/SignupForm`
2. `mvnw.cmd spring-boot:run`

Backend (macOS/Linux)

1. `cd Backend/SignupForm/SignupForm`
2. `./mvnw spring-boot:run`

**Configuration**

The backend reads config from `application.properties`. For safety, keep real credentials in local environment variables or a local override file. A sanitized template is provided at `Backend/SignupForm/SignupForm/src/main/resources/application.properties.example`.

Example `application.properties` (sanitize for GitHub):

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/LoginDetails
spring.datasource.username=YOUR_DB_USER
spring.datasource.password=YOUR_DB_PASSWORD

spring.mail.host=smtp.gmail.com
spring.mail.port=587
spring.mail.username=YOUR_EMAIL
spring.mail.password=YOUR_APP_PASSWORD
```

**Ports**

- Frontend: `http://localhost:3000`
- Backend: `http://localhost:8080`

**Scripts**

Frontend

- `npm start` Run dev server
- `npm run build` Production build
- `npm test` Run tests

Backend

- `mvnw.cmd spring-boot:run` Run dev server (Windows)
- `./mvnw spring-boot:run` Run dev server (macOS/Linux)
- `mvnw.cmd test` Run tests

**Notes**

- If you hit Java version mismatches, align `java.version` and compiler `source/target` in `Backend/SignupForm/SignupForm/pom.xml`.
- For API base URL, add a `.env` in `Frontend/` and set `REACT_APP_API_BASE_URL`.
