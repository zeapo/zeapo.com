Hello Ghost!
===========

Well, today I have discovered how easy it has become to get up and running with nginx and Ghost. But also, how fast you can get an email webserver to work properly. Everything described here is just an introduction, I will detail that in a post later.

#### Haaaaaave you met iRedMail?

Getting *postfix* and *dovecot* running is not an issue, getting them to run properly with *sasl* and all the fancy SSL can be tedious. 

Once downloaded and run, the script installs everything you need and configure them. However, it also installs *apache* and configures *rouncube* and co. I didn't really like this, but you can disable features by either uninstalling or restricting access to those directories.

Another issue is that if you have *nginx* running to serve your sweet *nodejs* you'll get struck with the infamous `port already used` or something like that. The solution is to use *nginx* as a reverse proxy to *apache* and do that for both the ports 80 and 443. Why you ask? Because *roundcube* is served through https, and if you want to put anything else through https other than that *apache* wont like it!
