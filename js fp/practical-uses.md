Functional Programming can seem a bit cryptic at first glance. Here are some of my aha moments, where the theory becomes practical:

Semigroup
All about combining stuff. Let's take something very common, arithmetic, as an example:

```javascript
// addition
1 + 1
// could be seen calling a method on Integer that takes another Integer
1.add(1)

// multiplication
2 * 2
// same idea:
2.multiplyBy(2)

// So what?
// Imagine a different type to Integer:
class Project {
  name,        //string
  lastUpdated, //date
  contributors //[string]
}

// and you have several instances of the same project from differen
```

Monoid
Basically a semigroup that you can `reduce`. 

```javascript
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbNDQxNjM0MTg3XX0=
-->