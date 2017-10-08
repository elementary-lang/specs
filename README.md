# Elementary Language Specs

By Trip Ottinger and Tom Wilson

A declarative functional language for an aspiring developer!

DISCLAIMER: If you are a professional developer you will most likely hate this language, and that is ok, it is not for you, but it should be very easy to contribute to in your compile to js language of choice. This language is for people interested in software development.

Elementary is a Declarative Programming Language, where everything is a function, there are no operators or special constructs, everything is a function. Instead of traditional languages where there are all kinds of choices with syntax, Elementary uses a very common declarative syntax that has been proven to be very descriptive and expressive and compositional.

XML or extensible markup language.

How do I invoke a function?

<[Function Name] argument1=[value] argument2=[value]>
  data
</[Function Name]>

Or

<[Function Name] />

---

How do I define a function?

Use the Function component to define a function with a name and arguments

In this example we create a function called Hello

``` xml
<function name=”hello” arg1 arg2>
  <js>console.log(arg1 + ' ' + arg2)</js>
</function>
```

Here is how we would invoke the function:

``` xml
<hello arg1=”Big” arg2="World" />
```
---

Why create another language?

While teaching programming, one of the largest barriers is the syntax and frankly figuring out how to type on the keyboard and understand how to start and close functions. The current syntax serves developers you are over this bridge very well, but does not serve beginners, there is simply too many options and too many deviations, it confuses the beginner.

Why not a visual language like blockly? I think it is too visual and results is very large and cumbersome patterns, also it does not fit well with modules and file systems. Using a declarative `HTML` like syntax should allow for a lot more flexibility and has been proven to create a cognitive visual expressive style that we has humans are able to relate to when seen consistently.  

What about XSLT? I think xslt is great for transforming data, but I believe it dropped down to imperative code to do logic. We want elementry to be a language about composability, support closures and higher order functions.

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
