# CodeAlpha_Secure_Coding_Review

## Overview

This repository contains a review of the secure coding practices implemented in an open-source application chosen for an intern task at CodeAlpha. The task involved selecting an open-source application and conducting a manual security review process. The primary objective of this review is to identify security vulnerabilities within the codebase and offer recommendations for enhancing secure coding practices.

## Task Requirements

- Choose an open-source application to review.
- Conduct a thorough review of the codebase to identify security vulnerabilities.
- Provide detailed recommendations for implementing secure coding practices.
- Utilize manual code reviews to assess the codebase.

## Application Description

The application chosen for this task is a web-based recipe management system called "ReciPHP." It allows users to add, search, and view recipes, as well as post comments on recipes. The application is written in PHP and interacts with a MySQL database for data storage.

## Security Review

The codebase was reviewed for potential security vulnerabilities using manual code review techniques. Identified vulnerabilities were categorized and documented along with recommendations for implementing secure coding practices. The review aimed to ensure that the application adheres to industry best practices for security and mitigates common security threats effectively.

## Recommendations

- **Implement Parameterized Queries:** Use parameterized queries or prepared statements with PDO to prevent SQL injection attacks. This approach helps separate SQL logic from user input, reducing the risk of injection vulnerabilities.
    
- **Sanitize User Input:** Sanitize user input before displaying it on web pages to prevent cross-site scripting (XSS) attacks. Utilize functions like `htmlspecialchars()` to encode special characters and prevent script injection.
    
- **Avoid Hard-Coded Credentials:** Remove hard-coded credentials and sensitive information from the source code. Instead, use environment variables or secure configuration files to store credentials securely.
    
- **Update Deprecated Functions:** Replace deprecated functions like `mysql_connect()` with more secure alternatives such as PDO for database connectivity. Deprecated functions may have security vulnerabilities and lack support in newer PHP versions.
    
- **Prevent File Inclusion Vulnerabilities:** Avoid using user-controlled input in file inclusion functions to prevent remote file inclusion (RFI) and local file inclusion (LFI) attacks. Implement whitelisting or input validation to restrict file paths and prevent unauthorized access to sensitive files.
    
- **Regular Security Updates:** Stay informed about security updates and patches for PHP, MySQL, and other dependencies used in the application. Regularly update the application and its components to mitigate security risks associated with known vulnerabilities.
    

## Conclusion

The security review of the "ReciPHP" application has identified several security vulnerabilities and provided recommendations for enhancing the security posture of the codebase. By implementing the recommended secure coding practices, the application can better withstand potential security threats and protect user data.

## Resources

- [ReciPHP Source-Code](https://sourceforge.net/projects/reciphp/)
- [TryHackMe SAST Room](https://tryhackme.com/room/sast)
- [Pentesterlab Code Review](https://pentesterlab.com/exercises/codereview/course) 
- [secure-code-review-checklist](https://github.com/softwaresecured/secure-code-review-checklist)
- [PHP-vulnerability-audit-cheatsheet](https://github.com/dustyfresh/PHP-vulnerability-audit-cheatsheet)
- [php-pdo-prepared-statements-to-prevent-sql-injection](https://websitebeaver.com/php-pdo-prepared-statements-to-prevent-sql-injection)
- [OWASP TOP TEN](https://owasp.org/www-project-top-ten/)
- [OWASP Security Code Review 101](https://owasp.org/SecureCodingDojo/codereview101/)
- [OWASP SQL Injection Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/SQL_Injection_Prevention_Cheat_Sheet.html)
- [OWASP XSS (Cross Site Scripting) Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/DOM_based_XSS_Prevention_Cheat_Sheet.html)
- [OWASP PHP Configuration Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/PHP_Configuration_Cheat_Sheet.html)

