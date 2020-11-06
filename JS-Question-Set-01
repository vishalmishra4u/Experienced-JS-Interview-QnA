1. What is lexical scope?

Answer :
    lexical scope is scope that is defined at lexing(Compile time, Look to question#11 for more) time.
    In other words, lexical scope is based on where variables and blocks of scope are authored,
    by you, at write time, and thus is (mostly) set in stone by the time the lexer processes your code.


2. What is a closure?

Answer :
    When a function is able to remember and access its lexical scope even when that function is executing outside its lexical scope.

    lets understand it by this example below :

    function foo() {
	     var a = 2;

      function bar() {
    		console.log( a );
    	}

    	return bar;
    }

    var baz = foo();

    baz(); // 2

    On executing baz(), it returns output 2 because bar() still has a refernce to the scope in
    which it was defined, and that refernce is closed closure.

    The function is being invoked well outside of its author-time lexical scope.
    Closure lets the function continue to access the lexical scope it was defined in at author-time.

3. What are apply, call, bind?

Answer :
    Apply : The apply() method calls a function with a given this value,
    and arguments provided as an array (or an array-like object).

      Example :
      var numbers = [5, 6, 2, 3, 7];

      var max = Math.max.apply(null, numbers);

      console.log(max);
      // expected output: 7

      var min = Math.min.apply(null, numbers);

      console.log(min);
      // expected output: 2


    Call : The call() method calls a function with a given this value and arguments provided individually.

      Example :
      function Product(name, price) {
        this.name = name;
        this.price = price;
      }

      function Food(name, price) {
        Product.call(this, name, price);
        this.category = 'food';
      }

      console.log(new Food('cheese', 5).name);
      // expected output: "cheese"


    Bind : The bind() method creates a new function that,
    when called, has its this keyword set to the provided value,
    with a given sequence of arguments preceding any provided when the new function is called.

    this.x = 9;    // this refers to global "window" object here in the browser
    var module = {
      x: 81,
      getX: function() { return this.x; }
    };

    module.getX(); // 81

    var retrieveX = module.getX;
    retrieveX();
    // returns 9 - The function gets invoked at the global scope

    // Create a new function with 'this' bound to module
    // New programmers might confuse the
    // global var x with module's property x
    var boundGetX = retrieveX.bind(module);
    boundGetX(); // 81


4. Name some array methods.

Answer :
    Array.forEach(), Array.push(), Array.pop(), Array.shift(), Array.unshift(), Array.indexOf(),
    Array.slice(), Array.map(), Array.split() etc

5. What are the differences between let, var and const?

```
var declarations are globally scoped or function scoped while let and const are block scoped.

var variables can be updated and re-declared within its scope; let variables can be updated but not re-declared; 
const variables can neither be updated nor re-declared.

They are all hoisted to the top of their scope. But while var variables are initialized with undefined, let and const variables are not initialized.

While var and let can be declared without being initialized, const must be initialized during declaration.
```


6. What is the output of the following code?

  function a(){
    var a = 10;
    console.log(a);

    if(true){
      var a = 20;
      console.log(a);
    }

    console.log(a);
  }

Answer :
10
20
20

Because we are redeclaring the variable a and assigning it value 20;

7. What is the output of the following code?

  function a(){
    let a = 10;
    console.log(a);

    if(true){
      let a = 20;
      console.log(a);
    }

    console.log(a);
  }

Answer :
10
20
10

8. How do you delete the last element of an array? Delete the last element of this array :

  Arr : ['a','b','c','d','e']

  Arr.pop(); // This will return 'e' and resulting array will be ['a','b','c','d']

9. How to loop over elements of objects.

  e.g :
  obj = {
    rain : {"sun" : "5 inch","mon":"3 inch"},
    snow : {"sun" : "10 inch","mon":"8 inch"}
  };

Answer : 

for (let day in obj.rain) {
    if (obj.hasOwnProperty('rain')) {
        // do stuff
    }
}


10. What is a spread operator. (...)

Answer : Spread syntax allows an iterable such as an array expression or string to be expanded
in places where zero or more arguments (for function calls) or elements (for array literals) are expected.

  Example :
    function sum(x, y, z) {
      return x + y + z;
    }

    const numbers = [1, 2, 3];

    console.log(sum(...numbers));
    // expected output: 6

    console.log(sum.apply(null, numbers));

11. Is JS compiled language or interpreted language?

Answer : JS is a interpreted language but its also not completely interpreted.
Things like hoisting take place in js compile time.
