# Deliverable5

Vulnerability 1

Type of Attack: Cross Site Scripting(Reflected)

URL: http://demo.testfire.net/bank/login.aspx 
Steps to exploit:

    1.open the http://demo.testfire.net/bank/login.aspx
    2 input “><script>alert(1);</script> to Username input box, and input 111 to Password input box, then press login button
    3. Then you will see a pop-up window like below.





Q1. Part of InfoSec Triad:

Q2. Kind of Security Attack: Fabrication

Q3. active attacks

Q4. business value lost: user’s session, cookies to 

Q5. possible ways to fix:

    1. do filtration to special character, for asp we can use Server.HTMLEncode(),
    2. Use the HTTP head to specify type,use and specify a character encoding such as ISO-8859-1 or UTF-8
    3. recheck input validation,consider all potentially relevant properties

Vulnerability 2

Type of Attack: SQL Injection
URL: http://testphp.vulnweb.com/userinfo.php
Steps to exploit:

	1. open http://testphp.vulnweb.com/userinfo.php in browser
	2. type ZAP' OR '1'='1' --  to Username input box, and 123 to password input box
	3. Then you will see one user’s information, change the address of it, then press update button.
    4. log out and use the same username and password to login, then you will see the address have changed to the one you input.
