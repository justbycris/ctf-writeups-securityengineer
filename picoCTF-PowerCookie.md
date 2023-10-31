# Power Cookie CTF - picoCTF 
Beginning this CTF I assumed by the name of it: 'Power Cookie' that it has to do with tampering cookies. 
<img width="683" alt="Screenshot 2023-10-31 at 9 46 45 AM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/bc72811c-d610-4488-b58b-0d2fd3f19e63">

1. My first step was to open Burp Suite and turn on my broswer's burp suite proxy.
2. On Burp Suite I turn On the intercept, in the Burp Suite proxy and request to reload the page:
<img width="663" alt="Screenshot 2023-10-31 at 9 46 28 AM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/277cb60a-5c3f-48d1-8dfc-063b767a80c5">

3.I can see that BurpSuite has intercepted the request when clicking 'Continue as guest'

4. In the header request, we can see that there is indeed one cookie: **isAdmin=0**
   <img width="680" alt="Screenshot 2023-10-31 at 9 35 26 AM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/154cea5b-5faf-4e58-8053-147e581a300b">
5. If we send the request with **isAdmin=0** the server's response would be:
   <img width="762" alt="Screenshot 2023-10-31 at 9 41 32 AM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/00ffcf34-56a8-46b3-bfe3-167d7d0f33ae">
6. I send that request to the Repeater in BurpSuite so we can modify it.
7. Once I have the request header in the repeater, I modify the cookie to **isAdmin=1**
8. We send the request and success! We got the flag: 
<img width="780" alt="Screenshot 2023-10-31 at 9 42 06 AM" src="https://github.com/justbycris/ctf-writeups-securityengineer/assets/65434648/79705e07-fbae-47d4-a32f-4f081f7d23fc">
