---
title: getOwnPropertyNames
todo_broken_links:
  note: 'During import MediaWiki could not find the following links, please fix and adjust this list.'
  links:
    - concepts/programming/javascript/objects/js/objects/Object/keys
    - concepts/programming/javascript/objects/js/statements/for...in
uri: concepts/programming/javascript/objects/js/objects/Object/getOwnPropertyNames

---
This is a method of [Object](/javascript/objects) which was implemented in ECMAScript 5th Edition.

## Overview

This method returns an [Array](/concepts/programming/javascript/core_objects) of the string names of all properties ( *both enumerable and non-enumerable* ) of a given Object. This does not include the properties in the prototype chain.

Should the given object not be of type *Object*, a TypeError exception is thrown. If the given object is an instance of *String* ( having been created via the String's constructor, which is thus of type *Object*, ), the properties that will be processed will correspond to the character positions within the object's PrimitiveValue string.

To obtain only the enumerable properties of an Object, use [Object.keys](/w/index.php?title=concepts/programming/javascript/objects/js/objects/Object/keys&action=edit&redlink=1), should all properties, both enumerable and non-enumerable, of the object and it's prototype chain be required, use a [for...in loop](/w/index.php?title=concepts/programming/javascript/objects/js/statements/for...in&action=edit&redlink=1).

## Syntax

Object.getOwnPropertyNames( *objectToInspect* )

*where "objectToInspect" is an Object whose properties are required*

### Example

``` js
// basic example
var objectToInspect = {
      foo: 'Hello World!',
      bar: 'Welcome To',
      baz: 'WebPlatform Docs'
    };

console.log( Object.getOwnPropertyNames( objectToInspect ) );
// this will log [ "foo" , "bar" , "baz" ]

/*
  A slightly more complex example with non-enumerable properties.
  In this example, we will also show the difference between Object.getOwnPropertyNames() and Object.keys().
  Also note, by default, Object.create treats properties as non-enumerable unless otherwise stated.
  As with baz in the below example.
*/

var objectToInspect = Object.create( Object.prototype , {
      foo: {
          enumerable : true ,
          value : 'Hello World!'
      } ,
      bar : {
          enumerable : false ,
          value : 'Welcome To'
      } ,
      baz : {
          value : 'WebPlatform Docs'
      }
    });

console.log( Object.getOwnPropertyNames( objectToInspect ) );
/*
  this will log [ "foo" , "bar" , "baz" ]
  where as Object.keys will only log "foo"
*/

console.log( Object.keys( objectToInspect ) );
// this will log [ "foo" ] due to "bar" and "baz" being non-enumerable.

// another example, dealing with the prototype chain

function WebPlatform( section ) {

    // non prototype property
    this.section = section;

}

// prototype method
WebPlatform.prototype.methodToInherit = function () {

};

var wpDocs = new WebPlatform( 'Documents' );

wpDocs.ownMethod = function () {

};

console.log( Object.getOwnPropertyNames( objectToInspect ) );
/*
    this will log [ "section" , "ownMethod" ] as methodToInherit is not a direct property of wpDocs
    but instead is part of it's prototype chain ( inherited from WebPlatform )
*/
```

## Extract From Specification

>     15.2.3.4 Object.getOwnPropertyNames ( O )
>         When the getOwnPropertyNames function is called, the following steps are taken:
>             1. If Type(O) is not Object throw a TypeError exception.
>             2. Let array be the result of creating a new object as if by the expression new Array ()
>                where Array is the standard built-in constructor with that name.
>             3. Let n be 0.
>             4. For each named own property P of O
>                 a. Let name be the String value that is the name of P.
>                 b. Call the [[DefineOwnProperty]] internal method of array with arguments ToString(n),
>                    the PropertyDescriptor {[[Value]]: name, [[Writable]]: true, [[Enumerable]]: true,
>                    [[Configurable]]: true}, and false.
>                 c. Increment n by 1.
>             5. Return array.
>
>     NOTE If O is a String instance, the set of own properties processed in step 4 includes the implicit
>     properties defined in 15.5.5.2 that correspond to character positions within the
>     object‘s [[PrimitiveValue]] String.

## External resources

-   [ECMAScript Language Specification 5.1 Edition](http://es5.github.com/#x15.2.3.4)
-   [ES5 Compatibility Table](http://kangax.github.com/es5-compat-table/)
