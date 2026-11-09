# Type Narrowing in TypeScript

## Introduction

Type Narrowing is an important feature of TypeScript that helps developers work safely with different types of values. It reduces a variable's possible types by checking its actual value or structure. This makes code easier to understand and helps prevent type-related errors.

## Detailed Explanation

TypeScript provides several ways to narrow types. Three common techniques are `typeof`, `instanceof`, and the `in` operator.

The `typeof` operator checks primitive types such as strings, numbers, and booleans.

For example:

```ts
function printValue(value: string | number): void {
  if (typeof value === "string") {
    console.log(value.toUpperCase());
  } else {
    console.log(value.toFixed(2));
  }
}
```

Here, TypeScript understands whether the value is a string or a number before performing an operation.

The `instanceof` operator checks whether an object belongs to a particular class. For example, `value instanceof Date` checks whether a value is a Date object.

The `in` operator checks whether a property exists inside an object. For example, `"email" in user` checks whether the user object contains an email property.

These techniques are useful when working with union types and objects that have different structures. They help developers choose the correct operation based on the actual type of a value.

## Conclusion

Type Narrowing makes TypeScript code safer and easier to understand. It helps developers handle different types correctly and prevents many type-related errors during development.