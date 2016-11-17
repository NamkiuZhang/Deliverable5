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

