# Dry Programming Isn't Always Best

## Counterpoint to the DRY Principle

In the book _Software Mistakes and Tradeoffs_[^1], the authors make this point about incidental duplication:

> Sometimes what looks like duplication is just "two different things that happen to be treated the same way in our current requirements,
> but which may vary later and shouldn't be treated as equivalent."

This was refreshing to read.
As a beginner, I often spend time trying to combine and de-duplicate code only to separate it again later.
This always created the feeling like I was doing something wrong.
This small statement made me realize that I was taking DRY too literally and not applying "context" or thinking about changes.

## Rule of Three

_Rule of Three_[^2] is a rule of thumb that states only after you have used the same code three (3) times should you move it into a function for maintainability.

## References

[^1]: [Software Mistakes and Tradeoffs](https://www.manning.com/books/software-mistakes-and-tradeoffs), by Jon Skeet and Tomasz Lelek
[^2]: [Rule of Three](https://en.wikipedia.org/wiki/Rule_of_three_(computer_programming)) Wikipedia article
