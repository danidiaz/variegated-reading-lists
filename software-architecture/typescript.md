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

[Typed useState with TypeScript](https://www.carlrippon.com/typed-usestate-with-typescript/)

[React Children with TypeScript](https://www.carlrippon.com/react-children-with-typescript/). [TypeScript and React: Components](https://fettblog.eu/typescript-react/components/). [Using the React children prop with TypeScript](https://blog.logrocket.com/using-react-children-prop-typescript/). [How to write a React Component in TypeScript](https://kentcdodds.com/blog/how-to-write-a-react-component-in-typescript). [Why You Should Probably Think Twice About Using React.FC](https://spin.atomicobject.com/2022/01/04/think-twice-react-fc/). [Usage of `React.FC` from my experience](https://dev.to/xenoxdev/usage-of-reactfc-from-my-experience-22n7). [Should you use React.FC for typing React Components](https://medium.com/@harrymt/should-you-use-react-fc-for-typing-react-components-62cde9ba67c). [TypeScript + React: Why I don't use React.FC](https://fettblog.eu/typescript-react-why-i-dont-use-react-fc/). [Remove React.FC from Typescript template](https://github.com/facebook/create-react-app/pull/8177). [Why you probably shouldn’t use React.FC to type your React components](https://blog.raccoons.be/react-fc-opinion).

[Use JSDoc: Block and inline tags](https://jsdoc.app/about-block-inline-tags.html). [markdown plugin](https://jsdoc.app/plugins-markdown.html). [Render Markdown of JSDoc (2016)](https://github.com/microsoft/vscode/issues/17414). [link](https://jsdoc.app/tags-inline-link.html). [see](https://jsdoc.app/tags-see.html). [JSDoc Reference for TS](https://www.typescriptlang.org/docs/handbook/jsdoc-supported-types.html).

[Why is the infer keyword needed in Typescript?](https://stackoverflow.com/questions/60067100/why-is-the-infer-keyword-needed-in-typescript)

[homomorphic mapped types](https://github.com/Microsoft/TypeScript/pull/12563)

[More on Functions](https://www.typescriptlang.org/docs/handbook/2/functions.html)

[Type-safely parsing JSON to a TypeScript Interface](https://dev.to/codeprototype/safely-parsing-json-to-a-typescript-interface-3lkj)

[const assertions are the killer new TypeScript feature](https://blog.logrocket.com/const-assertions-are-the-killer-new-typescript-feature-b73451f35802/)

[Object literal may only specify known properties](https://stackoverflow.com/questions/31816061/why-am-i-getting-an-error-object-literal-may-only-specify-known-properties)

[Type Compatibility](https://www.typescriptlang.org/docs/handbook/type-compatibility.html)

[complex types](https://twitter.com/tesseralis/status/1530346544137789443)

[Advanced TypeScript: How we made our router typesafe](https://twitter.com/zoontek/status/1531190031372673024?t=sAEYxNDdseHXVgChM_1UpQ&s=03).

[Advanced TypeScript course](https://www.youtube.com/playlist?list=PLIvujZeVDLMx040-j1W4WFs1BxuTGdI_b).





