# Type Alias vs Interface in TypeScript

## Introduction

TypeScript provides two useful ways to define the structure of data: Type Aliases and Interfaces. Both help developers write safer and more organized code. However, they have some important differences.

## Detailed Explanation

A Type Alias uses the `type` keyword to create a custom type. It can define primitive types, union types, intersection types, objects, and tuples.

```ts
type User = {
    name: string;
    age: number;
};

type Status = "active" | "inactive";
```

An Interface uses the `interface` keyword to describe the structure of an object. It is commonly used for objects and class contracts.

```ts
interface Student {
    name: string;
    age: number;
}
```

One important difference is that Interfaces support declaration merging. This means multiple declarations with the same interface name can be combined.

```ts
interface User {
    name: string;
}

interface User {
    email: string;
}
```

Now, User contains both name and email properties. Type Aliases do not support this behavior.

Type Aliases are more flexible when working with unions, intersections, and primitive types. Interfaces are often a good choice for object structures and class implementations.

## Conclusion

Both Type Aliases and Interfaces are useful in TypeScript. Choose Interfaces for extendable object structures and Type Aliases for unions, primitives, and more complex type combinations. The best choice depends on the requirements of the project.