---
layout: post
title:  "Objects, Classes, & Scope"
date:   2015-03-06 11:21:45
categories: jekyll objects classes scope
---

#**Sensei says: "To master craft, spend less time doing not craft."**

![Zen Pic][ZenPic]

With a semester in C being my only pervious programming experience, my tendency is to jump willy-nilly into loops and conditionals.  However, with an Object Oriented (OO) language like Ruby, it is often beneficial to breakdown problems into objects and classes. Today I focused on learning the important characteristics and uses of objects and classes.

**Class methods and instance methods:**
The same way that variables can have different scopes, methods can have different scopes as well. A class method is a function called on the entire class and not specific to any one instance of a class. However, an instance method is a function specific to an instance of a class. For example, the color options for a class Car would be a class level variable because it’s not specific to a single instance, where the color of a single car would be an instance level variable.

**Public and Private methods:**
Methods can have different scopes and are primarily defined as public, protected, or private. It is beneficial for a method to be public if it needs to be accessed or modified and it’s better for a method to be defined as private if accessing the method is potentially harmful. For example, given a class BankAccount, the name and account type may be a public method whereas transferring money between accounts would be a private method.

**attr_accessor & friends:**
Ruby’s built in attr methods are useful for defining getters and setters in a class. If you want to be able to read an attribute from a class you can use attr_reader, to define an attribute, attr_writer, or attr_accessor to do both. You can also define your own custom getter and setter methods.

[ZenPic]: http://everydayfunnyfunny.com/wp-content/uploads/2010/07/zen-question-you-need-to-read-more-than-twice.jpg

