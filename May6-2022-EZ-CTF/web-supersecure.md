## Web - Super Secure


![](/May6-2022-EZ-CTF/img/ez-ctf-web0.PNG)

Once we select the site we're presented with a login form with username and password.

![](/May6-2022-EZ-CTF/img/ez-ctf-web1.PNG)

Testing the standard stuff such as "admin, admin", "admin, password" etc. leaves a response outline above where the username and password do not match. 

Next let's test for any SQL injection possibilities with ' . We recieve the bellow error message:

![](/May6-2022-EZ-CTF/img/ez-ctf-web2.PNG)

Seems vulnerable to SQLi and we have the password there.

Let's make username evaluate to true and input our password:

![](/May6-2022-EZ-CTF/img/ez-ctf-web2-payload.PNG)

We've logged in and got the first flag! 

![](/May6-2022-EZ-CTF/img/ez-ctf-web3-solve.PNG)

### Resources
