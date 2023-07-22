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

[Build an NPM Package in TypeScript from the Ground Up](https://spin.atomicobject.com/2022/06/21/npm-package-typescript/)

[Fixing TypeScript's Blindspot: Runtime Typechecking](https://www.youtube.com/watch?v=rY_XqfSHock)

[adding optional properties](https://twitter.com/housecor/status/1580600449367183360)

[const modifiers for type parameters](https://twitter.com/AndaristRake/status/1602645915474477056). [more](https://twitter.com/AndaristRake/status/1602701606721814528).

[loops with recursive types](https://twitter.com/GabrielVergnaud/status/1602700630182739968)

[ts-pattern](https://twitter.com/GabrielVergnaud/status/1606290608934395906). [version 3.0](https://dev.to/gvergnaud/bringing-pattern-matching-to-typescript-introducing-ts-pattern-v3-0-o1k)

[Typescript improvements](https://news.ycombinator.com/item?id=34132866)

[Using the React children prop with TypeScript](https://blog.logrocket.com/using-react-children-prop-with-typescript/)

[Self-Type-Checking Types](https://twitter.com/devanshj__/status/1610423724708343808)

[type-safe React Query](https://tkdodo.eu/blog/type-safe-react-query)

[Intl.ListFormat](https://www.youtube.com/watch?v=dpyHNj1l0wg)

[You might be using `fetch` wrong](https://twitter.com/Steve8708/status/1611437686958739456)

[Error.prototype.cause](https://twitter.com/Steve8708/status/1611757223008665600)

[when to use zod](https://twitter.com/mattpocockuk/status/1612397810183274497)

[Typescript satisfies in Haskell](https://www.reddit.com/r/haskell/comments/105hvwc/typescript_satisfies_in_haskell/)

[Better Configuration in TypeScript with the `satisfies` Operator](https://www.builder.io/blog/satisfies-operator)

[setTimeout(resolve, ms, value);](https://twitter.com/WebReflection/status/1616835902893969409)

[Deep Cloning Objects in JavaScript, the Modern Way](https://dev.to/builderio/deep-cloning-objects-in-javascript-the-modern-way-17kf)

[type challenges](https://twitter.com/mattpocockuk/status/1617891002563588099)

[you should specify return types](https://twitter.com/jimmykoppel/status/1623159666078253056). [Modules Matter Most](https://existentialtype.wordpress.com/2011/04/16/modules-matter-most/). [The Design of Software is A Thing Apart](https://www.pathsensitive.com/2018/01/the-design-of-software-is-thing-apart.html).

> There is and should be a many-many relationship between programs and their interfaces.  When you choose a return type, you are not just communicating information, but also intentionally withholding information.

> the information of a program’s design is largely not present in its code1. I don’t just mean that you have to really read the code carefully to understand the design; I mean that there are many designs that correspond to the exact same code, and so recovering all the design information is actually impossible.

> One nice thing about understanding the design/specification level of code is that it gives us very clean definitions of formerly-fuzzy concepts like “this code knows about that code.” For now, stick with your intuition as you answer this question:

[Better dev environments with npm workspaces](https://oliverjam.es/articles/npm-workspaces). [Npm workspaces using TypeScript](https://pgarciacamou.medium.com/workspaces-mvp-with-npm-using-typescript-37e391e26c93). [How to use npm workspace](https://stackoverflow.com/questions/73286125/how-to-use-npm-workspace). [official docs](https://docs.npmjs.com/cli/v9/using-npm/workspaces?v=true)

>  Most npm commands can now have workspace-related options added to make them run against just one (or all) of your workspaces. To run a command against a single workspace you can append --workspace=client. To run a command against all workspaces you can append --workspaces (note the s).

> All the following commands are run from the root directory. No cding around required!

[interview with the creator of TypeScript](https://twitter.com/TimSweeneyEpic/status/1624556394245419011)

[branded types](https://twitter.com/mattpocockuk/status/1625173884885401600)

[megamorphic](https://twitter.com/mhevery/status/1625568637976453121)

[tweaking Promises with unknown](https://twitter.com/mattpocockuk/status/1627296901329477632)

[modernizing the TypeScript codebase](https://twitter.com/typescript/status/1633946375422644225)

[JavaScript and TypeScript features of the last 3 years](https://news.ycombinator.com/item?id=35079971)

[Full-Stack TypeScript with tRPC and React](https://news.ycombinator.com/item?id=35150100)

[TypeScript 5.0](https://devblogs.microsoft.com/typescript/announcing-typescript-5-0/)

[when creating custom query hooks, don't try to support every single option that `useQuery` accepts.](https://twitter.com/Julien_Delort/status/1636740585473077250)

[resolvePackageJsonExports](https://twitter.com/ixahmedxii/status/1636708896365588480)

[Fully Typed Web Apps](https://www.epicweb.dev/fully-typed-web-apps)

[exclude members of a discriminated union by shape](https://twitter.com/sebastienlorber/status/1644250044042715137)

[useful libraries](https://twitter.com/housecor/status/1644699226138456069)

[hiding query keys](https://twitter.com/mattia_asti/status/1645450734949761026)

[how to name your types](https://www.totaltypescript.com/tips/how-to-name-your-types). [tweet](https://twitter.com/mattpocockuk/status/1646108727467024385). [giving names](https://twitter.com/mattpocockuk/status/1646087589114396673). 

[advantages vs. Haskell](https://www.reddit.com/r/haskell/comments/134c1kt/comment/jiebdc0/)

[sql tagged template](https://twitter.com/cramforce/status/1654569294620135424)

[Avoid centralizing TypeScript types](https://twitter.com/housecor/status/1655188355569659908)

[Unleashing the Power of Conditional Types in TypeScript](https://www.susanpotter.net/software/unleashing-the-power-of-conditional-types-in-typescript/)

[Given an object, grab the keys where the values match a certain type](https://twitter.com/mattpocockuk/status/1672151954212937728). [loose autocomplete trick](https://twitter.com/mattpocockuk/status/1671908303918473217). [type argument placeholders](https://twitter.com/mattpocockuk/status/1671892728282759172). 

[as const](https://twitter.com/mattpocockuk/status/1671794965393842176)

[antipatterns](https://twitter.com/TkDodo/status/1672313484250325002)

[I see so many bugs caused by devs trusting a value provided by the network](https://twitter.com/mattphillipsio/status/1672516898670403584)

[Iterating over a known set of object keys in TypeScript](https://twitter.com/mattpocockuk/status/1681267079977000961). [more](https://twitter.com/TkDodo/status/1681699050653925379).

[drizzle ORM](https://twitter.com/kentcdodds/status/1682484161100259328)



