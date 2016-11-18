# Deliverable5

##Vulnerability 1

####Type of Attack: Cross Site Scripting(Reflected)  
####URL: http://demo.testfire.net/bank/login.aspx  
Steps to exploit:  
	
 	1. Open the http://demo.testfire.net/bank/login.aspx  
	2. Input “><script>alert(1);</script> to Username input box, and input 111 to Password input box, then click login button  
	3. Then you will see a pop-up window like below.


<img width="644" alt="1" src="https://cloud.githubusercontent.com/assets/16142079/20376754/728b287a-ac57-11e6-83f0-87284efa4bb6.png"> 


Q1. Part of InfoSec Triad: Integrity

Q2. Kind of Security Attack: Fabrication

Q3. active attacks

Q4. business value lost: unauthorized user may get user’s sessions, cookies information

Q5. possible ways to fix:	
	

     	* Do filtration to special character, for asp we can use Server.HTMLEncode(),
     	* Use the HTTP head to specify type,use and specify a character encoding such as ISO-8859-1 or UTF-8
     	* Recheck input validation,consider all potentially relevant properties
        * User can set the session cookie to be HttpOnly.


##Vulnerability 2

####Type of Attack: SQL Injection  
####URL: http://testphp.vulnweb.com/userinfo.php  
Steps to exploit:

	1. open http://testphp.vulnweb.com/userinfo.php in browser
	2. type ZAP' OR '1'='1' --  to Username input box, and 123 to password input box
	3. Then you will see one user’s information, change the address of it, then press update button.
	4. log out and use the same username and password to login, then you will see the address have changed to the one you input.  
	5. Then you will see following situation
  <img width="644" alt="2" src="https://cloud.githubusercontent.com/assets/16142079/20376775/a5a945de-ac57-11e6-8974-f1a7ba670233.png">
  
Q1. Part of the InfoSec Triad:  Confidentiality, Integrity 

Q2. Kind of Security attack: Interception, Modification  

Q3. Be passive when just looking the user’s information  
    		Be active when modify user’s information  
		
Q4. Business value lost: data loss, unauthorized access. Unauthorized user may login in this system and get some user's informaion 

Q5.Possible Solution:   

	* Do type and format check all data on the server side
	* Do filtration to special character
	* Recheck database information encipherment security.

##Vulnerability 3


####Type of Attack: SQL Injection－MySQL
####URL: http://testphp.vulnweb.com/signup.php  
Steps to exploit:  

	1. Open http://testphp.vulnweb.com/signup.php in browser
	2. Input ZAP' UNION ALL select NULL -- to Username input box
	3. Press signup button
<img width="794" alt="3" src="https://cloud.githubusercontent.com/assets/16142079/20405679/32ceaa1e-acd8-11e6-8f92-f9d43b52e7c0.png">  

Q1. Part of the InfoSec Triad:  Confidentiality  
Q2. Kind of Security attack: Interception  
Q3. passive attack, since it just get information, do not change info  
Q4. Business value lost: data loss, unauthorized access. Through trying different sql, unauthorized user may get lots of other users information.  
Q5.Possible Solution:  

	    * Do type and format check on user input data
	    * Do filtration to special character
	    * Recheck database information encipherment security.
	    * Apply a 'whitelist' of allowed characters, or a 'blacklist' of disallowed characteres in user input
	    * Grant the minimum database access
