# Explanations for defensive coding

## Immutability

The concept that fields and properties cannot change once the object or struct has been created.
This is achieved by marking all fields readonly, all properties get only and using the IReadOnly interfaces for collections and arrays.
The Record type (from C# 9.0 and onwards) is immutable by default.
The price for immutability is extensive copying and added code in the shape of With methods (With methods come for free for Records).

See: https://en.wikipedia.org/wiki/Immutable_object

## Parse, don't validate

The concept that we parse input as soon as we receive it instead of validating same input all over the place.
We also validate the input when parsing so we at all times are sure the content is as it should be.
If we for instance receive a product id in the type of a string, we create a readonly struct that takes the string as input into the constructor,
where we validate the string (string length, alphanumeric, etc.). 
We then pass on the struct instead of the string, thereby having a more strongly typed data object that is already
validated and ready to be used.
The price is more modelling of the domain in the shape of all the extra types we need to create.

## Fail early, fail fast

This is reflected in that we validate all input as soon as we receive it in the constructor or at the start of methods, be that for null reference,
empty strings or invalid status.
We also validate the internal state of objects and fail as soon as an invalid state is discovered.
We then fail immediately if we discover flawed input or an invalid state instead of continuing.
The price is we have to write more code for all the validation steps.

See: https://en.wikipedia.org/wiki/Fail-fast_system

## Composition instead of inheritance

This also goes by "Code towards an interface instead of an implementation" or "HAS a instead of IS a"
The concept is that even though code reuse in the shape of a class hierarchy seems nice, having the same code in a property instead of a base class
allows for way more flexibility and targetted testing.
The price is a lot of methods that just forwards calls to the internal property.

See: https://en.wikipedia.org/wiki/Composition_over_inheritance
