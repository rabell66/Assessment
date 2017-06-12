## Scope, hoisting and compartmentalization

### Answer the following:
In you own words, explain the concepts of scope, hoisting, compartmentalization.

Scopes are global or local. A variable defined in global is available to everything, a locally defined 
variable is only available within its' own function.

hoisting is what javascript does to variables and functions so that it can set aside memory for them to use later
 It does this by pulling them to the top of the program and then executes the program in a top to bottom style.

compartmentalization - its intentionally limiting the availability of a variable so as not to affect the global scope

### Provide examples for all three, below:

#### Scope:
 var x = 15
    function(){
        var x = 5
        console.log(x)  would equal 5
    }
  console.log(x) = 15

#### Hoisting:
   
var a = 6

x = a + b

var b = 5
      x = 11 even though b was declared after the calculation because JavaScript hoisted the variable to the top first

#### Compartmentalization:
(function() {
  "use strict";
  var multiply = 2 * 8;

  function duplicate() {
    var multiply = 2 * 10;
  };

  duplicate();

  console.log( "multiply", multiply );
  
})();