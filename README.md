# Application Security Testing

This repository demonstrates an application security test performed on a login page. The test was conducted on a demo web application (`https://daadesina.pythonanywhere.com`) to identify vulnerabilities and recommend fixes.


## Summary

The security assessment revealed:
- **Weak authentication mechanisms**
- **Rate-limiting issues**
- **Cross-Site Scripting (XSS) vulnerability** in the Sign-Up form


### Key Findings
1. Multiple valid passwords per username
2. Cross-Site Scripting (XSS)
3. General lack of security best practices
   

### Recommendations
-​ Strengthen authentication security.  
-​ Mitigate XSS Vulnerabilities.  
-​ Conduct regular security audits.  

---

## Attack Modes & Tools Used

### 1. **Hydra**
Tool: `Hydra`
Command used:
```bash
hydra -L vero@gmail.com -P custom-password.txt daadesina.pythonanywhere.com \
  http-post-form /login:username=^USER^&password=^PASS^:F=Invalid Details
```

This allowed brute-force testing of the login page.

### 2. **Manual XSS Payload Injection**
Chrome DevTools `(F12 or fn+F12)` was used to manipulate the HTML tags of the Sign-Up form, bypassing required field validations.

---

## Test Environment
- **Target Website**: `https://daadesina.pythonanywhere.com`
- **Tools Used**: Hydra, Manual Payload Injection
- **Environment**: Ubuntu 20.04.1 LTS

---

## Repository Structure

- `/docs`: Project requirements, project documentation with detailed reports and findings.
- `/tools`: Example scripts and commands used during the test.
- `/examples`: Optional vulnerable app for demonstration purposes.

---

### Disclaimer
This project is for **educational purposes** only. The target application was tested with proper authorization and is not intended to showcase malicious activities.

---

