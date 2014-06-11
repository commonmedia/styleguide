# Javascript Code Style

* Use JSHINT - http://www.jshint.com/
http://www.jshint.com/install/
There are multiple Sublime Text plugins that will alert you to errors/redundancies in your code

## Coding Style

* Never leave trailing whitespace.

* Always use triple equals (strict equality) === and not double equals ==
There are very few exceptions for when you should use == and not ===

* Semicolons
ALWAYS USE THEM.  Relying on implicit insertion can cause subtle, hard to debug problems. Don't do it. You're better than that.

GOOD:
```
  (function(window, document, $, undefined){

    var myFunction = function(x, y, z) {
      return x + y + z;
    };

  })(window, document, jQuery, undefined);

``` 

BAD:

```
  (function(window, document, $, undefined){

    var myFunction = function(x, y, z) {
      return x + y + z;
    }

  })(window, document, jQuery, undefined)

``` 

* Array and Object literals
Use Array and Object literals instead of Array and Object constructors.

Example:

How to create an object

GOOD: 

```
  var myObject = {
    propetyOne: 'Value One',
    propetyTwo: 'Value Two'
  };

  var myArray = [1, 2, 3];

```

BAD: 

```
  var myObject = new Object();
  myObject.propertyOne = 'Value One';
  myObject.propertyOne = 'Value Two';

  var myArray = new Array(1, 2, 3);

```

* The LAST property of an object never gets a comma after it
This can cause errors in some browsers

Example:
```
  var myObject = {
    myProperty: 'Value',
    anotherProperty: 'Another Value', // BAD BAD BAD
  };

```

* ALWAYS USE CAMEL CASE
The creators of javascript went with camel case.  For consistancy's sake we need to stick with one convention and being consistant with what the creators decided is a good option.

Example:
``` 
  var myVeryLongVariableIsCamelCase = true; // GOOD
  var this_is_a_Variable = false; // BAD
```