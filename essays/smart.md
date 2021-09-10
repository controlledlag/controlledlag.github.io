---
layout: essay
type: essay
title: Better Life With Smart Questins
# All dates must be YYYY-MM-DD format!
date: 2021-09-09
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img class="ui medium left floated image" src="../images/rtfm.png">

## What is a stupid question?

Stupid questions are bad. Stupid questions lower the chances of you receiving useful information to help solve your problem. A dumb question could have a bad structure, ambiguous answer options, or lack the information needed to help the person answering the question come to a helpful answer. Another thing that could be a factor is that there was a lack of research before even asking the question. Not looking into the problem and trying to find the answer before asking the question is also a contributor to stupid questions.

## How about a smart question?

As a student asking questions is a major part of our scholarly life. Also, as a  future developer we will eventually run into a problem that stumps us or goes over our head. Understanding how to ask a smart question will not only benefit us now but later as well. Here are some examples of stupid and smart question that I found on stackoverflow(A website for developers to ask questions)..

```
Q: What are the differences between git pull and git fetch?

```
```
A: In the simplest terms, git pull does a git fetch followed by a git merge.

You can do a git fetch at any time to update your remote-tracking branches under refs/remotes/<remote>/. This operation never changes any of your own local branches under refs/heads, and is safe to do without changing your working copy. I have even heard of people running git fetch periodically in a cron job in the background (although I wouldn't recommend doing this).

A git pull is what you would do to bring a local branch up-to-date with its remote version, while also updating your other remote-tracking branches.

```

```
Link
https://stackoverflow.com/questions/292357/what-is-the-difference-between-git-pull-and-git-fetch
```
 The person clearly did not do any research of his own before asking this question. Although he it is direct the answer is also very board as to the differences between the two. The asker also doesn't try to give out some information that he/she knows and is basically asking for the entire description. Although the question was answered the answer was vauge and it is hard to tell weather the asker was able to fix his probelm with the given solution. Next is an example of a smart question.

```
Q: 
I've been using the == operator in my program to compare all my strings so far. However, I ran into a bug, changed one of them into .equals() instead, and it fixed the bug.

Is == bad? When should it and should it not be used? What's the difference?
```

```
== tests for reference equality (whether they are the same object).

.equals() tests for value equality (whether they are logically "equal").

Objects.equals() checks for null before calling .equals() so you don't have to (available as of JDK7, also available in Guava).

Consequently, if you want to test whether two strings have the same value you will probably want to use Objects.equals().

// These two have the same value
new String("test").equals("test") // --> true 

// ... but they are not the same object
new String("test") == "test" // --> false 

// ... neither are these
new String("test") == new String("test") // --> false 

// ... but these are because literals are interned by 
// the compiler and thus refer to the same object
"test" == "test" // --> true 

// ... string literals are concatenated by the compiler
// and the results are interned.
"test" == "te" + "st" // --> true

// ... but you should really just call Objects.equals()
Objects.equals("test", new String("test")) // --> true
Objects.equals(null, "test") // --> false
Objects.equals(null, null) // --> true
You almost always want to use Objects.equals(). In the rare situation where you know you're dealing with interned strings, you can use ==.
```

Here the user asks a very direct questino without beating around the bush. They also give an example of what kind of answer they are trying to achieve as well as some background information into the probelm at hand. Giving specifics without going overboard. As you can tell by the answer it is very specific and there is even an example of how it should look like as opposed to the dumb question. This just goes to show that understanding how to ask a smart question really is a fruitfull skill to learn.

```
Link
https://stackoverflow.com/questions/513832/how-do-i-compare-strings-in-java
```
