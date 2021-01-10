---
title: What is Aggregation?
date: "2021-01-10T17:12:03.284Z"
description: ""
---

```
Combining several objects into a new one is known as aggregation or composition.

```

The aggregation concept illustrates the ability to combine several objects into a new one. Aggregation is a powerful way to separate a problem into smaller and more manageable parts (divide and conquer).

When a problem scope is so complex that it's impossible to think about it at a detailed level in its entirety, you can separate the problem into several smaller areas, and possibly then separate each of these into even smaller chunks. This allows you to think about the problem on several levels of abstraction.

A personal computer is a very complex object. You cannot think about all the things that need to happen when you start your computer. But you can abstract the problem saying that you need to initialize the objects it consists of: the Monitor object, the Mouse object, the Keyboard object, and so on. Then you can dive deeper into each of the sub-objects. This way you are composing complex objects by assembling reusable parts.

To use another analogy, a Book object could can contain (aggregate) one or more author objects, a publisher object, several chapter objects, a table of contents, and so on.
