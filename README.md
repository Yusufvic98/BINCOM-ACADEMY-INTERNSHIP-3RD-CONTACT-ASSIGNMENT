# BINCOM-ACADEMY-INTERNSHIP-3RD-CONTACT-ASSIGNMENT
BINCOM Academy Internship Assessment 3 — DVWA SQLi/XSS, ModSecurity + OWASP CRS, AWS/PrestaShop 9.1.5 security hardening, WAF attack simulation, logging, backup/recovery and security assessment.
Period: SEPTEMBER 2026
3rd Contact Assignment — Assessment 3: Attack and Defend Web Application

Attack and Defend Web Application

This repository contains the complete technical documentation and evidence for my BINCOM Academy Internship Assessment 3.

Scope

DVWA SQL Injection and XSS testing
One of the strongest parts of the project is the complete defensive chain:

Kali attack → HTTP request → ModSecurity inspection → OWASP CRS 942100 detection → anomaly score/blocking → HTTP 403 → ModSecurity audit log

You also demonstrated a separate custom defensive control:

Kali → randomized PrestaShop admin path → custom rule 1001001 → HTTP 403 → audit evidence

That makes the project more than simply "I installed a WAF." It demonstrates attack execution, defensive configuration, validation, logging and evidence correlation.

The original deployment work also established layered controls including AWS Security Groups, host-based UFW, separate database infrastructure and MariaDB isolation.

ModSecurity + OWASP CRS configuration and blocking

AWS-hosted PrestaShop 9.1.5 security assessment and hardening

PrestaShop security checklist and remediation

Controlled PrestaShop SQL Injection simulation

WAF audit-log correlation

Database backup and recovery validation

AWS/Apache/PHP/cache/resource troubleshooting

Key Results

Custom ModSecurity rule 1001001 protected /admin113pn8yfvwfb8jihird.

Direct access to the protected admin path returned HTTP 403 Forbidden.

OWASP CRS rule 942100 detected a controlled SQL Injection probe and blocked it with HTTP 403.

A pre-remediation SQL dump was restored to a temporary database containing 301 tables, with key row counts verified.

Demo/sample content was remediated.

Limitations

HTTPS/TLS was not completed because no domain/certificate was available for this iteration. MFA was not evidenced in the reviewed Back Office. Payment-provider/API assurance was limited to the available configuration and unauthenticated route testing.

All testing was restricted to the authorized internship/lab environment and the PrestaShop simulation was non-destructive.
