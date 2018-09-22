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
class Page {
  name,        //string
  lastUpdated, //date
  contributors //[string]
}

// and we have a record of people editing the page on their own devices
const edits = [
  Page('FP', '2018-01-01', ['Sue']),
  Page('FP', '2018-02-02', ['Sue', 'Bob']),
  Page('FP', '2018-02-02', [`Sue`, `Sam`])
]

// we could loop through it to merge the information...
let page = new Page()
for (let i = 0; i < edits.length; i++){
  page.name = edits[i].name
  page.lastUpdated = Date.latest(page.date, edits[0].date)
  page.contributors = [... new Set(
    ... page.contributors,
    ... edits[0].contributors
  )]
}

// but that code isn't readily reusable,
// and there's state in 

// you can make Page a Semigroup by adding a merge method:
class Page {
  ...
  merge(otherPage) {
    return new Page(
      otherPage.name,
      Date.latest(this.date, otherPage.date),
      [... new Set(
        ...this.contributors,
        ...otherPage.contributors
      )]
    )
  }
}
```

Monoid
Basically a semigroup that you can `reduce`. 

```javascript
```
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTE5MzYyNzAyNjcsLTQ1NDUwODYzMl19
-->