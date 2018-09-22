# JS FP notation
Explaining, in my own words, the Hindley-Milner notation found in Functional Javascript projects such as:

 - http://www.tomharding.me/fantasy-land
 - https://github.com/sanctuary-js/sanctuary
```javascript
fn :: a -> b
// fn is a member of a function 
// that takes a type of a 
// and returns a type of b

fn :: a -> b -> c
// fn is a member of a function 
// that takes a type of a and a type of b, 
// and returns a type of c

fn :: a ~> b -> c
// fn is a method of a type of a 
// that takes a type of b 
// and returns a type of c

fn :: Thing a => a ~> b -> c
// fn is a method of Thing 
// that takes a type of b 
// and returns a type of c

fn :: Thing f => f a ~> f (a -> b) -> f b
// fn is a method of Thing
// Thing contains an a
// 
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTExNDk5OTYwNzMsODM0OTgyMTYzLC0xOD
MzMDMyMjg3XX0=
-->