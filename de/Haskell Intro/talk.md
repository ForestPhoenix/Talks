# Introduction

## Overview
> TODO: translate to german

- Statically typed
    - higher order types (kinds)
    - type inference
- purely functional
- explicit effects
- lazy

## History

- Originated from Academics in 1990
- First standard in 1998
- Became more popular in industry recently
- more popular that F# (both redmonk & TIOBE)

# Defining values & functions

## Values

defining the type:

```haskell
zero :: Int
```

- values and parameters are lowercase
- types are uppercase

defining the value:

```haskell
zero = 0
```

C# equivalent:

```CSharp
public const int zero = 0;
```
or
```CSharp
public static int zero() { return 0; }
```

## functions

Both in Haskell and mathematics a function maps one input to one output.

It does not do anything else, like printing stuff, reading the current time, etc...

In Haskell all functions are based on lambda expressions.

a function that adds one to an integer:

```haskell
-- function from Int to Int
plusOne :: Int -> Int
-- taking a parameter n and adding 1:
plusOne n = n + 1
-- is equivalent writing with a lambda expression instead:
plusOne = \n -> n + 1
```

## functions with multiple parameters

a function that adds two integers:

```haskell
-- takes an Int and returns a function from Int to Int
plus :: Int -> Int -> Int
-- or, with explicit parentheses
plus :: Int -> (Int -> Int)

plus x y = x + y
plus = \x -> (\y -> x + y)
```

One possible C# equivalent for plus:

```CSharp
public static Func<int, int> plus(int x)
{
    return y => x + y;
}
```
