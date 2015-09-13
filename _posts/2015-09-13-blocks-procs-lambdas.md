---
layout: post
title: Block, Proc and Lambda in Ruby
---
In short:
* Blocks are not objects, while Procs and Lambdas are.
* A method can only take at most one block argument, while it can take many procs and/or lambdas.
* Lambdas must be passed correct number of arguments when called, while procs can still be called with incorrect number of arguments.
* Return in lambdas will return to within the method from which it was called, while a return in procs returns and immediately exit the method from which it was called.

*Basic examples*

```ruby
# Block Examples
['Joe','Lulu'].each {|name| puts 'Hello '+name+'!'}   
# block is in between the curly braces which could be replaced by do end

# Proc Examples             
proc1 = Proc.new { |x| puts x*x*x }
[2,5,9].each(&proc1)              
# The '&' tells ruby to turn the proc into a block

proc2 = Proc.new { puts "Hello Ruby" }
proc2.call                     
# The body of the Proc object gets executed when called

# Lambda Examples            
lambda1 = lambda { |i| puts 'hello! '*i }
[1,2,3].each(&lambda1)
# The lambda is turned into a block by & which is then passed to each

lamda2 = lambda { puts "Hello Rubyists!" }
lamda2.call
# When called, it executes just like a proc.
```

*Procs vs Lambdas*

```ruby
l = lambda { |x| puts x }  # creates a lambda that takes 1 argument
l.call('hello')            # prints out hello
l.call                     # ArgumentError: wrong number of arguments (0 for 1)
l.call('hello','joe')      # ArgumentError: wrong number of arguments (2 for 1)
p = Proc.new { |x| puts x } # creates a proc that takes 1 argument
p.call(2)                   # prints out 2
p.call                      # returns nil
p.call(1,2,3)               # prints out 1 and forgets about the extra arguments
```

*Procs vs Lambdas - returns*

```ruby
def method1
  lam = lambda { return 'I am lambda!' }
  puts lam.call
  puts "I am method!"
end

method1  
# puts 'I am lambda!' followed by 'I am method!'

def method2
  proc = Proc.new { return 'I am lambda!' }
  proc.call
  puts "I am method!"
end

method2  
# puts nothing at all, calling proc also existed the method
```

The flexibility afforded by block, lambda and proc usage is one of the reasons ruby is such a great language!
