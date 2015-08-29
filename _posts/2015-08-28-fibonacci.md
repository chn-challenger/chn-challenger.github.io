---
layout: post
title: Speed of finding Fibonacci nth term
---

As we are in our last week of pre-course, the main task is to focus on reading as much of well-grounded rubyist as possible.  However, I thought it would be good to at the same time, keep myself sharp with a kata or two each day.  So I came across this [kata](http://www.codewars.com/kata/559a28007caad2ac4e000083) that involve some maths, I had a look at it and was happy to realise it's a fibonacci sequence, something I am familiar with.  I can calculate the nth term with recurssion or better still, I know the fibonacci formula for the nth term:

![](http://i.imgur.com/RyK9UfP.png)

so this should be easy enough, let's try a few things, it shouldn't take long.  So off I went, set everything up, first I tried the formula, it worked for small cases, stopped working when the resulting number was more than 20 digits, which was no good at all, just no way accurate enough.  I tried to get ruby to take more decimal places in intermediate calculations, after a lot of googling still could not get it to work.  At that point, I read discussions about the kata, to my dismay, we are expected to calculate Fibonacci terms which have about 50 thousand *digits*.  

Ok so I tossed out the formula, and brought in a basic fibonacci recurssion method.  Something along the lines of 

```ruby
def fib(n)
  return 0 if n == 0
  return 1 if n == 1
  fib(n-1) + fib(n-2)
end
```

Sadly, when I ran for fib(100000), it was still calculating a minute later.  Definitely still too slow, by this time, I was intrigued - I had to resolve it somehow.  Reading more deeply into some people's comments, I realised I needed to find faster methods to generate the terms.  [This](http://www.nayuki.io/page/fast-fibonacci-algorithms) link had some particularly good methods that are not too hard to implement.  And after some serious labour:

```ruby
def fib_double f_k, f_k1, times
	for i in 1..times
		f_k, f_k1 = f_k*(2*f_k1 - f_k), f_k1**2 + f_k**2
	end
	result = []; result << f_k; result << f_k1
end

def fib n
	return nil if n < 0
	first_fibs = [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 
				987, 1597, 2584, 4181, 6765, 10946, 17711, 28657, 46368, 75025, 
				121393, 196418, 317811, 514229, 832040, 1346269, 2178309]
	m = n.to_f; i = 0
	while m > first_fibs.length - 2
		m /= 2
		i += 1
	end
	m = m.to_i

	fib_db = fib_double first_fibs[m], first_fibs[m+1], i
	f_k_2 = fib_db[0]; f_k_1 = fib_db[1]

	(n-m*(2**i)).times do
		f_k_2, f_k_1 = f_k_1, f_k_2+f_k_1
	end
	return f_k_2
end

p fib(999999).to_s.length  #=>  208988 #digits long  1.2 seconds
```
Eventually got it to be fast enough, this final version calculates the 999999th Fibonacci number which seems to be over 200 thousand digits long in 1.2 seconds!  And finally, I was able to pass the kata with a lot of time to spare, as my test took only 341ms!  It turns out they only tested for n below 100,000.


This has been an unexpectedly intriguing and fulfilling journey, and may maths and coding continue this happy marriage for years to come!  Now, the final push to get as ready as I can ever be for Maker's academy.  Only a few more days to go...





       



