# Online-Traffic-Offense-Management-System-1.0---Remote-Code-Execution-RCE-Unauthenticated-(Fixed)

<br>

## Online Traffic Offense Management System 1.0 - Remote Code Execution (RCE) (Unauthenticated) has been fixed.

<br>

### Description

When the exploit code asked us for a url and we gave the target url, the exploit worked, but when we entered commands such as id, whoami, pwd, the code exploded. For this, we go into the code and request = requests.post( find_shell.get("src") + "?cmd=" + cmd, data={'key':'value'}, headers=headers)

In this part of the code we need to give "target_url:port", here I will get this part from the user directly from the terminal and catch errors with try except blocks, so that we will have a smoother and debuggable code.

Usage: python2 toms.py <target:_url:port>

Example: `python2 toms.py http://<10.10.10.10.1:445>`

Url: http://10.10.10.1:445/management

Fixed: debug operation with try,except block
Fixed: receive input from the user and process it from the terminal
