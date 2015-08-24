---
layout: post
title: Pair Programming with Harriet and More Codewars!
---

Last Friday, we organized pair programming amongst our September cohort, we actually had 11 of us turning up that was great.  Phillip who wanted to come but couldn't, still contributed by writing us a script to produce random pairs, while leaving out an unlucky 11th person.  The program worked great, luckily for me I was paired with Harriet.  After a brief discussion, we decided perhaps we could also make ourselves useful by making a method to produce random pairs on the basis that a person does not get paired with someone they have already paired with previosly.

In true spirit of pair programming, even though both of us barely knew how it was supposed to work.  We followed Nikesh's guide to setup Github Ping Pong?  We made an initial test with me creating a file, Harriet pulling it, then she making a change, me pulling it..and it indeed worked!  So I decided to try to be strict about Navigator/Drive swaps, and got on with the task of writing the code.

In our initial version, we came up with a brilliantly simple and lazy idea :) - keep running Phillip's method until it produced a set of pairings for which none has happened previously.  The idea was simple and intuitive, and making use of code we already have for laziness sake ! (Sorry Phillip we had to amend your code by remove your witty comments to produce an array of pair arrays for our purpose. :))  After what seemed to be hours of labour, we finally mannaged to transfer our idea into code, and it worked!  Hurray!!!  There was indeed elation when the recursions happened and it returned a brand new pairing.

However, we very quickly realised it was not however very efficient way of producing the pairing.  And for me, being a maths guy, I started to think of doomsday scenario, say you had 1000 people to pair (why and how? no clue!), and since each person has to pair with 999 other people, once a person has paired with 998 people, there is only one pairing left that has to happen next.  Now then, with our program, we will have to be extremely lucky to hit that *one* combination from what will be zillions of combinations possible, and we may not be that lucky, it may even crash the computer!  Ok back to reality, we are pretty certain that given our use of the code we will never ran into such problems, but nonetheless we were so fired up by our previous victory, we felt we had to attempt a more efficient method of doing the same thing. 

This next method, is also very natural, though the coding seems more demanding.  The idea is: before we select a random person from the list of people to pair with a given person (e.g. John), we should remove all those people's names who has already paired with John (Doh! wasn't it obvious Joe???), so when we pick someone at random from the remaining names, we are guaranteed to get a new pairing...  Now thinking back, not sure why we didn't think of that first time!  Anyway, we ploughed ahead with this.  After what seemed more hours of labouring (we wrote less than 30 lines of code), we finally got close to get it working, at this point, graduation was about to start, and Harriet and I were both exhausted.  So there ended our pairing session, it was great fun and we both learnt a great deal.  Harriet seemed to think she learnt more from me, but she doesn't realise by having to explain some ideas to her help me understood them far better, so it was definitely a great team effort!  

The graduation was very interesting!  We were shown many interesting quality projects, and it is daunting to think it will be us a little more than 12 weeks!  Can scarcely believe it is possible, but then again this is why we signed up.  In addition, the boooooz was goooooooood - while it lasted, which unfortunately was not very long.  Although people like _me_ who drank 4 bottles rather quickly certainlly didn't help.  In the end, we seemed to have consumed everything - the snacks, boozz, soft-drinks, even - water!  So what little choice did we have but to invade the pub! There were too many Maker's people at the pub, there were little space left anywhere, we could not even fit into the chalk lines outside the pub!  It was great times, too bad I had to work the next day, so I had to be sensible and head home early with Tim (who happened to live very close to me!).  

Wow....so much happened already, and the weekend hasn't even began!  The weekend was far quiet for me, I had to work on Saturday, and a bit on Sunday, and spent a lot of time with my lovely son.  

![](http://i.imgur.com/Zc6RjI6.jpg)

Today - Monday, I felt I had to work hard on Ruby.  Although I have done a lot of codewars before, but I haven't actually worked on the recommended katas, so I spent today working through them.  They were indeed very useful and I felt I learnt a great deal.  Only one week left to prepare, my plans is to have done all the recommended katas, gone through ruby kickstart completely, and read as much as I can of the Rubyist!  Perhaps I am too ambitious hahaha and I am just kidding myself!








       



