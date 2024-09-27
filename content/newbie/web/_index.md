---
title: "Web"
date: 2024-06-18T13:48:52+02:00
---

I am assuming that you have used a web browser to visit a website
at some point! Since this part of the Internet is so widely used,
it is of great interest to us passionate about cybersecurity.

The most simple way to start digging deeper into websites is
viewing the source. You can do this by either pressing F12 on
your keyboard when visiting a website, or right-click and select
"View Page Source" or "Inspect". You can also add "view-source:"
in front of the URL.

<img width="100%" style='border:1px solid #FFFFFF' src="/images/newbie-web1.png" />

Here you can find JavaScript adding functionalities to the website, references
to hidden or forgotten pages, and sometimes interesting comments or even
passwords (yes, it happens).

You might have opened the browser dev tools (F12 or "Inspect") which
can show you a lot more about the website. Here you can inspect the
traffic to and from the webserver, view and modify your cookies, and
run JavaScript.

Sometimes you might want a web proxy, an application which intercepts the
packets from and to your browser. In the application you can view and modify
fields and automate tests.  Also keep an eye on the URL, it might show you some
interesting parameters that you can play with.

There is a common type of web attacks classified as "injections".
SQL injection, JavaScript injection (also known as Cross-site scripting (XSS)),
and Template injection. All of these methods rely on input fields to
change the behavior of the website.

### Useful platforms
- https://overthewire.org/wargames/natas/
- https://tryhackme.com/path/outline/web
- https://academy.hackthebox.com/module/details/35
- https://academy.hackthebox.com/module/details/75

### Useful tools
- curl
- burpsuite
- mitmproxy
- wappalyzer
- sqlmap

### Try your skills
If you feel ready then you can try to solve our [Web
challenges](http://intro.kauotic.se) (registration code: 1337).
When you have solved three of them, head over to one of our CTF events
and you will get a sticker!
