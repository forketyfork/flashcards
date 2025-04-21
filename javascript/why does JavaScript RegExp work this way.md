START
Basic
Front: Why does JavaScript RegExp work this way?
```javascript
console.log(new RegExp({}).test('mom'))  
> true
console.log(new RegExp({}).test('dad'))
> false
```
Back: 
`RegExp` constructor takes a string, so the object `{}` is being converted to a string here. The string would be `[object Object]` which is a valid regular expression matching any symbol in the square brackets. The word `mom` has a letter `o`, therefore it matches. The word `dad` doesn't have any letters from this list, therefore it doesn't match.
<!--ID: 1745138723642-->
END
