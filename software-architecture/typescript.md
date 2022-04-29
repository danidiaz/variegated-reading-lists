[Creating Types from Types](https://www.typescriptlang.org/docs/handbook/2/types-from-types.html)

[Conditional Types](https://www.typescriptlang.org/docs/handbook/2/conditional-types.html)

> Typically, distributivity is the desired behavior. To avoid that behavior, you can surround each side of the extends keyword with square brackets.

[Mapped Types](https://www.typescriptlang.org/docs/handbook/2/mapped-types.html). [TypeScript Records and Mapped Types](https://www.wwt.com/article/typescript-records-and-mapped-types)

    type OnlyBoolsAndHorses = {
      [key: string]: boolean | Horse;
    };
 
const conforms: OnlyBoolsAndHorses = {
  del: true,
  rodney: false,
};

> You can filter out keys by producing never via a conditional type

    // Remove the 'kind' property
    type RemoveKindField<Type> = {
        [Property in keyof Type as Exclude<Property, "kind">]: Type[Property]
    };

[Utility Types](https://www.typescriptlang.org/docs/handbook/utility-types.html)

[Indexed Access Types](https://www.typescriptlang.org/docs/handbook/2/indexed-access-types.html)

[Understanding infer in TypeScript](https://blog.logrocket.com/understanding-infer-typescript/)

[typescript - What does 'declare' do in 'export declare class Actions'?](https://stackoverflow.com/questions/35019987/what-does-declare-do-in-export-declare-class-actions)

[Module Federation for Enterprise (Part 2)](https://dev.to/waldronmatt/module-federation-for-enterprise-part-2-men)

[assigning local variables to default generic slots](https://twitter.com/mpocock1/status/1516752789564764160)

[TypeScript tips and Tricks with Matt](https://www.youtube.com/watch?v=hBk4nV7q6-w)

