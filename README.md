# Performance Testing Scripts – Login & Register Interfaces - SVV_Project

## 1. Project Overview

This repository contains **Apache JMeter performance testing scripts** developed for a **school group assignment**.  
The scripts are used to evaluate the **performance, concurrency handling, and stability** of the **Login** and **Register** functionalities implemented by our project team.

Three separate JMeter test plans are provided to cover different testing scenarios:

- Login interface performance testing  
- Register interface performance testing  
- Combined Register + Login transaction performance testing  

These scripts support the performance analysis and reporting required by the course assignment.

---

## 2. Test Scripts Description

### 2.1 Login Interface Performance Test

**Script file:** `login_interface.jmx`

This script focuses on testing the **Login API** independently.

**Test objectives:**
- Measure response time under different concurrency levels  
- Observe throughput (TPS) behavior as concurrent users increase  
- Verify system stability and error rate during sustained login requests  

**Typical scenarios:**
- Baseline performance test  
- Concurrent user test  
- Load and stress testing for the login interface  

---

### 2.2 Register Interface Performance Test

**Script file:** `register_interface.jmx`

This script evaluates the **Register API**, which involves input validation and database write operations.

**Test objectives:**
- Measure registration response time  
- Identify performance bottlenecks during user registration  
- Observe system behavior under repeated registration requests  

**Notes:**
- Database cleanup may be required between test runs to avoid duplicate user conflicts.

---

### 2.3 Register + Login Transaction Performance Test

**Script file:** `register_login_interface.jmx`

This script simulates a **complete user workflow**, where a user registers and then immediately logs in.

**Test objectives:**
- Evaluate end-to-end transaction performance  
- Measure combined response time for registration and login  
- Analyze throughput and stability under realistic user behavior  

**Scenario characteristics:**
- Sequential execution of Register → Login  
- Higher resource usage compared to single-interface tests  
- Suitable for simulating real-world user behavior  

---

## 3. Test Environment

The performance tests were conducted in a **controlled testing environment** for academic purposes.

General assumptions include:
- Apache JMeter 5.x  
- Backend service deployed on a test server  
- Database populated with test data  
- Test users generated dynamically or loaded using CSV Data Set Config  

*(Detailed environment configuration is documented in the performance test report.)*

---

## 4. How to Run the Tests

1. Install **Apache JMeter** (version 5.x recommended).
2. Launch JMeter and open the required `.jmx` file.
3. Configure the following parameters:
   - Server IP / Domain
   - Port number
   - Thread Group settings (users, ramp-up time, duration)
4. (Optional) Update CSV files for test user data if applicable.
5. Start the test and monitor results using:
   - Summary Report
   - Aggregate Report
   - Response Time Graph
   - Backend Listener / PerfMon (if enabled)

---

## 5. Test Results and Analysis

Detailed **test results, charts, and analysis** are provided in the **performance testing report** submitted as part of the coursework.

Key metrics analyzed include:
- Average / 90% / 95% response time  
- Throughput (TPS)  
- Error rate  
- System stability under sustained load  

---

## 6. Notes

- These scripts are intended for **academic and testing purposes only**.
- Test parameters may need adjustment depending on the deployment environment.
- Performance results may vary based on system configuration and server load.

---

## 7. Authors

Developed by **School Project Group**  
Performance testing conducted as part of a **software testing and quality assurance assignment**.
