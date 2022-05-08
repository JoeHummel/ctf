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
