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
ANSWER: This code will always output the largest integer in the array. Recursively the code starts segmenting the initial array down into smaller sub-arrays until it reaches the base case. It then checks the prior value of foo to element 1 in the smaller sub-array. If the value is greater than the value of foo, that new value becomes foo itself. This process repeats for the other larger sub-arrays looking for the largest foo value. In the end the the largest integer will always be outputted.
