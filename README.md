# Application Security Testing

This repository showcases an application security test on a demo web application ([https://daadesina.pythonanywhere.com](https://daadesina.pythonanywhere.com)) to identify vulnerabilities and recommend fixes.

---

## **Summary**
### Key Findings
- Weak authentication mechanisms.  
- Rate-limiting issues.  
- Cross-Site Scripting (XSS) in the Sign-Up form.  

### Recommendations
- Strengthen authentication: Enforce MFA and password policies.
- Mitigate XSS: Sanitize inputs and adopt Content Security Policies.
- Perform regular security audits.

---

## **Attack Methods & Tools**
1. **Hydra**: Used for brute-force login testing.
   ```bash
   hydra -L vero@gmail.com -P custom-password.txt daadesina.pythonanywhere.com \
     http-post-form /login:username=^USER^&password=^PASS^:F=Invalid Details
   ```
2. **Manual XSS Testing**: Chrome DevTools to inject payloads and bypass validations.

---

## **Environment**
- **Target**: [https://daadesina.pythonanywhere.com](https://daadesina.pythonanywhere.com)  
- **Tools**: Hydra, Chrome DevTools  
- **System**: Ubuntu 20.04.1 LTS

---

## **Disclaimer**
_This project is for **educational purposes only** and was authorized by the target application owner._

---