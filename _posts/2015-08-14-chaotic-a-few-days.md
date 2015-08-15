---
layout: post
title: Chaotic A Few Days
---

The day before yesterday - Wednesday was the last oppotunity to take my family out this week, and the weather was great, so we headed down to Brighton.  Not doing much work is bad, but having completed the git work and having done most of Chris Pine's book before the pre-course, it seems right to spend one day of what's left of the summer with my family and my one year old son - Matthew.  Anyway, it was a great but exhausting day, we had annual tickets to Brighton aquarium, well worth a vitit if anyone heads to Brighton.  Also had some beautifully fresh seafood at 'Fish + Liquor' restaurant along Madeira Drive, highly recommend.

Then came Thursday, A-level results day.  It is easy for me to forget that less than two months ago, I was working like a lunatic to prepare my students for their A-level Maths and Further Maths exams. Thankfully, they have all done very well, mostly A stars.  Spent the rest of the day talking to students and helping some of those who missed their offers for reasons other than maths...  It is a satisfactory end to my old career, well I wish it has all ended, but I still need to keep working one day a week to feed my family!

Today (Friday), did some more work on ruby, managed to spend some hours on chapter 11, writing some methods to move files, search files etc...  Only to find out later, very little was required to pass rspec on chapter 11, no matter however, all good practice.

I still had a little trouble with git and github, just achieve some basic goals.  So I ended up doing lots of experimentation, and here are my conclusions (I am sure my understanding will improve later!...I hope!):

**Make a new branch - edit - commit - merge / overwrite master with these**
 
```sh
$ git branch -b new_branch
$ <make edits, new files, delete files>
$ git add -A
$ git commit -m "Some suitable comment"
$ git checkout master
$ git merge new_branch
```
**Going back to an earlier commit and override master**

```sh
$ git checkout <id_of_commit>
$ git checkout -b new_branch_name
$ git merge -s ours master
$ git checkout master #maybe asked to put comment, just :q  it
$ git merge new_branch_name
```
The Octocat challenge wasn't too bad, although I completely did not realse the concept of remote upstream is *different* from just origin connection I use to push and pull...well until near the end hahaha.  I probably still don't 100% get it, but at least I now know its something different and know how to set it up.  What fun!  We will all get there!

