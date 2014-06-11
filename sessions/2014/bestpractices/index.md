---
layout: presentation
year: 2014
title: Best Practices
instructors:
 - Jonathon
---
<section markdown="block">
<p style="text-align:center">What are "Best Practices"?</p>

Approaches and techniques that reduce development time, improve quality and simplify maintenance.

\"Best Practices\" could be the sole subject of a two week course!  The content in this lesson will focus on practices that simplify maintenance, though others will be discussed.
</section>

<section markdown="block">
<p style="text-align:center">Why Maintenance?</p>

The majority of the software lifecycle is spent in maintenance.  More time is spent correcting defects and adding features after the software is delivered than in its initial development.  Additionally, the same practices that simplify maintenance also support correcting defects in software during its initial development.
</section>

<section markdown="block">
To this end, consider these practices:
</section>

<section markdown="block">
<h5 style="text-align:center">Coding Conventions</h5>

A coding convention is a set of rules for writing and organizing code.  Following the set of
rules will not guarantee good quality code.  The purpose of a coding convention is to communicate
intent between developers.  The actual convention used is not important; what is important is
that it is adhered to.
</section>

<section markdown="block">
You can have conventions for:

* Comments
* Indent style
* Naming
* Programming practices

<br />

I will not cover all of these today.  I would like to cover Common Naming Conventions.
</section>

<section markdown="block">
* UpperCamelCase (often used for classes)
* lowerCamelCase (often used for class methods and variables)
* CAPITAL_UNDERSCORE (often used for constants)
* pot_hole_case (often used for variables and functions)
* Single characters are often used for short temporary variables such as indexes.  The characters
i, j, k are often used as integers; c, d, e are often used as characters; s is often used as a string.

<br />

Always use descriptive names unless name is for a short temporary variable.
</section>

<section markdown="block">
{% highlight python %}
import os
import sys
import subprocess
import nltk
import plain

class ProcessedPost(object):
  def __init__(self, file_name=None, raw_dist=None):
  self.file_name = file_name
  self.raw_dist = raw_dist
  self.processed = nltk.FreqDist()

def main():
  base_dir = sys.argv[1]
  posts = []
  global_dist = nltk.FreqDist()

  for path, sub_dirs, file_path in os.walk(base_dir):
    for sub_dir in sub_dirs:

...

  weighted_terms = dict()

  for p in posts:
    keys = p.processed_posts.keys()
    for k in keys:
      if weighted_terms.has_key(k):
{% endhighlight %}
</section>

<section markdown="block">
<h5 style="text-align:center">Engineering Practices</h5>

<br />
There are legions of them.  Here are a few . . .
</section>

<section markdown="block">
Don`t Repeat Yourself (DRY) - Any series of steps that are performed multiple times should be put
into a programming construct such a loop, function or class.  That ensures the series of steps is
performed the same way every time.
</section>

<section markdown="block">
You aren\'t going to need it (YAGNI) - Do not implement functionality until you need it.  The danger
is if you don\'t use it, the unused function may have a defect or maintenance changes elsewhere will
introduce a defect.  A maintenance programmer may see the previously unused function, believe it works
and try to use it.
</section>

<section markdown="block">
Don`t Make Me Think - Any code written should be easy to read and understood with the minimum
effort required.  This concept is related to:

Do The Simplest Thing That Could Possibly Work - Avoid unnecessary complexity.
</section>

<section markdown="block">
Single Responsibility Principle - A component of code (class or function) should perform a single well defined task.  Code with unexpected side-effects can be overlooked by the maintenance programmer.
</section>

<section markdown="block">
Minimize Coupling - Coupling is when a section of code depends on another section of code.  Coupling is an advanced topic and there are many types.  One dangerous type is \"content coupling\". In content coupling, changes to data values in one section of code can directly effect the behavior of another section of code.
</section>

<section markdown="block">
<p style="text-align:center">These are Best Practices, not a set of laws.</p>

There are times a best practice can be disregarded.  When to do so comes with experience.  Often this is when one practice conflicts with another.

With YAGNI, one may forsee future needs and build the code in such a way that supports these needs.  Or codes to test for errors that can`t occur, anticipating future changes in input.

Sometimes you *do* need to repeat yourself.  It can happen that implementing DRY makes the code very difficult to follow.  What is more important, DRY or \"Don`t make me think\"?
</section>

<section markdown="block">
<h5 style="text-align:center">For Object Oriented Programming (OOP)</h5>  

There are many good practices for OOP.  Two are discussed here.
</section>

<section markdown="block">
<center>Hide implementation details.</center>
<br />
Use an object`s methods and constructor to hide the details of its operation.  That way changes to the object will not affect the program and changes to the program will not affect the object.
</section>

<section markdown="block">
Law of Demeter - Put simply, an object can only communicate with classes it inherits from, objects
it contains, and objects passed by argument to a method.

This law ensures minimal coupling, which was mentioned earlier.
</section>

<section markdown="block">
<h5 style="text-align:center">Additional Practices</h5>
</section>

<section markdown="block">
Refactor often - Refactoring is reorganizing your code to ensure the above principles are adhered
to.  As a side benefit, it can also expose defects in the coding.
</section>

<section markdown="block">
Tools - Pick a small set of software engineering tools and learn them well.
</section>

<section markdown="block">
Code defensively - Think about what can go wrong and apply good practices appropriately.
</section>

<section markdown="block">
<h5 style="text-align:center">Assignment</h5>

Two poorly designed code modules will be provided.  This is not a debugging
exercise.  The code runs and if there is a defect, it is due to design issues.
For each code module:

(a) Identify all design flaws.  
(b) Explain what problems the flaws can cause.  
(c) Modify the code to repair the flaws.  
(d) Be prepared to justify your modifications.

</section>
