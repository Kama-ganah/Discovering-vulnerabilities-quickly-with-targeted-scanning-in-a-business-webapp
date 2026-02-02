# Overview
I evaluated the application’s file handling endpoints to identify high-impact vulnerabilities quickly using targeted scanning techniques. During testing, I discovered a Local File Inclusion (LFI) vulnerability that allowed reading arbitrary files on the server, including /etc/passwd. By focusing scans on suspicious endpoints with user-controllable parameters, I was able to confirm and exploit the issue efficiently. This project demonstrates how strategic, targeted scanning can rapidly uncover critical vulnerabilities.

# Methodology

Step 1: Identified potentially vulnerable endpoints for file access (e.g., download, view, or export functionality).

Step 2: Performed targeted scans using Burp Suite on user-controllable parameters rather than scanning the entire application.

Step 3: Confirmed the presence of an LFI vulnerability by analyzing scanner results and application responses.

Step 4: Crafted a traversal payload (../../../../etc/passwd) to read sensitive system files.

Step 5: Retrieved file contents successfully, verifying the vulnerability and its exploitability under time constraints.

# Conclusion

This assessment confirmed a high-severity LFI vulnerability in the application. Implementing strict input validation, directory whitelisting, and secure file-handling practices is essential to prevent unauthorized access to system files and strengthen the application’s overall security posture.
