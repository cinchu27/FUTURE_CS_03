# 🛡️ Task 03 – API Security Risk Analysis

This repository contains the work completed for **Task 03: API Security Risk Analysis** as part of the **Cyber Security Internship Program at Future Interns**.

The objective of this task is to perform a **basic, ethical, and read-only API security risk analysis** on a public demo API in order to understand common API security weaknesses such as missing authentication, excessive data exposure, and lack of access control.


---

## API Tested
- **Name:** JSONPlaceholder  
- **Base URL:** `https://jsonplaceholder.typicode.com`  
- **Endpoints Tested:**
  - `GET /users`
  - `GET /users/{id}`
  - `POST /posts`

**Reason for Selection:**  
JSONPlaceholder is a safe, public API designed for testing and educational purposes. Its open access allows demonstration of API security risks such as missing authentication, excessive data exposure, input validation gaps, and potential authorization issues, without risk to real users or systems.

---

## Tools Used
- [Postman](https://www.postman.com) – API request testing and inspection  
- Browser DevTools – Request and response header analysis  
- Google Docs / MS Word – Report creation  

---

## Scope
- Read-only and safe testing only  
- Public/demo API endpoints  
- No exploitation, bypassing, or denial-of-service testing  

---

## Methodology
1. Reviewed API documentation  
2. Tested endpoints using Postman  
3. Inspected authentication, headers, and responses  
4. Evaluated input validation and payload handling  
5. Identified risks and classified severity (High / Medium / Low)  
6. Recommended remediation steps in line with OWASP API Security Top 10  

---

## Key Findings
| # | Risk | Severity | Description |
|---|------|----------|-------------|
| 1 | No Authentication | High | API endpoints accessible without authentication |
| 2 | ID Enumeration (BOLA risk) | High | User IDs can be enumerated without authorization |
| 3 | Input Validation Failure | Medium | Invalid data types accepted in POST requests |
| 4 | No Payload Size Limit | Medium | Excessively large payloads accepted without restriction |
| 5 | Excessive Data Exposure | Medium | Full user objects returned, including email, phone, address |

---

## Report & Screenshots
- Report: `/report/API Security Risk Analysis Report.pdf`  
- Evidence: `/Evidence/`  
  - GET users request  
  - ID enumeration demonstration  
  - POST normal payload  
  - POST malformed payload  
  - POST large payload  
  - Header inspection  

---

## Disclaimer
This assessment was conducted strictly on a public demo API for educational purposes. No exploitation, unauthorized access, or denial-of-service testing was performed. Findings are intended to demonstrate API security risks in a controlled environment only.

---

## Outcome
This project demonstrates key API security concepts including authentication, authorization, input validation, and data exposure. It provides practical remediation recommendations aligned with industry best practices and the OWASP API Security Top 10.  
