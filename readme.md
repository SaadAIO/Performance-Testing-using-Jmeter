# 🧪 JMeter Load Testing Project

This project demonstrates load testing of key API endpoints (Register, Login, Create User, Update User, and Delete User) using **Apache JMeter**. It includes real-time data extraction, logical controllers, conditional execution, and reporting for performance evaluation.

---

## 📌 Project Features

### ✅ Load Testing Scenarios
- **Register User**: Simulates multiple users registering on the platform.
- **Login User**: Authenticates the users with valid credentials.
- **Create User**: Mimics user creation scenarios with dynamic input.
- **Update User**: Tests update operations for an existing user.
- **Delete User**: Performs user deletion and validates the response.

---

### 🔁 JMeter Components Used

#### 1. **Loop Controller**
Used to simulate multiple iterations of user behavior for each API. This helps in stress-testing the endpoints under continuous load.

#### 2. **If Controller**
Added a conditional check based on **timestamp** to prevent the test from running if it exceeds a 30-minute window. Ensures time-bounded execution during long test runs.

#### 3. **User Defined Variables**
Custom variables like `baseUrl`, `email`, `password`, etc., were declared and reused across multiple samplers to improve maintainability and flexibility.

#### 4. **JSON Extractor**
Used to extract dynamic values like user `id` or `token` from responses. These extracted values are passed on to subsequent samplers, simulating real-world workflows (e.g., login → get token → update/delete).

---

### 📊 Reporting and Results

- **JTL Report**: Test results were saved in `.jtl` format for detailed analysis.
- **Dashboard Report**: A beautiful and interactive HTML dashboard was generated using JMeter's built-in reporting features.

The dashboard includes:
- Throughput
- Response Time
- Error Rate
- Latency Breakdown
- Requests per Second


