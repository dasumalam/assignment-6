**Q-1 What is JavaScript?**
**Ans:-**
 * JavaScript is a scripting or programming language.
 * that allows developers to create interactive web pages and mobile apps and web browser receives the JavaScript code in its original text form and runs the script from that

<hr>
**Q-2 What is the use of isNaN function?**
**Ans:-**
  *  isNaN() returns true if a number is Not-a-Number.
* In other words: isNaN() converts the value to a number before testing it.

* **Example :**
```html
<html>
<body>

<h2>The isNaN() Method</h2>
<p id="demo"></p>
<p id="some"></p>

<script>
let text = "Hello";
document.getElementById("demo").innerHTML = isNaN(text);
document.getElementById("some").innerHTML = isNaN(123);
</script>

</body>
</html>
```
<hr>

**Q-3 What is negative Infinity?**
**Ans:-**
Negative Infinity is a value in JavaScript that represents something that is smaller than any number you can think of. It’s like the lowest point on a number line.

* **Key Points:**
* How to Use It:
 You can refer to negative infinity using -Infinity.

* **Always Less:** Negative infinity is always less than any other number:
* **For example**
```javascript
-Infinity < -1000 is true because negative infinity is way lower than -1000.
```
* **Type:** Even though it’s a special value, it’s considered a number in JavaScript:

  * If you check its type, it says “number.”
  
 * **Why It’s Useful:** It can help when you need to find the smallest number in a set or when working with limits in math.

<hr>

**Q-4 Which company developed JavaScript?**
**Ans:**
 * JavaScript was created at Netscape Communications by Brendan Each in 1995. 
 * Netscape and Each designed JavaScript as a scripting language for use with the company's flagship web browser, Netscape Navigator.
<hr>

**Q-5 What are undeclared and undefined variables?**
**Ans:**

* **Undeclared:**
 A variable is undeclared if it has not been declared with a keyword like var, let, or const.
 Accessing an undeclared variable will throw a ReferenceError.
* **Undefined:**
A variable is undefined if it has been declared but has not been assigned a value. undefined is a primitive data type that represents the absence of a value.

<hr>

**Q-6 Write the code for adding new elements dynamically?**
**Ans:**
New elements can be dynamically created in JavaScript with the help of `createElement()` method. 
The attributes of the created element can be set using the `setAttribute()` method.

<hr>

**Q-7 What is the difference between ViewState and SessionState?**
**Ans:**
* **ViewState:**


- **Scope:**  Bound to a specific control on a web page.
- **Persistence:** Preserves values across postbacks within the same page request.
- **Storage:** Stores data in a hidden field within the HTML form.
- **Security:** Susceptible to tampering, as the data is visible in the HTML source.
- **Performance:** Can impact performance if used excessively, as it increases the size of the page.
* **SessionState:**

- **Scope:** Bound to a user's session, which is a collection of related requests from a single user.
- **Persistence:** Preserves values across multiple page requests within a single session.
- **Storage:** Stores data on the server, either in memory (InProc) or in a database (StateServer or SQLServer).
- **Security:** More secure than ViewState, as the data is not exposed in the HTML source.
- **Performance:** Generally has a lower performance overhead compared to ViewState.

<hr>

**Q-8 What is === operator?**
**Ans:**
The === operator in JavaScript is known as the strict equality operator. It checks for equality between two values and also ensures that the values are of the same type.

* **Key Characteristics of ===:**

 * Same Types Required: 
 If you compare different types it will always return `false.`
* Value Comparison:
 If the values and types of both operands are the same, it returns true; otherwise, it returns false.

* **Examples:**
```javascript

console.log(5 === 5);          
console.log(5 === '5');        
console.log(null === undefined);
console.log(true === 1);       
console.log('hello' === 'hello'); 
```
<hr>

**Q-9 How can the style/class of an element be changed?**
**Ans:**
**1. Using the style property:**
Access the element's style property.
Set individual CSS properties directly.

* **Example:**
```JavaScript
let element = document.getElementById('myElement');
element.style.color = 'red';
element.style.fontSize = '20px';
```


* **2. Using the classList property:**

Access the element's classList property.
Use methods like add, remove, and toggle to manage classes.
* **Example:**
```JavaScript
let element = document.getElementById('myElement');
element.classList.add('active');
element.classList.remove('inactive');
element.classList.toggle('hovered');
```
<hr>

**Q-10 How to read and write a file using JavaScript?**
**Ans:**

* **Reading a File**
To read a file, you can use the fs.readFile() method. Here’s how it works:
* **Syntax:**
```javascript
fs.readFile(filePath, encoding, callback);
```

* **Parameters:**
* filePath: The path to the file you want to read.
* encoding: The character encoding (e.g., 'utf8').
* callback: A function that takes two arguments: an error (if any) and the data read from the file.

* **Example:**
```javascript
const fs = require('fs');
fs.readFile('example.txt', 'utf8', (err, data) => {
    if (err) {
        console.error(err);
        return;
    }
    console.log(data);
});
```
* **Writing to a File**
To write data to a file, use the fs.writeFile() method:

* **Syntax:**
```javascript
fs.writeFile(filePath, data, options, callback);
```
* **Parameters:**
* filePath: The path to the file where data will be written.
* data: The content to write.
* options: Optional parameters such as encoding and mode.
* callback: A function that runs after writing is complete.
* **Example:**
```javascript
const fs = require('fs');

fs.writeFile('example.txt', 'Hello, World!', (err) => {
    if (err) {
        console.error(err);
        return;
    }
    console.log('File has been written');
});
```
<hr>

**Q-11 What are all the looping structures in JavaScript?**
**Ans:**

**1. for Loop:**
Executes a block of code a specified number of times.
* Syntax:
```
for (initialization; condition; increment/decrement)
 {
  // Code to be executed
}
```

* **Example:**
```JavaScript
for (let i = 0; i < 5; i++) {
  console.log("Iteration " + i);
}
```


 **2. while Loop:**
Executes a block of code as long as a specified condition is true.

* Syntax:

```JavaScript
while (condition) {
  // Code to be executed
}
```

* **Example:**
```JavaScript
let count = 0;
while (count < 5) {
  console.log("Count: " + count);
  count++;
}
```

**3. do...while Loop:**

Executes a block of code once, then repeats as long as a specified condition is true.
* Syntax:
```JavaScript
do {
  // Code to be executed
} while (condition);
```

* **Example:**
```JavaScript
let i = 0;
do {
  console.log("i: " + i);
  i++;
} while (i < 5);
```

**4. for...in Loop:**

Iterates over the properties of an object.
* Syntax:
```JavaScript
for (let property in object) {
  // Code to be executed
}
```

* **Example:**
```JavaScript
let person = { name: "Alice", age: 30 };
for (let key in person) {
  console.log(key + ": " + person[key]);
}
```

**5. for...of Loop:**

Iterates over the values of an iterable object (like arrays, strings, and Maps).
* Syntax:
```JavaScript
for (let value of iterable) {
  // Code to be executed
}
```

* **Example:**
```JavaScript
let fruits = ["apple", "banana", "orange"];
for (let fruit of fruits) {
  console.log(fruit);
}
```

* **6. forEach() Method:**

Iterates over the elements of an array.
* Syntax:
```JavaScript
array.forEach(callbackFunction);
```
* **Example:**
```JavaScript
let numbers = [1, 2, 3, 4, 5];
numbers.forEach(number => {
  console.log(number * 2);
});
```
<hr>

**Q-12 How can you convert the string of any base to an integer in JavaScript?**
**Ans:**
string : The value of string that needs to be parsed or converted into a number. The function expects the value to be a string if it not a string than it is automatically converted into string using the toString() method.

radix an optional integer between the range of 2 and 36 that represents the root or the base of the numerical system. If nothing is provided by default 10 is used.

`Syntax: parseInt(string, radix)`
```javascript
let input = "100px";
let number = parseInt(inputString, 10);
```
**Q-13 What is the function of the delete operator?**
**Ans:**
*  **Deleting Object Properties**
You can use delete to remove a specific property from an object. If the property exists, it will be removed, and the operation will return true. If the property does not exist or cannot be deleted, it will return false.

```javascript
let obj = { name: 'Alice', age: 25 };
delete obj.age; 
console.log(obj);
```
* **Deleting Array Elements**
While you can use delete on an array, it does not change the length of the array. Instead, it leaves a undefined hole at the index where the element was deleted.

```javascript
let arr = [1, 2, 3];
delete arr[1]; 
console.log(arr); 
```
* **Deleting Variables**
You cannot use delete to remove variables declared with var, let, or const. Attempting to do so will result in a SyntaxError in strict mode, and it will return false in non-strict mode.

```javascript
let x = 10;
delete x; 
```
**Q-14 What are all the types of Pop up boxes available in JavaScript?**
**Ans:**
JavaScript has three kind of popup boxes: Alert box, Confirm box, and Prompt box.

  **1.  Alert Box:**
- Displays a message to the user.
- Has an "OK" button that the user must click to dismiss the box.
* **Example:**
```javascript
 alert("This is an alert box!");
 ```
**2. Confirm Box:**
* Displays a message to the user and asks for confirmation.
* Has two buttons: "OK" and "Cancel."
* Returns true if the user clicks "OK," false if the user clicks "Cancel."
* **Example:**
```javascript
 let result = confirm("Are you sure you want to continue?");
 ```
**3. Prompt Box:**
* Displays a message to the user and prompts them to enter a value.
* Has a text input field and "OK" and "Cancel" buttons.
Returns the value entered by the user if "OK" is clicked, or null if "Cancel" is clicked.
* **Example:**
```javascript
 let name = prompt("What is your name?");
 ```
**Q-15 What is the use of Void (0)?**
**Ans:**

* JavaScript void 0 means returning undefined (void) as a primitive value. 
* You might come across the term “JavaScript:void(0)” while going through HTML documents.
*  It is used to prevent any side effects caused while inserting an expression in a web page

* **Example**
```javascript
<a href="javascript:void(0)" onclick="showPopup();return false;">Show Popup</a>
```
**Q-16 How can a page be forced to load another page in JavaScript?**
**Ans:**

You can force a page to load another page in JavaScript using several methods, depending on your needs. 
Here are a few common techniques:

* **Using `window.location`**
You can change the current page by setting `window.location` to the URL of the page you want to load:

```javascript
window.location.href = 'https://www.youtube.com/watch?app=desktop&v=GP3wtr2HVnk';
```

* **Using `window.open`**
If you want to open a new page in a new tab or window, use `window.open`:

```javascript
window.open('https://www.youtube.com/watch?app=desktop&v=GP3wtr2HVnk', '_blank'); // Opens in a new tab
```

* **Using `location.replace`**
If you want to replace the current page in the history stack (meaning the user won't be able to go back to it), use `location.replace`:

```javascript
window.location.replace('https://www.youtube.com/watch?app=desktop&v=GP3wtr2HVnk');
```

* **Redirecting with Meta Tag (for HTML)**
If you're looking to redirect a page after a set time using HTML, you can use a `<meta>` tag in the `<head>` section:

```html
<meta http-equiv="refresh" content="0;url=https://www.youtube.com/watch?app=desktop&v=GP3wtr2HVnk">
```
* **Redirecting with `setTimeout`**
If you want to delay the redirection, you can use `setTimeout`:

```javascript
setTimeout(() => {
    window.location.href = 'https://www.youtube.com/watch?app=desktop&v=GP3wtr2HVnk';
}, 3000); // Redirects after 3 seconds
```

Choose the method that best fits your scenario!
**Q-17 What are the disadvantages of using innerHTML in JavaScript?**
**Ans:**
* **Security Risks:**
 It can expose your application to Cross-Site Scripting (XSS) attacks if user input is not properly sanitized.
  Malicious scripts can be injected if the input is not handled correctly.

* **Performance Issues:** Updating the entire innerHTML of an element can be less efficient than manipulating the DOM directly. 
This is because it forces the browser to reparse and re-render the entire HTML structure within that element.

* **Loss of Event Listeners:** When you set innerHTML, any existing event listeners on child elements are removed. 
This can lead to unexpected behavior if you rely on those listeners.

* **Complexity with Complex Structures:** Managing complex DOM structures can become cumbersome, as innerHTML treats the content as a string rather than a structured object.
 This can make it harder to manipulate individual elements or attributes.

* **HTML Parsing Errors:** If the HTML string you assign to innerHTML is not well-formed, it can lead to parsing errors or unexpected results.

* **Browser Compatibility:** While most modern browsers support innerHTML, relying on it can sometimes lead to inconsistencies across different browsers, especially with more complex HTML or edge cases.









