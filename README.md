
# Spring Security Project 01 - Default Authentication

A beginner-friendly Spring Boot project exploring the fundamentals of Spring Security, default authentication, and securing REST APIs.

## 📌 About the Project

This is my first Spring Security project, created to understand how Spring Security protects application endpoints by default.

In this project, I explored the default authentication mechanism provided by Spring Security and configured custom login credentials instead of relying on the default generated password.

The project also contains basic banking-related REST APIs for checking balance, updating balance, and accessing contact information.

## 🛠️ Technologies Used

- Java
- Spring Boot
- Spring Security
- Spring Web
- Maven
- IntelliJ IDEA

## 🔐 Security Features

- All endpoints require authentication by default unless explicitly permitted.
- Explored Spring Security's default authentication mechanism.
- Configured custom username and password.
- Tested secured REST APIs using authentication.
- Learned the basics of protecting REST endpoints.

## 🌐 API Endpoints

| HTTP Method | Endpoint | Description |
|-------------|----------|-------------|
| GET | `/balance` | Returns the current balance |
| POST | `/add` | Calculates the balance plus the submitted amount |
| GET | `/contactUs` | Returns contact information |

### 1. Get Balance

- **Endpoint:** `/balance`
- **Method:** GET
- **Access:** Authentication Required
- **Description:** Returns the current balance, initialized to `1000`.

### 2. Add Amount

- **Endpoint:** `/add`
- **Method:** POST
- **Access:** Authentication Required
- **Parameters:**
  - `AccNo` - Account number
  - `num` - Amount to add

Example request:

```text
POST http://localhost:8080/add?AccNo=12345&num=500
```

The current implementation returns the initial balance plus the submitted amount. It does not persistently update the balance.

### 3. Contact Us

- **Endpoint:** `/contactUs`
- **Method:** GET
- **Access:** Authentication Required
- **Description:** Returns contact information.

## ⚙️ How to Run the Project

### Step 1: Clone the Repository

```bash
git clone <YOUR_REPOSITORY_URL>
```

### Step 2: Open the Project

Open the cloned project in IntelliJ IDEA.

### Step 3: Configure Credentials

Set your custom Spring Security username and password in the application's configuration, such as `application.properties`, if that is how your project is configured.

Example:

```properties
spring.security.user.name=your_username
spring.security.user.password=your_password
```

Replace the example values with your own credentials. Do not commit real passwords or secrets to a public repository.

### Step 4: Run the Application

Run the main Spring Boot application class.

### Step 5: Test the APIs

The application runs on port `8080` by default.

- `http://localhost:8080/balance`
- `http://localhost:8080/contactUs`

Use Postman or another HTTP client to test the POST `/add` endpoint.

Authenticate using the credentials configured for your application.

## 🎯 Key Learning Outcomes

- Understanding Spring Security fundamentals.
- Learning why endpoints are secured by default.
- Understanding default authentication.
- Configuring custom username and password.
- Testing secured REST APIs.
- Working with `@GetMapping`, `@PostMapping`, and `@RequestParam`.

## 👨‍💻 Author

**Motilal Gupta**

This project marks my first step toward learning Spring Security and implementing authentication in Spring Boot applications.

---

⭐ If you find this project useful, consider giving the repository a star!
