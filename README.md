[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/GDPVb20V)
# Mystery Function

What does the `mystery()` function in the following piece of code do? Add your
answer to this markdown file.

```javascript
function mystery(a) {
    if(a.length == 1) return a[0];
    var foo = mystery(a.slice(1, a.length))
    if(foo > a[0]) return foo;
    else return a[0];
}
```

ANSWER:
This code will always output the largest integer in the array.
Recursively the code starts segmenting the initial array down into smaller sub-arrays until it reaches the base case.
It then checks the prior value of foo to element 1 in the smaller sub-array.
If the value is greater than the value of foo, that new value becomes foo itself.
This process repeats for the other larger sub-arrays looking for the largest foo value.
In the end the the largest integer will always be outputted.
