# Elementary Language Specs

By Trip Ottinger and Tom Wilson

A declarative functional language for an aspiring developer!

> DISCLAIMER: If you are a professional developer you'll probably hate this language. This language is for beginners and those new to functional concepts.

Elementary is a Declarative Programming Language where everything is a function. There are no operators or special constructs. Everything is a function. Traditional languages stress the importance of creating the correct syntax. Elementary uses a very common declarative syntax that has been proven to be very descriptive, expressive and compositional.

## Invoking a Function

Elementary is very similar to HTML or XML.  Invoking a function is simply a matter of declaring the function name, and providing argument/property/attribute/parameter values to the function. 

```xml
<[Function Name] argument1=[value] argument2=[value]>
  data
</[Function Name]>
```

Or

```xml
<[Function Name] />
```
---

### Defining a function?

Use the `Function` component to define a function with a name and arguments.

In this example we create a function called `Hello`.

``` xml
<function name=”hello” arg1 arg2>
  <js>console.log(arg1 + ' ' + arg2)</js>
</function>
```

Here is how we would invoke the function:

``` xml
<hello arg1=”Big” arg2="World" />
```

## Why create another language?

When first encountering a programming language, a student has to overcome many barriers including learning strange syntax, typing the correct symbols on the keyboard, and understanding how to start and close functions. For beginners, there are simply too many options and too many deviations.

## Why not a visual language like blockly? 

Blockly is cool but its inheritly visual nature results is very large and cumbersome patterns.  Its code does not fit well within modules and file systems. Elementary's declarative `HTML` like syntax should allow for flexibility and a cognitive visual expressive style.  

## What about XSLT?

Its great for transforming data but imperitive rather than functional.  Elementry is all about composability, closures, and higher order functions.

``` xml
<function name=”add” a data>
  <js>a + data</js>
</function>

<log>
  <add a="1" />
  <add a="3" />
  <js>4</js>
</log>
```

By default composition is built in the language, since every function must return a result it becomes the data argument for the function above it. In the above example, 4 is added to 3 then added to 1 and the result is logged.
