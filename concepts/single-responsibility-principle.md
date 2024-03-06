# Single Responsibility Principle (SRP)

Originally stated as: "A Module should have one, and only one, reason to change."

If I were to attempt to translate this for a novice programmer, I might say: "A module should do tasks for only one department in a company."

A module shouldn't have methods to:

+ Calculate sales tax (Accounting Dept)
+ Create a shipping label (Shipping Dept)
+ Export marketing data (Marketing Dept).

If a software module did all of these things, it is doing **too much**.
Breaking the module into three different modules, is called _Separation Of Concerns_.
You aren't concerned about breaking the shipping labels when making a change to sales tax calculations.

In his blog article regarding _The Single Responsibility Principle_[^1], Robert C. Martin summarizes the idea like this:

> Gather together the things that change for the same reasons. Separate those things that change for different reasons.

## References

[^1]: [The Single Responsibility Principle](https://blog.cleancoder.com/uncle-bob/2014/05/08/SingleReponsibilityPrinciple.html) by Robert C. Martin.
