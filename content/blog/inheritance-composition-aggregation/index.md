---
title: Inheritance, Composition, and Aggregation in OOPS?
date: "2021-01-01T22:12:03.284Z"
description: ""
---

Complex class structures can be built through inheritance, composition, and aggregation.

===> Inheritance establishes an “is-a” relationship between classes.

1. The subclass has the same features and functionality as its base class, with some extensions.

2. A Car is-a Vehicle. An Apple is-a Food.

===> Composition and aggregation are the construction of complex classes that incorporate other objects.

1. They establish a “has-a” relationship between classes.

2. A Car has-a Engine. A Customer has-a CreditCard.

In composition, the component object exists solely for the use of its composite object.

1. If the composite object is destroyed, the component object is destroyed as well.

2. For example, an Employee has-a name, implemented as a String object. There is no need to retain the String object once the Employee object has been destroyed.

In aggregation, the component object can (but isn’t required to) have an existence independent of its use in the aggregate object.

1. Depending on the structure of the aggregate, destroying the aggregate may or may not destroy the component.

2. For example, let’s say a Customer has-a BankAccount object. However, the BankAccount might represent a joint account owned by multiple Customers. In that case, it might not be appropriate to delete the BankAccount object just because one Customer object is deleted from the system.

Notice that composition and aggregation represent another aspect of encapsulation. For example, consider a Customer class that includes a customer’s birthdate as a property. We could define a Customer class in such a way that it duplicates all of the fields and methods from and existing class like Date, but duplicating code is almost always a bad idea. What if the data or methods associated with a Date were to change in the future? We would also have to change the definitions for our Customer class. Whenever a set of data or methods are used in more than one place, we should look for opportunities to encapsulate the data or methods so that we can reuse the code and isolate any changes we might need to make in the future.

Additionally when designing a class structure with composition or aggregation, we should keep in mind the principle of encapsulation when deciding where to implement functionality. Consider implementing a method on Customer that would return the customer’s age. Obviously, this depends on the birth date of the customer stored in the Date object. But should we have code in Customer that calculates the elapsed time since the birth date? It would require the Customer class to know some very Date-specific manipulation. In this case, the code would be tightly coupled –- a change to Date is more likely to require a change to Customer as well. It seems more appropriate for Date objects to know how to calculate the elapsed time between two instances. The Customer object could then delegate the age request to the Date object in an appropriate manner. This makes the classes loosely coupled –- so that a change to Date is unlikely to require a change to Customer.
