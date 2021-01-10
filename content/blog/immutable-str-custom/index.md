---
title: How to create your own immutable class like String in java?
date: "2021-01-10T17:12:03.284Z"
description: ""
---

Before knowing how to create own immutable class, Need to understand String concepts:

As you know in Java, String class is immutable. Value of a String Object once created cannot be modified. Any modification on a String object creates a new String object. All strings literals are stored in "String constant pool". If compiler finds a String literal, it checks if it exists in the pool. If it exists, it is reused.

```
If you use String str1 = "Hello";
The above statement creates (Both created in common pool)
1 string object value i.e., Hello
1 reference variable i.e., str1.
```

```
If you use String str2 = new String("Hello");
The above statement creates
1. The first object will be created in java permanent heap memory i.e., str2
2. Second object will be created within string constant pool i.e., Hello
```

Java has provided a special mechanism for keeping the String literals - in a so-called string common pool. If two string literals have the same contents, they will share the same storage inside the common pool. This approach is adopted to conserve storage for frequently-used strings.

On the other hand, String objects created via the new operator and constructor are kept in the heap. Each String object in the heap has its own storage just like any other object. There is no sharing of storage in heap even if two String objects have the same contents.

Steps to create custom Immutable class?
Don’t provide “setter” methods - Setter methods are meant to change the state of object and this is what we want to prevent here.
Make all fields final and private. This is another way to increase immutability. Fields declared private will not be accessible outside the class and making them final will ensure the even accidentally you can not change them.
Don’t allow subclasses to override methods The simplest way to do this is to declare the class as final. Final classes in java can not be overridden.
Special attention when having mutable instance variables
