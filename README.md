# IcePy

A programming language that has strict Icelandic grammar rules built in.

## Concepts

There are a set of known variable names that can be used. Each have forms in
nominative, accusative, dative, genitive.

Each argument to a function must define the case expected.

Each class has a gender

Core constructs of the language may take different cases too.


## Language constructs

As the name suggests, the language is python-esque. Except that there are mass
translations of things (eg `class` and `def` are no longer available).


### Defining a method or function

To define the function "reikna", you use the keyword "virka"

```
virka reikna():
    pass
```

### Defining a class (tegund)

```
tegund Bátur():

   einstaklingar = []

   virka __frumstilla__(sjalfur):
       pass

```

### Iterating through an iterable

```
hópur = ['Margrét', 'Anna', 'Emma', 'Þór', 'Hrafn', 'Freyr']

fyrir einstaklingur í hóp:
    # Gera eitthvað

```
Note:
 - that using `fyrir einstaklingur í hópur` would raise a syntax error here, on
   account of hópur not being in the correct case.
 - that the days of `for i in x` are behind you now. Even these somewhat
   temporary variable names must be known to the system - so that it can
   determine case when they are used.


### Calling methods with correct case

Note that all variables should be instansiated in nominative form. Once
created they are available to the interpreter in any of the cases and must be
used appropriately.

```
bátur = Bátur()
bátur.

```

### Using numbers

Objects have genders. Numbers used must match those genders (and cases).

For example, if you ask for `lengd(bátur.einstaklingar)`, you will get back a
male integer ( due to the gender of einstaklingar ).

The system, like the natural language, allows you to use this interchangably
with other gender numbers (so you can easily add Male 2 to Female 3), but you
must prove you know what is going on, by casting explicitly from what they
were.

ie:
```
lengd(bátur.einstaklingar).karlkyn + lengd(blómar).hvorugkyn
```
