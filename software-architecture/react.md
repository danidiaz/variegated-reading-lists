[Roadmap to becoming a React developer in 2018](https://github.com/adam-golab/react-developer-roadmap) [hn](https://news.ycombinator.com/item?id=17470496)

[Using Redux actions](https://lobste.rs/s/gnwza3/using_redux_actions_why_how)

[Make your PWA work offline I](https://www.monterail.com/blog/pwa-working-offline)

[How to visually design state in JavaScript](https://medium.freecodecamp.org/how-to-visually-design-state-in-javascript-3a6a1aadab2b)

[Redux or ES6?](https://www.fullstackreact.com/articles/redux-or-es6/)

[Offlinefähige Desktopanwendungen mit Angular und Electron](https://jaxenter.de/offlinefaehige-desktopanwendungen-angular-electron-73438)

[Redux vs. The React Context API](https://daveceddia.com/context-api-vs-redux/)

[The Terrible Performance Cost of CORS Request on the Single-Page Application](https://medium.com/@ankur_anand/the-terrible-performance-cost-of-cors-api-on-the-single-page-application-spa-6fcf71e50147). [hn](https://news.ycombinator.com/item?id=17896973).

[removing jquery from GitHub](https://twitter.com/mislav/status/1022058279000842240). [blog](https://githubengineering.com/removing-jquery-from-github-frontend/).

[Creating a Drag-and-Drop File Uploader with React & TypeScript](https://spin.atomicobject.com/2018/09/13/file-uploader-react-typescript/)

[reactive timed popup](https://spin.atomicobject.com/2018/09/19/reactive-timed-popup/)

[Introducing Hooks](https://reactjs.org/docs/hooks-intro.html). [HN](https://news.ycombinator.com/item?id=18302162). [tweet](https://twitter.com/dan_abramov/status/1056339564250435584).

[React Today and Tomorrow and 90% Cleaner React](https://www.youtube.com/watch?v=dpw9EHDh2bM).

> The React hooks proposal shows how to express several existing concepts that are currently bulky (React component declaration, state, context, lifecycle) using only functions

[React Component Patterns by Michael Chan](https://www.youtube.com/watch?v=YaZg8wg39QQ)

[Vue 3.0](https://news.ycombinator.com/item?id=18474745) Contains info about suing JSX without webpack. [gist](https://gist.github.com/Badestrand/3609e7c3c88ba47bb9682a4746e513db).

> if you are referring to React when mentioning webpack / transliteration, i'd like to mention that you don't need them for React neither. It can be resumed to a simple script tag as well.

> Could you paste the simple script tag that makes React work without transpilation? I always thought you needed Webpack (or an equivalent) to transpile JSX into a vanilla js function the browser can interpret.

> No, I meant simply adding a tag and using react directly, in any context. That's how it was originally designed, btw. It wasn't meant only for SPAs when it was conceived, but as an addon to existing websites.
The other comment gives a perfect example and there are a few tutorials (although I do agree not very mainstream) that teach React without JSX/Webpack/Babel/etc.

> There's also a babel script that you can drop into a script tag and will transpile stuff in the browser for you if you want JSX.
Not recommended for large projects in production (but then I'd be using webpack or similar for large vue projects too), but it works pretty well (and surprisingly fast) for quick experiments.

[React.Component vs React.createClass](https://stackoverflow.com/questions/30668464/react-component-vs-react-createclass).

[React.createClass versus extends React.Component](https://toddmotto.com/react-create-class-versus-component/).

> Two ways to do the same thing. Almost. React traditionally provided the React.createClass method to create component classes, and released a small syntax sugar update to allow for better use with ES6 modules by extends React.Component, which extends the Component class instead of calling createClass.

> For the React changes, we now create a class called “Contacts” and extend from React.Component instead of accessing React.createClass directly, which uses less React boilerplate and more JavaScript. This is an important change to note further changes this syntax swap brings.

[ECMAScript 6 modules: the final syntax](http://2ality.com/2014/09/es6-modules-final.html).

> The default export is actually just a named export with the special name default.

> In current JavaScript module systems, you have to execute the code in order to find out what the imports and exports are. That is the main reason why ECMAScript 6 breaks with those systems: by building the module system into the language, you can syntactically enforce a static module structure. Let’s first examine what that means and then what benefits it brings.

[Making Sense of React Hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889).

[Why mixins are broken](https://reactjs.org/blog/2016/07/13/mixins-considered-harmful.html#why-mixins-are-broken)

> If several components used this mixin to subscribe to a data source, a nice way to avoid repetition is to use a pattern called “higher-order components”. It can sound intimidating so we will take a closer look at how this pattern naturally emerges from the component model.

[Mixins Are Dead. Long Live Composition](https://medium.com/@dan_abramov/mixins-are-dead-long-live-higher-order-components-94a0d2f9e750).

> render props, mixins, hocs...

[5 common practices that you can stop doing in React](https://blog.logrocket.com/5-common-practices-that-you-can-stop-doing-in-react-9e866df5d269).

[How Does setState Know What to Do?](https://overreacted.io/how-does-setstate-know-what-to-do/). [HN](https://news.ycombinator.com/item?id=18639024).

[Why Do React Hooks Rely on Call Order?](https://overreacted.io/why-do-hooks-rely-on-call-order/). [HN](https://news.ycombinator.com/item?id=18669142).

[decluttering a React application](https://lattix.com/blog/2018/12/11/decluttering-react-application). [reddit](https://lattix.com/blog/2018/12/11/decluttering-react-application).

[what is the shadow DOM?](https://www.reddit.com/r/programming/comments/a581wy/what_is_the_shadow_dom/). [reddit](https://www.reddit.com/r/programming/comments/a581wy/what_is_the_shadow_dom/)

[Understanding JavaScript Modules As A TypeScript User](https://www.reddit.com/r/programming/comments/a4rgap/understanding_javascript_modules_as_a_typescript/).

[Ask HN: Go-to web stack today?](https://news.ycombinator.com/item?id=18829557)

[Making SetInterval Declarative with React Hooks](https://news.ycombinator.com/item?id=19073851) [more](https://news.ycombinator.com/item?id=19100257)

[Spring Framework 5 (Boot/Cloud) + React?](https://www.reddit.com/r/java/comments/an9y2x/spring_framework_5_bootcloud_react/).

[new es2018 features](https://css-tricks.com/new-es2018-features-every-javascript-developer-should-know/)

[hooks example](https://twitter.com/dan_abramov/status/1102008543014735873)

[scheduling in react](https://philippspiess.com/scheduling-in-react/)

[useReducer](https://twitter.com/dan_abramov/status/1104069655352823809)

[useEffect](https://twitter.com/dan_abramov/status/1104373579901272064)

[Architecting UIs for Change](https://joreteg.com/blog/architecting-uis-for-change)

[TypeScript for Enterprise Developers](https://www.infoq.com/presentations/typescript-type-system-2018)

[react unpopular opinions](https://twitter.com/dan_abramov/status/1109461037391187968)

[Dilemmas With React Hooks - Part 2: Persistence And Memoization](https://yearn2learn.netlify.com/dilemmas-with-react-hooks-2). [hn](https://news.ycombinator.com/item?id=19573433).

[web components](https://news.ycombinator.com/item?id=19640226)

[biggest lies about react hooks](https://www.reddit.com/r/programming/comments/bcqupq/the_biggest_lies_about_react_hooks/)

[Comparing JVM alternatives to JavaScript](https://renato.athaydes.com/posts/comparing-jvm-alternatives-to-js.html). [hn](https://news.ycombinator.com/item?id=19714924).

[binding actions creators - doesn't make much sense with hooks](https://twitter.com/dan_abramov/status/1123380027230498816)

[Deeply Understanding JavaScript Async and Await with Examples](https://blog.bitsrc.io/understanding-javascript-async-and-await-with-examples-a010b03926ea)

[hooks tip](https://twitter.com/dan_abramov/status/1125223181701263360)

[React articles from Google](https://twitter.com/ChromiumDev/status/1125893811668840448)

[Typescript & React: Manipulating Prop Types](https://medium.com/@rossbulat/typescript-react-manipulating-prop-types-ec13f841a550)

[RxJS: A Better Way to Write Front-end Applications](https://www.infoq.com/presentations/rxjs-front-end). [RxJS behaviour subjects](https://medium.com/@rmcavin/my-favorite-state-management-technique-in-angular-rxjs-behavior-subjects-49f18daa31a7)

[Typescript 3.5](https://devblogs.microsoft.com/typescript/announcing-typescript-3-5/)

[react from vue](https://twitter.com/dan_abramov/status/1137987818486083584)

[pitfalls adopting react hooks](https://twitter.com/kentcdodds/status/1140055079862407168)

[unnecessary rerenders](https://twitter.com/kentcdodds/status/1140257656826761216)

[React testings vs. end-to-end testing](https://twitter.com/Gpx/status/1142719744841306112)

[You Probably Don't Need Derived State](https://reactjs.org/blog/2018/06/07/you-probably-dont-need-derived-state.html)

[The modern PWA worksheet](https://www.youtube.com/watch?v=cybhV88KLfI)

[React and PureScript](https://thomashoneyman.com/articles/replace-react-components-with-purescript/)

[reusable componentes using React](https://buttercms.com/blog/building-reusable-components-using-react)

[adopting typescript at scale](https://www.youtube.com/watch?v=P-J9Eg7hJwE)

[improving your react with typescript ADTs](http://www.javiercasas.com/articles/typescript-adts)

[React + Redux + Typescript](http://www.javiercasas.com/articles/typescript-typeful-state-transitions)

[smells in react apps](https://www.youtube.com/watch?v=xBa0_b-5XDw)

[Fantastic Front-End Performance Tricks](https://www.infoq.com/presentations/front-end-performance-optimization/)

pseudo-elements https://css-tricks.com/a-little-reminder-that-pseudo-elements-are-children-kinda/

[A Simple, Understandable Production Ready Frontend Project Setup](http://marianoguerra.org/posts/a-simple-understandable-production-ready-frontend-project-setup.html)

[Facebook GraphQL interview](https://twitter.com/software_daily/status/1151779902137556992)

[State Management for React Using Context and Hooks](https://www.infoq.com/presentations/react-redux-state-management/)

[algebraic effects](https://twitter.com/dan_abramov/status/1152940032359092225)

[theming with react and sass](https://www.reddit.com/r/programming/comments/cgf743/theming_with_react_and_sass/)

[Programming the Cloud with TypeScript](https://www.infoq.com/presentations/cloud-programming-typescript/)

[People keep asking if Hooks can replace Redux](https://twitter.com/_ericelliott/status/1154036791235629056)

[Using React Hooks to Wrap Connectors to Live Data Sources](https://medium.com/perlin-network/using-react-hooks-to-wrap-connectors-to-live-data-sources-3d97a934a38f)

[Loading States in React Components Using TypeScript’s Discriminated Unions](https://spin.atomicobject.com/2019/07/31/loading-states-react/)

[using typescript like a pro](https://www.reddit.com/r/programming/comments/cm186o/using_typescript_like_a_pro/)

[react interview](https://twitter.com/kentcdodds/status/1159468138926182400)

[testing react with jest and enzyme](https://www.reddit.com/r/programming/comments/csi8x3/testing_react_apps_with_jest_and_enzyme/)

[using Typescript with React](https://news.ycombinator.com/item?id=20765187)

[JavaScript: The Modern Parts](https://news.ycombinator.com/item?id=20785616)

[The metaphysics of Javascript](https://news.ycombinator.com/item?id=20879778). [Deconstructing Web frameworks for a more resilient code base](https://www.youtube.com/watch?v=lApHGnIlx3U)

[react hooks pitfalls](https://www.reddit.com/r/programming/comments/d1k2ds/react_hook_pitfalls_kent_c_dodds_react_rally_2019/)

[Using React Hooks & Context to Avoid Adding Redux Too Early](https://spin.atomicobject.com/2019/09/09/avoid-redux-react-hooks-context/)

[frustrations with React hooks](https://news.ycombinator.com/item?id=20927031)

[Using React Hooks & Context to Avoid Adding Redux Too Early](https://spin.atomicobject.com/2019/09/09/avoid-redux-react-hooks-context/)

[Thinking in React Hooks](https://wattenberger.com/blog/react-hooks)

[Chart.js](https://news.ycombinator.com/item?id=21170288)

[aha moment with react hooks](https://twitter.com/paf31/status/1187484878192836608)

[Building a commentary sidebar in React](https://tuzz.tech/blog/react-commentary-sidebar)

[build your own React](https://news.ycombinator.com/item?id=21536789)

[react unit testing](https://blog.bitsrc.io/complete-guide-on-unit-and-integration-testing-of-react-redux-connected-forms-cd6f8476161)

[React Table is a “headless” UI library](https://news.ycombinator.com/item?id=21630459)

[One of the many problems with this data fetching approach is that the cache is too local](https://twitter.com/dan_abramov/status/1202052703813357574)

[useState with useReducer](https://twitter.com/kentcdodds/status/1203684534790705153)

[thinking in react hooks](https://news.ycombinator.com/item?id=21772038)

[newbie confusion](https://twitter.com/dan_abramov/status/1208090929497886720). [difficult things](https://twitter.com/mxstbr/status/1208133798602399745)

[TS tricks for React](https://react.christmas/2019/21)

[My browser does what?](https://jaxenter.com/javascript-apis-165333.html)

[classes vs hooks](https://lobste.rs/s/fcl0ba/when_class_based_react_beats_hooks)

[styled components](https://twitter.com/mxstbr/status/1216791579345727493)

[The Many Jobs of JS Build Tools](https://www.swyx.io/writing/jobs-of-js-build-tools/)

[testing react applications](https://jaxenter.com/react-testing-166330.html)

[advanced PWAs](https://jaxenter.com/pwa-push-notifications-167250.html)

[CSS options poll](https://twitter.com/kentcdodds/status/1224900215523512320)

[Replacing Redux with observables and React Hooks](https://blog.betomorrow.com/replacing-redux-with-observables-and-react-hooks-acdbbaf5ba80)

[Things I wish I knew about state management when I started writing React apps](https://news.ycombinator.com/item?id=22290061)

[SSR menagerie](https://twitter.com/_developit/status/1093223382223605762)

[How to Scale a React Component](https://www.youtube.com/watch?v=xn9RNfDlIkE)

[Create dynamic reducers by passing values or functions in as an argument](https://twitter.com/joelnet/status/1228026925559382017)

[Persisting React State in LocalStorage](https://news.ycombinator.com/item?id=22443965)

[a possible approach to leveraging remoteData in React with hooks and TypeScript](https://twitter.com/sharifsbeat/status/1235923964460969984)

[a possible approach to leveraging remoteData in React with hooks and TypeScript](https://twitter.com/sharifsbeat/status/1235923964460969984)

[es6 import for side effects meaning](https://stackoverflow.com/questions/41127479/es6-import-for-side-effects-meaning)

> Import an entire module for side effects only, without importing anything. This runs the module's global code, but doesn't actually import any values.

[ES6 Module Gotchas](https://geedew.com/es6-module-gotchas/)

> If you will have side-effects, separate them and load them in a module with short syntax.

[ES modules: A cartoon deep-dive](https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/)

> The final step is filling in these boxes in memory. The JS engine does this by executing the top-level code — the code that is outside of functions.

> Besides just filling in these boxes in memory, evaluating the code can also trigger side effects. For example, a module might make a call to a server.

> This is one reason to have the module map. The module map caches the module by canonical URL so that there is only one module record for each module. That ensures each module is only executed once. Just as with instantiation, this is done as a depth first post-order traversal.

[testing React apps](https://twitter.com/software_daily/status/1236391177521332229)

[useReducer > useState](https://twitter.com/kentcdodds/status/1237150014834503680)

[typescript without typescript](https://twitter.com/bahmutov/status/1240276223793729538)

[manage html dom with vanilla javascript](https://news.ycombinator.com/item?id=22758218)

[react mental models](https://news.ycombinator.com/item?id=22761622)

[method references & bind](https://stackoverflow.com/questions/1007340/javascript-function-aliasing-doesnt-seem-to-work). [Can you bind 'this' in an arrow function?](https://stackoverflow.com/questions/33308121/can-you-bind-this-in-an-arrow-function).

[the magic of static workflows](https://joshwcomeau.com/gatsby/a-static-future/)

[The Many Jobs of JS Build Tools](https://www.swyx.io/writing/jobs-of-js-build-tools/)

[source maps from top to bottom](https://itnext.io/source-maps-from-top-to-bottom-597bbc07436)

[when does react re-render?](https://news.ycombinator.com/item?id=23004848)

[things to know about react](https://news.ycombinator.com/item?id=23005929)

[How We Reduced Our React App’s Load Time by 60%](https://www.infoq.com/articles/reduce-react-load-time/)

[React-query and swr](https://twitter.com/housecor/status/1265103048365441024)

- Should I cache data on the client for a certain period?
- Should I load fresh data when the tab is refocused, or the network reconnects?
- Should I retry failed HTTP calls?
- Should I return cached data, then fetch fresh data behind the scenes?
- Should I handle server cache separately from app state?
- Should I avoid refetching recently fetched data?
- Should I prefetch data the user is likely to want?

[Common mistakes writing React components with hooks ](https://news.ycombinator.com/item?id=23906402).

[A React implementation of Spectrum, Adobe’s design system](https://news.ycombinator.com/item?id=23919509)

[render props are not dead](https://www.youtube.com/watch?v=pn0pIgdQvhU&list=PLCC436JpVnK0Q4WHoB85ZYBwcCyTaMgAl&index=6&ref=hackernoon.com) [Exploring Render Props Vs. React Hooks In 2020
](https://hackernoon.com/exploring-render-props-vs-react-hooks-in-2020-xg1b3uko). [Using custom hooks in place of "render props"](https://dev.to/emeka/using-custom-hooks-in-place-of-render-props-38mf)

[modern forms in react](https://www.youtube.com/watch?v=v1JAUiqskiw)

cancelling promises with hooks
https://reactjs.org/docs/hooks-state.html
https://juliangaramendy.dev/use-promise-subscription/
https://medium.com/@rajeshnaroth/writing-a-react-hook-to-cancel-promises-when-a-component-unmounts-526efabf251f
https://dev.to/rodw1995/cancel-your-promises-when-a-component-unmounts-gkl
https://www.reddit.com/r/reactjs/comments/blhj2b/how_do_i_cancelignore_previously_running_promises/
https://itnext.io/introduction-to-abortable-async-functions-for-react-with-hooks-768bc72c0a2b
https://codesandbox.io/s/useeffect-react-hooks-cancel-promise-h6dcw
https://github.com/Lemoncode/react-hooks-by-example/issues/4
https://stackoverflow.com/questions/49906437/how-to-cancel-a-fetch-on-componentwillunmount
https://github.com/microsoft/PowerBI-JavaScript/wiki/Bootstrap-For-Better-Performance
https://github.com/microsoft/PowerBI-client-react#powerbi-client-react

https://react-query.tanstack.com/

[How I built a modern website in 2021](https://kentcdodds.com/blog/how-i-built-a-modern-website-in-2021)

[We memo all the things (2020)](https://news.ycombinator.com/item?id=28987421)

[Django, HTMX and Alpine.js: Modern websites, JavaScript optional](https://news.ycombinator.com/item?id=29319034)

[Hypermedia-Driven Application (HDA) architecture](https://twitter.com/htmx_org/status/1490333129000697856)

[Hooks: React’s Do-Notation](https://news.ycombinator.com/item?id=30495034)

[Story of a Failed React Project](https://javascript.plainenglish.io/story-of-a-failed-react-project-f32177479bdf)

[Announcing TypeScript 4.6](https://devblogs.microsoft.com/typescript/announcing-typescript-4-6/)

[Things you don't need JavaScript for](https://news.ycombinator.com/item?id=30512512)

[Hooks Considered Harmful](https://news.ycombinator.com/item?id=30753127)

[Preventing XSS in React (Part 1): Data binding and URLs](https://pragmaticwebsecurity.com/articles/spasecurity/react-xss-part1.html). [(Part 2): dangerouslySetInnerHTML](https://pragmaticwebsecurity.com/articles/spasecurity/react-xss-part2.html). [React XSS Guide: Examples and Prevention](https://www.stackhawk.com/blog/react-xss-guide-examples-and-prevention/).

> React applies auto-escaping

> The React APIs are aware of common XSS vulnerabilities and apply the necessary protection. That same protection is applied when the components are generated from JSX code, instead of through the React APIs. 

> When this component is rendered, the data in the review will be placed inside the HTML p tag. Thanks to the auto-escaping applied by React, malicious content in the review will not be seen as code.  

[With the new transform, you can use JSX without importing React.](https://reactjs.org/blog/2020/09/22/introducing-the-new-jsx-transform.html)

[suspense](https://blog.logrocket.com/async-rendering-react-suspense/). [React Suspense & Concurrent Mode: Async Rendering](https://apiumhub.com/tech-blog-barcelona/react-suspense-concurrent-mode-async-rendering/). [Building Great User Experiences with Concurrent Mode and Suspense](https://reactjs.org/blog/2019/11/06/building-great-user-experiences-with-concurrent-mode-and-suspense.html)

> You’ll probably have some Loading flag saved with Redux. Suspense will allow you to replace it.

[Preemptive Memoization In React Is Probably Not Evil (Yet)](https://www.zhenghao.io/posts/memo-or-not)

[How to Manage State in a React App – With Hooks, Redux, and More](https://www.freecodecamp.org/news/how-to-manage-state-in-a-react-app/)

[Conquering JavaScript Hydration](https://dev.to/this-is-learning/conquering-javascript-hydration-a9f)

[React v18.0](https://news.ycombinator.com/item?id=30844414)

[A Guide to React Hooks Stale-while-revalidate Data Fetching](https://www.toptal.com/react-hooks/stale-while-revalidate)

[wretch VS react-query](https://www.libhunt.com/compare-wretch-vs-react-query)

[react-query](https://react-query.tanstack.com/) 

> Fetch, cache and update data in your React and React Native applications all without touching any "global state".

[Does React Query replace Redux, MobX or other global state managers?](https://react-query.tanstack.com/guides/does-this-replace-client-state)

> let's start with a few important items:

> React Query is a server-state library, responsible for managing asynchronous operations between your server and client

> Redux, MobX, Zustand, etc. are client-state libraries that can be used to store asynchronous data, albeit inefficiently when compared to a tool like React Query

> With those points in mind, the short answer is that React Query replaces the boilerplate code and related wiring used to manage cache data in your client-state and replaces it with just a few lines of code.

> For a vast majority of applications, the truly globally accessible client state that is left over after migrating all of your async code to React Query is usually very tiny.

[Query Invalidation](https://react-query.tanstack.com/guides/query-invalidation). [React Query Tutorial - 22 - Query Invalidation](https://www.youtube.com/watch?v=ldg3QIT53pI). [Query Invalidation in React Query](https://backbencher.dev/articles/query-invalidation-in-react-query). [query keys](https://react-query.tanstack.com/guides/query-keys)

> Waiting for queries to become stale before they are fetched again doesn't always work, especially when you know for a fact that a query's data is out of date because of something the user has done. 

[Use React.memo() wisely](https://dmitripavlutin.com/use-react-memo-wisely/) 

> Every time a parent component defines a callback for its child, it creates new function instances. Let's see how this breaks memoization

> Let's apply useCallback() to preserve the callback instance between renderings

[Optimizing React performance by preventing unnecessary re-renders](https://www.debugbear.com/blog/react-rerenders)

> When a component re-renders, React will also re-render child components by default.

[React Virtual DOM Explained in Simple English](https://programmingwithmosh.com/react/react-virtual-dom-explained/)

> Each element is a node on this tree. If the state of any of these elements changes, a new virtual DOM tree is created. This tree is then compared or “diffed” with the previous virtual DOM tree.

> Once this is done, the virtual DOM calculates the best possible method to make these changes to the real DOM. 

[Understanding Reconciliation: React Rendering Phases](https://dev.to/thee_divide/reconciliation-react-rendering-phases-56g2)

> There are two phases to the React rendering cycle.

> The render phase and the commit phase.

> Here's the quick overview. The Render phase takes your JSX and turns it into a javascript representation of what the HTML structure should look like. This is called the VirtualDOM. While the commit phase is actually taking that representation and applying it to the real DOM. The whole process is called reconciliation.

[Trigger child re-rendering in React.js](https://stackoverflow.com/questions/30034265/trigger-child-re-rendering-in-react-js)

[Using forwardRef in React to clean up the DOM](https://blog.logrocket.com/cleaning-up-the-dom-with-forwardref-in-react/)

[10 React Antipatterns to Avoid](https://www.youtube.com/watch?v=b0IZo2Aho9Y)

[Thinking on ways to solve DIALOG](https://www.youtube.com/watch?v=GDzzIlRhEzM)

[React 18 Strict Mode](https://twitter.com/DavidKPiano/status/1523396823914008577)

[Intro to Storybook for React with Figma](https://www.youtube.com/watch?v=p2sZKAPOQXs)

[Complex State Management in React](https://www.telerik.com/blogs/complex-state-management-react)

[React Hooks Best Practices in 2022](https://dev.to/kuldeeptarapara/react-hooks-best-practices-in-2022-4bh0)

[Building a rich text editor with Lexical and React](https://blog.logrocket.com/build-rich-text-editor-lexical-react/)

[UseTransition() Vs UseDeferredValue() In React 18](https://blog.openreplay.com/usetransition-vs-usedeferredvalue-in-react-18)

[Understanding TypeScript 4.7 and ECMAScript module support](https://blog.logrocket.com/typescript-4-7-ecmascript-module-support/)

[try XState](https://twitter.com/AdamRackis/status/1527794654594445313). https://xstate.js.org/. [with React](https://xstate.js.org/docs/recipes/react.html).

[Practical React Query](https://tkdodo.eu/blog/practical-react-query). [tweet](https://twitter.com/abdadeel_/status/1527747604712415233).

[React Interview Questions ( v17.0.x )](https://learning-zone.github.io/react-interview-questions/)

[Goodbye, useEffect](https://www.youtube.com/watch?v=HPoC-k7Rxwo). [Everything you need to know about React 18](https://www.youtube.com/watch?v=Z-NCLePa2x8). [React 18: useEffect Double Call; Mistake or Awesome?](https://www.youtube.com/watch?v=j8s01ThR7bQ). [useEvent](https://twitter.com/dan_abramov/status/1522218410695794694). [Suppressing the linter is wrong and causes bugs.](https://twitter.com/dan_abramov/status/1522226438631473152). [What are legitimate dependency array items?](https://blog.logrocket.com/guide-to-react-useeffect-hook/). [github issue](https://github.com/facebook/react/issues/24502). [ensuring reusable state](https://reactjs.org/docs/strict-mode.html#ensuring-reusable-state). [How to support Reusable State in Effects](https://github.com/reactwg/react-18/discussions/18). [Effects that require cleanup should have symmetry.](https://github.com/reactwg/react-18/discussions/18)

> This brings us to an important question: What items should be included in the dependency array? According to the React Docs, you have to include all values from the component scope that change their values between re-renders.
> What does this mean, exactly? All external values referenced inside of the useEffect callback function, such as props, state variables, or context variables, are dependencies of the effect. Ref containers (i.e., what you directly get from useRef() and not the current property) are also valid dependencies. Even local variables, which are derived from the aforementioned values, have to be listed in the dependency array.
> It is essential to understand the conceptual thinking of effects; the React team wants you to treat every value used inside of the effect as dynamic. So even if you use a non-function value inside the effect, and you are pretty sure this value is unlikely to change, you should include the value in the dependency array.
> That’s because — however unlikely it may be — there is still a chance the value will change. Who knows whether the component will get refactored? Suddenly, the value is no longer constant in every case, and you might have introduced a potential stale prop/state/context bug.

> Whether a component gets hidden or unmounted, refs that are attached to host components (like HTML elements) will be cleaned up and re-initialized the same as they are today during unmount/remount.

> Refs that store use-managed values won't be reset when a component is hidden though. They allow things to be persisted for the case where a component is hidden and later shown again.

[stale closure bugs](https://dmitripavlutin.com/react-hooks-stale-closures/). [useEffect and stale closures](https://medium.com/edonec/useeffect-and-stale-closures-ea74df7ac452). [Hooks, Dependencies and Stale Closures](https://tkdodo.eu/blog/hooks-dependencies-and-stale-closures). [5 Mistakes to Avoid When Using React Hooks](https://dmitripavlutin.com/react-hooks-mistakes-to-avoid/). [video](https://www.youtube.com/watch?v=QdByGrUzmY8). [video](https://www.youtube.com/watch?v=eVRDqtTCd74).

[Fetch as you render](https://twitter.com/housecor/status/1531642615283625984). [Stack the bars, move them to the left](https://twitter.com/ryanflorence/status/1531643540677070849).

[AbortController](https://developer.mozilla.org/en-US/docs/Web/API/AbortController). [Cancelling fetch in React and TypeScript](https://www.carlrippon.com/cancelling-fetch-in-React-and-typescript/). [Using AbortController (with React Hooks and TypeScript) to cancel window.fetch requests](https://dev.to/bil/using-abortcontroller-with-react-hooks-and-typescript-to-cancel-window-fetch-requests-1md4). [Cancel Properly HTTP Requests in React Hooks and avoid Memory Leaks](https://dev.to/viclafouch/cancel-properly-http-requests-in-react-hooks-and-avoid-memory-leaks-pd7). [Handling API request race conditions in React](https://sebastienlorber.com/handling-api-request-race-conditions-in-react). [Abort controller and race conditions in React](https://wanago.io/2022/04/11/abort-controller-race-conditions-react/). [Using React to understand Abort Controllers](https://medium.com/@icjoseph/using-react-to-understand-abort-controllers-eb10654485df). [isMounted is an Antipattern](https://es.reactjs.org/blog/2015/12/16/ismounted-antipattern.html). [Is there a way to check if the react component is unmounted?](https://stackoverflow.com/questions/39767482/is-there-a-way-to-check-if-the-react-component-is-unmounted). [React - How to Check if a Component is Mounted or Unmounted](https://jasonwatmore.com/post/2021/08/27/react-how-to-check-if-a-component-is-mounted-or-unmounted). [How to use Abort Controller to abort APIs initiated from inside useEffect but triggered by user action?](https://stackoverflow.com/questions/67469457/how-to-use-abort-controller-to-abort-apis-initiated-from-inside-useeffect-but-tr). [I'm starting to give up on React Strict Mode](https://twitter.com/schickling/status/1523378971458498560). [The tricky behavior of useEffect hook in React 18](https://medium.com/geekculture/the-tricky-behavior-of-useeffect-hook-in-react-18-282ef4fb570a).

[abort controller and hooks <- best solution?](https://twitter.com/kentcdodds/status/1246219272562421760).

> Check out Wretch. Its pretty nice fetch wrapper with abort controller support

[dynamic and recursive forms with Formik](https://wanago.io/2022/05/09/dynamic-recursive-forms-formik-typescript-react/)

[React Spectrum and React Aria now support React 18!](https://react-spectrum.adobe.com/releases/2022-05-27.html).

[Avoid putting volatile function instances into useEffect dependencies](https://twitter.com/sompylasar/status/1246305338875195392).

> Avoid putting volatile function instances into useEffect dependencies: useCallback name gives misleading confidence. It can and will return new functions so the effect will rerun! And old effect cleanup will get called! Store the functions in Refs, from them close over Refs only.

> useCallback only makes sense for extra targeted performance optimization, and in the context of passing callbacks into subscription effects (e.g. onSomething props) to avoid re-subscribing to events. These effects must not do anything else side-effectful, or that will get rerun.

[React v18.0](https://es.reactjs.org/blog/2022/03/29/react-v18.html). [How to Upgrade to React 18](https://reactjs.org/blog/2022/03/08/react-18-upgrade-guide.html). [Sneak peek into React 18 useDeferredValue hook](https://blog.saeloun.com/2022/01/13/react-18-useDefferedValue-hook.html). ["useTransition() vs useDeferredValue](https://www.youtube.com/watch?v=lDukIAymutM).

[Mastering React Context: Do you NEED a state manager?](https://www.youtube.com/watch?v=MpdFj8MEuJA). [Top 5 React State Management Libraries in 2022](https://www.youtube.com/watch?v=DaqzO22LTdk). [Picking From 20 React State Managers](https://www.youtube.com/watch?v=P95DuIBwnqw).

[mastering useEffect](https://youtu.be/dH6i3GurZW8)

[Setting up a dev environment with React, Vite, and Tailwind](https://blog.logrocket.com/setting-up-dev-environment-react-vite-tailwind/)

[Some misunderstandings with React.memo, useMemo, and useCallback](https://albertyuebaixu.medium.com/some-misunderstandings-with-react-memo-usememo-and-usecallback-27449b670d60)

[Are you in multi-step-form hell with useState/useEffect?](https://twitter.com/statelyai/status/1534493188630532096)

[Using Functions as Children and Render Props in React Components](https://www.codedaily.io/tutorials/Using-Functions-as-Children-and-Render-Props-in-React-Components)

> This only works because our LoadContent understands how to deal with children when it's a function.

[XState with TypeScript](https://twitter.com/statelyai/status/1537760720900657158). [Stop using isLoading booleans](https://kentcdodds.com/blog/stop-using-isloading-booleans). [tweet](https://twitter.com/DavidKPiano/status/1537126730011398144). [XState for handling forms](https://twitter.com/statelyai/status/1536673052045373441). [useEffect talk hit a nerve](https://twitter.com/mattpocockuk/status/1537022877131849729)

[How to decide between useState, useReducer and XState](https://www.youtube.com/watch?v=FrNXCJa5FLs)

[guidance on effects](https://twitter.com/dan_abramov/status/1537419089605545986). [effects in event handlers communicate intent better](https://twitter.com/DavidKPiano/status/1537136365212770304).

[the first draft of You Might Not Need an Effect](https://beta-reactjs-org-git-you-might-not-fbopensource.vercel.app/learn/you-might-not-need-an-effect)

[React UI Library Structure, Storybook and Tests](https://www.youtube.com/watch?v=NgkYH97Z3nk)

[React Aria's date/time pickers](https://react-spectrum.adobe.com/blog/date-and-time-pickers-for-all.html)

>  As with all of React Aria, our hooks give you full control over the
>  rendering and styling of your components, while letting us handle the
>  internationalization and accessibility challenges for you. We have examples
>  using many different styling libraries, such as Tailwind CSS, Styled
>  Components, CSS modules, and Chakra UI.


