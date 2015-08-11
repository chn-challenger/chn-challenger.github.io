---
layout: post
title: Precourse 1st Friday Challenge
---

Don't tell anyone, but I am a Mac noob and a windows comfort user!  I have a very nice Macbook Pro and the first thing I did was to install bootcamp on it (travesty I know!).  After studying the precourse on command line, I have to say Mac is rather nice after all, I do not find it difficult to navigate and do basic things any longer:)

The 1st Friday challenge was fairly ok, the tasks gradually got more difficult, but it was manageable.  I completed everything but on submitting it said my 6 was wrong (adding a new env variable to my .bash_profile).  I was sure I did everything correctly, but for some weird reason it just wont work, and the variable is not even accessible from my current session!  

Anyway, eventually, after 30 mins of googling and trying everything, I stumbled onto something that solved my issue:

> source ~/.bash_profile

this is after I have appended the export to the file.  It seems to have 'reset' my profile to the correct file for bash, however I am still not 100% sure why it worked.  Here comes the bad part, I closed that session I was working on and reopened another, it turns out my previous work wasn't linked or some other issue has occurred and none of my answers worked any more!  In the end, I just redid everything, it didn't take very long I was surpised (10-15 mins), was actually good to practice again.

Recently I have been relaxing maybe a little too much!  I used to do a lot of codewars to keep sharp, I think its time to get that habit back.  The last kata I was working on is validating suduko, I think I will try that tomorrow!
