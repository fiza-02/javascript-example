https://2048daily.com/

Description
The classList property returns the CSS classnames of an element.

The classList property returns a DOMTokenList.

Using Object-oriented Class Syntax
The use of object-oriented class syntax can also be used to create private variables. JavaScript's class keyword enables us to define classes, which serve as templates for objects. A class can define a variable with the # symbol before the variable name to generate private variables; this is an experimental feature that indicates a private variable. It is not recommended to utilise this feature in production code as it is not currently widely supported.

Example
```
<html>
<body>
   <p id="output"></p>
   <script>
      class MyClass {
         #privateVariable = "This is a private variable";
         getValue() {
            return this.#privateVariable;
         }
         setValue(value) {
            this.#privateVariable = value;
         }
      }
      let obj = new MyClass();
      document.getElementById("output").innerHTML = obj.getValue(); // "This is a private variable"
      obj.setValue("New value");
      document.getElementById("output").innerHTML = obj.getValue(); // "New value"
   </script>
</body>
</html>
```
In this example, a class called MyClass has been constructed using the private variables #privateVariable, getValue, and setValue. A reference error would occur if a method outside of the class attempted to access a private variable that can only be accessible by methods inside the class.