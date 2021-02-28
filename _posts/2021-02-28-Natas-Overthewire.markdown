---
layout: post
title:  Natas - Overthewire
date:   2021-02-28 11:01:23 -0700
categories: Security
---

Started off with the NATAS challenge in overthewire and here are some of my notes during the game

Level0:
URL:    http://natas0.natas.labs.overthewire.org/
Cred:   natas0/natas0
Hint:   You can find the password for the next level on this page. 
Actions: Viewed page source and got the password for the next level

Level1:
URL:    http://natas1.natas.labs.overthewire.org/
Cred:   natas1/gtVrDuiDfck831PqWsLEZy5gyDz1clto
Hint:   You can find the password for the next level on this page, but rightclicking has been blocked! 
Actions: Ctrl+U to view the page source to get the password for the next level

Level2:
URL:    http://natas2.natas.labs.overthewire.org/
Cred:   natas2/ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi
Hint:   There is nothing on this page 
Actions: There is an image referenced at files/pixel.png. Hence try to access what is that image which is a black image. Hence came backt to http://natas2.natas.labs.overthewire.org/files and found that there is a users.txt. Find the password for next level in there.

Level3:
URL:    http://natas3.natas.labs.overthewire.org/
Cred:   natas3/sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
Hint:   There is a hint that even Google can't find this. 
Actions:So it means something to do with robots.txt.
        http://natas3.natas.labs.overthewire.org/robots.txt
        User-agent: *
        Disallow: /s3cr3t/
        http://natas3.natas.labs.overthewire.org/s3cr3t
        leads to users.txt and we can get the password from there.

Level4:
URL:    http://natas4.natas.labs.overthewire.org/
Cred:   natas4/Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
Hint:   Access disallowed. You are visiting from "" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/"
Actions:This means that it is looking in for the Referer (Note the spelling is incorrect, but it is intentional atleast from my part!) 
        Add a HTTP Request header with Referer: http://natas5.natas.labs.overthewire.org/
        The page comes back with "Access granted. The password for natas5 is iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq"

Level5:
URL:    http://natas5.natas.labs.overthewire.org/
Cred:   natas5/iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
Hint:   
Actions: