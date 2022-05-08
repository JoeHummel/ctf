## Web - I made a blog!

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog-0.PNG)

Once we navigate to the site we can look around and see some things. Initially I poked around the source to see if there was anything on either the main page or blog pages but nothing stood out. 

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmageablog-1.PNG)

Next standard step was to look to see if there was a robots.txt (Robots.txt is used to let the search engine crawlers to know what pages they shouldn't look at)

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog2.PNG)

We see a disallow for flag.php, so lets go ahead and look at this page. 

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog3.PNG)

Keyword being "filter" here which will be used later in the challenge. 

Since the title of the challenge involves blogs i'm going to look around the blog pages a bit more. 

I look around and see an interesting URL where it's pulling the blog file. 

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog-4.PNG)

Lets try some Local File Inclusion and try to get /etc/passwd maybe

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog5.PNG) 

This gives us the path so we could actually grab /etc/passwd with some directory traversal ../../../etc/passwd . That doesn't give us any flags or anything but let's see if there's anything with flag.php we can grab. I tried similar to see if there were any flag.php that we could grab but nothing came up. Thinking back to the hint from /flag.php with the keyword "filter". Some quick google searching came up with a way for us to use PHP filter to bypass if there are some restrictions and base64 encode it. 

We edit our URL to: http://ez.ctf.cafe:9999/blog-posts.php?file=php://filter/convert.base64-encode/resource=flag.php

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog6.PNG) 

We've got a Base64 encoded string now so let's go ahead and decode this which gives us the flag

![](/May6-2022-EZ-CTF/img/ez-ctf-web-challmadeablog7.PNG)

### Resources

[Local File Inclusion](https://www.aptive.co.uk/blog/local-file-inclusion-lfi-testing/)

