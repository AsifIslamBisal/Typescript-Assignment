# What is Type Narrowing in TypeScript?

## Introduction

Type Narrowing is an important feature in TypeScript that helps developers work safely with values that can have multiple types. It allows TypeScript to understand the specific type of a variable inside a conditional block.

## Detailed Explanation

The typeof operator checks the primitive type of a value.

```ts
function printValue(value: string | number): void {
    if (typeof value === "string") {
        console.log(value.toUpperCase());
    } else {
        console.log(value.toFixed(2));
    }
}
```


The instanceof operator checks whether an object belongs to a particular class.


class Dog {
    bark(): void {
        console.log("Woof!");
    }
}

function makeSound(animal: Dog | Date): void {
    if (animal instanceof Dog) {
        animal.bark();
    }
}


The in operator checks whether a property exists inside an object.

```ts
type Student = { name: string };
type Teacher = { subject: string };

function describe(person: Student | Teacher): void {
    if ("name" in person) {
        console.log(person.name);
    } else {
        console.log(person.subject);
    }
}
```

These operators help TypeScript identify the correct type before accessing specific properties or methods. This reduces type errors and makes code safer.

## Conclusion

Type Narrowing makes TypeScript development more reliable. Using typeof, instanceof, and in allows developers to handle union types safely and write clean, maintainable code.