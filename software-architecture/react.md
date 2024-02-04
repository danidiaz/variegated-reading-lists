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

[why React re-renders](https://news.ycombinator.com/item?id=32485460)

[How Nix Derivation Instantiation Works](https://comono.id/posts/2020-03-20-how-nix-instantiation-works/). [Nix Derivation Basics](https://scrive.github.io/nix-workshop/04-derivations/01-derivation-basics.html)

[Create a Drag-and-Drop Zone in React with react-dropzone](https://blog.openreplay.com/create-a-drag-and-drop-zone-in-react-with-react-dropzone). [react-dropzone](https://react-dropzone.js.org/). [GitHub - react-dropzone/react-dropzone: Simple HTML5 drag-drop zone](https://github.com/react-dropzone/react-dropzone).

[React form tip](https://twitter.com/DavidKPiano/status/1569361453928300545). [testing](https://twitter.com/bahmutov/status/1569384088309571587).

[Parent component re-renders all children](https://stackoverflow.com/questions/40819992/react-parent-component-re-renders-all-children-even-those-that-havent-changed). [The mystery of React Element, children, parents and re-renders](https://www.developerway.com/posts/react-elements-children-parents). [React re-renders guide: everything, all at once](https://www.developerway.com/posts/react-re-renders-guide). [React Tracked: Manage state and prevent excessive re-rendering](https://blog.logrocket.com/react-tracked-manage-state-prevent-excessive-re-rendering/). [Just Say No to Excessive Re-Rendering in React](https://www.grapecity.com/blogs/just-say-no-to-excessive-re-rendering-in-react). [Why Did You Render](https://medium.com/welldone-software/track-react-redux-redundant-re-renders-with-why-did-you-render-version-3-9f31f2797057).

[Fixing Redux/Zustand Re-Renders](https://www.youtube.com/watch?v=aOt4Hz3ze3Q). [Mastering React Memo](https://www.youtube.com/watch?v=DEPwA3mv_R8)

[TypeScript Tip #29 - unexpected useState beaviour](https://twitter.com/mattpocockuk/status/1570377640137179137)

[why keys](https://twitter.com/dan_abramov/status/1570557622620950536)

[MUI Base](https://twitter.com/MUI_hq/status/1570695041034731520)


[Zustand](https://twitter.com/0xca0a/status/1571084168821604353). [zustand issue](https://github.com/pmndrs/zustand/issues/82). [createContext can be used to initialize a store](https://github.com/pmndrs/zustand/pull/553/files). [Zustand recipes](https://docs.pmnd.rs/zustand/recipes/recipes). [oops](https://github.com/pmndrs/zustand/discussions/552). [How to use zustand in a non-singleton way](https://github.com/pmndrs/zustand/issues/162). [How to make a store instance per Component](https://github.com/pmndrs/zustand/issues/128). 

> however, you would then only have access to your store inside this component. As far as I know, the general approach with zustand is that you export the useStore hook created with create, and then access it from wherever you want just by importing the hook.

[useContext](https://reactjs.org/docs/hooks-reference.html#usecontext)

> When the nearest <MyContext.Provider> above the component updates, this Hook will trigger a rerender with the latest context value passed to that MyContext provider. Even if an ancestor uses React.memo or shouldComponentUpdate, a rerender will still happen starting at the component itself using useContext.

[Preventing rerenders with React.memo and useContext hook](https://github.com/facebook/react/issues/15156)

[passing a hook as a prop](https://stackoverflow.com/questions/66800263/passing-a-hook-as-a-prop)

> setCount is not a hook, it is just another function, So you can pass it as a prop. You can also think of the output of useMemo or useCallback, these can be passed as a prop.

> useState is a hook, useCallback is a hook, or even for a matter any function, which encapsulates other hooks, these should not be passed as prop.

[lifting state up](https://beta.reactjs.org/learn/sharing-state-between-components#lifting-state-up-by-example). [passing setState down](https://www.reddit.com/r/reactjs/comments/u5ol8w/is_it_bad_to_pass_usestate_as_a_prop_to_a/).

> Obligatory hey-don't-put-too-many-things-in-context, if the items you're passing down are immutable / have consistent references (ex: constants, setState, component functions wrapped in useCallback with empty / immutable deps, etc), great! You can access those items anywhere below that context provider in the tree, and not have to worry about performance issues.

> However, if that stuff you're passing down changes somewhat regularly (whether in value or reference), you're going to be forcing rerenders on every single component that relies on that context, regardless of if you're actually using those values in the component. It's fine in extremely small apps where a change only rerenders a handful of components, but it's going to exponentially cause issues the bigger and bigger your app gets.

[React: Lifting state up is killing your app](https://blog.goncharov.ai/react-lifting-state-up-is-killing-your-app) (must the "lift state up" pattern always be combined with useMemo for performance?). [reddit](https://www.reddit.com/r/reactjs/comments/dhck3y/react_lifting_state_up_is_killing_your_app/).

> Maybe I'm getting confused, but wasn't React.memo() used to handle this kind of problems? To avoid child components to update when the parent had triggered a re render and the child didn't actually change props. Again, maybe I'm getting confused with something else

[When should you NOT use React memo?](https://stackoverflow.com/questions/53074551/when-should-you-not-use-react-memo)

> You should always use React.memo LITERALLY, as comparing the tree returned by the Component is always more expensive than comparing a pair of props properties

> So don't listen to anyone and wrap ALL functional components in React.memo. React.memo was originally intended to be built into the core of functional components, but it is not used by default due to the loss of backward compatibility. (Since it compares the object superficially, and you MAYBE are using the nested properties of the sub-object in the component) =)

> If your component uses DEEP COMPARING PROPS then don't use memo, otherwise ALWAYS use it, comparing TWO OBJECTS is ALWAYS CHEAPER than calling React.createElement() and comparing two trees, creating FiberNodes, and so on.

> I believe the only caveat is in case your props are memory-heavy. Memoizing means storing props in memory potentially forever, i.e. until the next rerender, where new potentially memory-heavy props need to be stored. 

> it doesn't depend on the size of props (memory) - it depends on the number of props. If I had to guess, situations where there there are a lot of props (more than vdom nodes + attributes), are exceedingly rare. 

[Use React.memo() wisely](https://dmitripavlutin.com/use-react-memo-wisely/). [What are React pure functional components?](https://blog.logrocket.com/what-are-react-pure-functional-components/#how-to-react-memo). [Boost Your React Applications with React.memo, useCallback, and useMemo](https://medium.com/nerd-for-tech/boost-your-react-apps-with-react-memo-usecallback-and-usememo-52dfe9575ec6). Does react memo require *completely pure* components???? I don't think so. [Common Pitfalls of Using React.memo()](https://www.copycat.dev/blog/react-memo/). [official docs](https://reactjs.org/docs/react-api.html#reactmemo).

> React.memo only checks for prop changes. If your function component wrapped in React.memo has a useState, useReducer or useContext Hook in its implementation, it will still rerender when state or context change.

[Micro-State management with Zustand in React.](https://learnersbucket.com/tutorials/react/micro-state-management-with-zustand-in-react/)

>  In module state, stores are defined in modules and we export them, they work on the Singleton + Factory design pattern where all the boilerplate logic to create the store and update them will reside in a module (function) that can be exported and used.

[One other thing that the example shows is how nice immer is for immutability and hence memoization. Compare the spread syntax approach:](https://www.reddit.com/r/reactjs/comments/dhck3y/comment/f3pzofn/)

[Why "lifting state up" in react doesn't always work?](https://stackoverflow.com/questions/68487077/why-lifting-state-up-in-react-doesnt-always-work)

> It's not so much that it can't be done. It's more that it will make things terribly ugly and force prop drilling. If I have a global user, I don't won't to be forced to pass that user state down 6 levels through other components that do nothing with the user object besides forwarding it down further to something that does use it.

> One problem is that if you have a lot of components in your tree that needs to share the same piece of state and they are located far away, you have to "lift up" that state to the main ancestor and then you have to pass the state prop down the hierarchy on each children component.

[What exactly is prop drilling in React?](https://stackoverflow.com/questions/73020737/what-exactly-is-prop-drilling-in-react). [A better way of solving prop drilling in React apps](https://blog.logrocket.com/solving-prop-drilling-react-apps/). [Understanding React Context and Property (Prop) Drilling](https://blogs.perficient.com/2021/12/03/understanding-react-context-and-property-prop-drilling/). [Avoid Prop Drilling with React Context](https://medium.com/swlh/avoid-prop-drilling-with-react-context-a00392ee3d8).  

> Dealing with state management in React applications can be a tricky thing, especially when data needs to be passed from a root component down to deeply-nested components. We, as React developers, often tend to over-engineer our applications by relying too heavily on the Context API and Redux in situations that they aren’t actually needed. We reach out too quickly for these tools — even in basic situations that simply require passing state/data to deeply-nested components — all in an attempt to overcome prop drilling.

> Prop drilling is the unofficial term for passing data through several nested children components, in a bid to deliver this data to a deeply-nested component. The problem with this approach is that most of the components through which this data is passed have no actual need for this data. They are simply used as mediums for transporting this data to its destination component.

> The Context API uses a comparison algorithm that compares the value of its current state to any update it receives, and whenever a change occurs, the Context API broadcasts this change to every component consuming its provider, which in turn results in a re-render of these components.

> This would seem trivial at first glance, but when we rely heavily on Context for basic state management, we over-engineer our application by needlessly pushing all of our states into a context provider. As you’d expect, this isn’t very performant when many components depend on this Context Provider, as they’ll re-render whenever there is an update to the state regardless of whether the change concerns or affects them or not.

> If you only want to avoid passing some props through many levels, component composition is often a simpler solution than context.

> If you’ve built a React application before (and I’m sure you have), you have probably used component composition without recognizing it for what it is: an alternative for managing the state of our application.

[Strategies for mitigating prop drilling with React and TypeScript](https://blog.logrocket.com/mitigating-prop-drilling-with-react-and-typescript/). [Prop Drilling in React: How to Avoid It](https://isamatov.com/react-avoid-prop-drilling/). [Best way to pass props through multiple levels in React ( Prop drilling )](https://stackoverflow.com/questions/70892137/best-way-to-pass-props-through-multiple-levels-in-react-prop-drilling). [Is React Context an antidote for prop drilling?](https://stackoverflow.com/questions/63015028/is-react-context-an-antidote-for-prop-drilling).

> The recommended approach is to connect more components to the store (similar to your #2): https://redux.js.org/style-guide/style-guide#connect-more-components-to-read-data-from-the-store.

> Selecting data from the store is very efficient (assuming you made sure your selectors always return the same reference if the data didn't change), I don't think there is any reason to drill down props that the child component can obtain directly from the store (even if it's just one level down). Approaches #1 and #3 will be worse for performance, as a lot more components will need to rerender for every state change.

[Application State Management with React](https://kentcdodds.com/blog/application-state-management-with-react). [State Colocation will make your React app faster](https://kentcdodds.com/blog/state-colocation-will-make-your-react-app-faster). [Remix: The Yang to React's Yin](https://kentcdodds.com/blog/remix-the-yang-to-react-s-yin).

> There are various categories of state, but every type of state can fall into one of two buckets:

> Server Cache - State that's actually stored on the server and we store in the client for quick-access (like user data).

> UI State - State that's only useful in the UI for controlling the interactive parts of our app (like modal isOpen state).

> We make a mistake when we combine the two. Server cache has inherently different problems from UI state and therefore needs to be managed differently. If you embrace the fact that what you have is not actually state at all but is instead a cache of state, then you can start thinking about it correctly and therefore managing it correctly.

> Another solution people try is to apply one of React's rendering bailout escape hatches like React.memo. This works pretty well in our contrived example because it allows React to skip re-rendering our SlowComponent, but in a more practical scenario, you often suffer from "death by a thousand cuts" which means that there's not really a single place that's slow, so you wind up applying React.memo everywhere. And when you do that, you have to start using useMemo and useCallback everywhere as well (otherwise you undo all the work you put into React.memo). 

[How to use zustand in a non-singleton way (2020)](https://github.com/pmndrs/zustand/issues/162#issuecomment-689203547)

> jotai is out. Please check it. It's designed for non-singleton

[On state management and why I stopped using it](https://dev.to/beggars/on-state-management-and-why-i-stopped-using-it-4di). [React doesn't need state management tool, I said](https://dev.to/tolgee_i18n/react-doesnt-need-state-management-tool-i-said-31l4). [State Management: Separation of Concerns](https://alexei.me/blog/state-management--separation-of-concerns/). [Do You Really Need a React State Management Library?](https://blog.bitsrc.io/react-do-you-really-need-an-external-library-for-state-management-28f67d03ebe5)

> I cringe every time I see state management being shoehorned into simple forms and I have never seen it done in a clean and unobtrusive way. Almost every state management solution I know of has a forms plugin, the fact you even need an additional plugin says all you need to know: don't use state management for forms if you can avoid it.

> Please, for the sake of everyone else around you: stop using state management for loaders and modals. I swear, almost every web application I have seen using state management has loader states and other booleans in state management for the stupidest of things.

> It is often helpful to separate Form State handling from the rest of the UI state.  Reason - Form handling is tricky and nuanced

[React I Love You, But You're Bringing Me Down](https://marmelab.com/blog/2022/09/20/react-i-love-you.html). [tweet](https://twitter.com/tannerlinsley/status/1572291326519169024).

> you decided to get rid of Redux in favor of your own useContext. Except that useContext lacks a crucial feature of Redux: the ability to react to changes in parts of the context

[React component as prop: the right way™️](https://www.developerway.com/posts/react-component-as-prop-the-right-way)

[React Router 6.4](https://www.youtube.com/watch?v=L2kzUg6IzxM)

[optimizing compiler tweet](https://twitter.com/Eli_White/status/1576092090362011649)

[useState: Asynchronous or what?](https://www.youtube.com/watch?v=RAJD4KpX8LA)

[prop drilling](https://twitter.com/housecor/status/1597575317488824320). [React Context](https://twitter.com/t3dotgg/status/1597303632252530689).

[Stop using isLoading booleans](https://kentcdodds.com/blog/stop-using-isloading-booleans)

[What Is TanStack Router And Why I Love It](https://www.youtube.com/watch?v=OwoZtv6u9p4)

[jotai vs. useMemo](https://twitter.com/dai_shi/status/1606488720282386433)

[Store sharable state in the URL](https://twitter.com/housecor/status/1606659422922674178). [useParams hook from react-router](https://reactrouter.com/en/main/hooks/use-params). [another advantage [but... is global state always good?](https://twitter.com/housecor/status/1609547342436499456).

> Make the URL the single source of truth.

[put state in urls!](https://functional.cafe/@morewry@indieweb.social/10961563002047720s)

> Please put state in URLs! Put the state of my search and filters or the product ID I'm currently viewing! Put any state that saves me having to do the same workflow again when I accidentally pull down to refresh, fumble that annoying back button on the side of a mouse, or navigate from browser history on a different device!

[A Visual Guide to React's useEffect (2021)](https://news.ycombinator.com/item?id=34142168)

[passing props using the spread operator](https://dev.to/arikaturika/passing-props-using-the-spread-operator-in-react-52e4)

[Understanding Conditional Rendering in React](https://geromekevin.com/understanding-conditional-rendering-in-react/)

[Multi-Step Form with React & Formik](https://www.reddit.com/r/programming/comments/102myr7/multistep_form_with_react_formik/)

[forms (in)statisfaction](https://twitter.com/kentcdodds/status/1610785661816279041). [more](https://twitter.com/BHolmesDev/status/1610812416207495174). [more](https://twitter.com/Steve8708/status/1626945557515350017). [react-hook-form](https://react-hook-form.com/).

> people overuse react-hook-forms when there is no need. Most of the time
> useReducer and Zod is more than enough, and if you have the option Remix
> Forms

[React Query meets React Router](https://tkdodo.eu/blog/react-query-meets-react-router)

[react-router main concepts](https://reactrouter.com/en/main/start/concepts) [and FAQs](https://reactrouter.com/en/main/start/faq). [[V6] [Feature]: Support absolute paths in descendant <Routes>](https://github.com/remix-run/react-router/issues/8035). [loader trouble](https://twitter.com/housecor/status/1615125193747316736).

[A guide to streaming SSR with React 18](https://blog.logrocket.com/streaming-ssr-with-react-18/)

[A Cure for useState Hell](https://www.builder.io/blog/use-reducer). [but, boilerplate?](https://twitter.com/floydophone/status/1613592378493005824)

[Vercel, Turporepo, Next.js, TanStack Query, Zod, Stitches, Radix UI, Changesets, XState](https://twitter.com/christianhg/status/1613533674087088129)

[so many frameworks](https://twitter.com/mhevery/status/1613939006668177408)

[Safe Data Fetching in Modern JavaScript](https://www.builder.io/blog/safe-data-fetching)

[react-query isloading](https://stackoverflow.com/a/66345922/1364288)

> isLoading will only be true when the query is in a hard loading state where it has no data. Otherwise, it will give you the stale data while making a background refetch. This is on purpose for most cases (stale-while-revalidate). Your data stays in the cache for 5 minutes after your detail view unmounts because that’s the default cacheTime.

[Categorizing Components Into Smart & Dumb](https://www.digitalocean.com/community/tutorials/react-smart-dumb-components). [Presentational and Container Components](https://medium.com/@dan_abramov/smart-and-dumb-components-7ca2f9a7c7d0). [What is a correct usage of smart/dumb component pattern?](https://stackoverflow.com/questions/61906159/what-is-a-correct-usage-of-smart-dumb-component-pattern). [Smart vs Dumb Components: When to use which](https://coderwall.com/p/znkw-q/smart-vs-dumb-components-when-to-use-which). 

[Use React.FC or not?](https://twitter.com/jsjoeio/status/1615484128878788616)

[React Grid - Controlled (Stateless) and Uncontrolled (Stateful) Modes](https://devexpress.github.io/devextreme-reactive/react/grid/docs/guides/controlled-and-uncontrolled-modes/)

[React Data Grid: Grid API](https://www.ag-grid.com/react-data-grid/grid-api/)

[interesting uses of react-query](https://twitter.com/TkDodo/status/1616490384305311745)

[don't use create-react-app](https://twitter.com/adamwathan/status/1616938902966640641). [Next if you need SSR or an api, Vite if you don’t](https://twitter.com/t3dotgg/status/1616920999366365184).

[built-in solutions for data fetching, routing, and server rendering](https://twitter.com/acdlite/status/1617611127982284800). [more](https://twitter.com/heyImMapleLeaf/status/1617943400493481984). [more](https://twitter.com/FredKSchott/status/1617622422810939392)

[tanstack-query irksome things](https://twitter.com/TkDodo/status/1617529812180152320)

["Redux-saga was a bad idea"](https://twitter.com/t3dotgg/status/1618465858275381249)

[How is Remix different from Next.js?](https://remix.run/blog/remix-vs-next). [A Look At Remix And The Differences With Next.js](https://www.smashingmagazine.com/2022/07/look-remix-differences-next/). [another comparison](https://techblog.geekyants.com/remix-vs-nextjs). [one form many actions in remix](https://twitter.com/wking__/status/1618634521506877441)

[TanStack Router: Type safe routing and URL state management for your applications](https://www.youtube.com/watch?v=qUZm3gbMOeo). [What Is TanStack Router And Why I Love It](https://www.youtube.com/watch?v=OwoZtv6u9p4).

> the evolution of react-router?

[Speed Up Your React Apps With Code Splitting](https://www.youtube.com/watch?v=JU6sl_yyZqs)

[Virtual DOM is pure overhead (2018)](https://news.ycombinator.com/item?id=34615578)

[All of the major open-source React frameworks now have the backing of a for-profit company](https://twitter.com/tomlienard/status/1620875348945801216)

[Modularizing React Applications with Established UI Patterns](https://martinfowler.com/articles/modularizing-react-apps.html)

[prop drilling vs. nesting](https://twitter.com/dan_abramov/status/1623771055943831553)

[choosing Next.js](https://twitter.com/thdxr/status/1623848741672259587)

[self-healing apps](https://news.ycombinator.com/item?id=34706624)

[migrating to modern Redux](https://twitter.com/acemarke/status/1624628790218424321)

[How To Inspect Interactions In The Browser](https://www.builder.io/blog/inspect-interactions-in-the-browser)

[React is popular for rational reasons despite being bad for performance](https://lobste.rs/s/n2kovg/react_is_popular_for_rational_reasons)

[where to put state](https://twitter.com/RobertLibsansky/status/1626118873857593344)

[file system routers yay or nay](https://twitter.com/devongovett/status/1626635855199600660)

[keep state low or not](https://twitter.com/housecor/status/1626940633611919360)

[React context react-query](https://twitter.com/TkDodo/status/1627586506402537473). [Don't over-engineer it.](https://twitter.com/iponikar/status/1627653490926587904)

[React query meets react router](https://tkdodo.eu/blog/react-query-meets-react-router)

[useSyncExternalStore](https://beta.reactjs.org/reference/react/useSyncExternalStore). [more](https://blog.saeloun.com/2021/12/30/react-18-usesyncexternalstore-api)

[Transition](https://reactcommunity.org/react-transition-group/transition). [official react docs](https://reactjs.org/docs/animation.html)

> ReactTransitionGroup and ReactCSSTransitionGroup have been moved to the react-transition-group package that is maintained by the community

[weird ErrorBoundary technique](https://twitter.com/TkDodo/status/1628497900895444998)

[synchronizing with effects](https://beta.reactjs.org/learn/synchronizing-with-effects)

[everything would need to be wrapped and subscribed to before it could be read](https://twitter.com/dan_abramov/status/1629541409593098240). [tweet](https://twitter.com/0xca0a/status/1629617963874635777). [tweet](https://twitter.com/en_JS/status/1629580031986118657). [tweet](https://twitter.com/dan_abramov/status/1629597621126922241). [tweet](https://twitter.com/dan_abramov/status/1629872956288512007).

[what are signals](https://news.ycombinator.com/item?id=35009417)

[server components](https://twitter.com/dan_abramov/status/1632118979375292418). [video](https://www.youtube.com/watch?v=h7tur48JSaw)

[random uuid keys](https://www.joshwcomeau.com/react/common-beginner-mistakes/)

[how and when RSC runs](https://twitter.com/dan_abramov/status/1633574036767662080)

[were react hooks a mistake?](https://news.ycombinator.com/item?id=35095115)

[React-query tip: You don't have to mess with error handling on each query](https://twitter.com/housecor/status/1633875496760135681)

[the new documentation for React](https://react.dev/)

[New React docs pretend SPAs don't exist anymore](https://lobste.rs/s/s9hecv/new_react_docs_pretend_spas_don_t_exist)

[refactoring junior's React code](https://twitter.com/JoshWComeau/status/1637900565652078593)

[ref use case examples](https://twitter.com/JoshWComeau/status/1638614346078072833)

[react compiler](https://twitter.com/dan_abramov/status/1638741488778588167). 

[you might not need an effect](https://twitter.com/dan_abramov/status/1638773531881140224)

[react server components](https://twitter.com/dan_abramov/status/1638687992553381889). [rsc microfrontends](https://twitter.com/dan_abramov/status/1638756599970791426). [router internals](https://twitter.com/dan_abramov/status/1638731932426018816). [the server sent a function to the client](https://twitter.com/dan_abramov/status/1638760757239087104). [set up React Server Components WITHOUT NextJS](https://twitter.com/BHolmesDev/status/1643990398824763393)

[start a react project 2023](https://news.ycombinator.com/item?id=35280454)

[How do I dynamically set HTML5 data- attributes using react?](https://stackoverflow.com/questions/27285856/how-do-i-dynamically-set-html5-data-attributes-using-react)

[more about RSC](https://twitter.com/t6adev/status/1639607614932910080). [this time is a good idea](https://twitter.com/dan_abramov/status/1639824633124757504). [a good resource](https://twitter.com/JessePence5/status/1641617190540681216). [more](https://twitter.com/jarredsumner/status/1642032558895677440). [rule-of-thumb](https://twitter.com/dan_abramov/status/1647203329854799872)

[complex wizard flows in React](https://twitter.com/JakeDawkins/status/1637928330099040257)

[we’ve changed our forms recommendations to emphasize uncontrolled inputs a lot more](https://twitter.com/kentcdodds/status/1641925880690749445)

> this will become even more powerful with RSC because it’ll be able to refresh server data automatically 

> This is validating. I've been teaching for years that folks should go against the docs and instead default to uncontrolled inputs instead.

> But I would probably use react hook form if I needed one.

> Worth keeping an eye on the new @radix_ui form primitive. Looks like it will work great with remix.

[Building an adaptive, accessible UI library with React Aria](https://blog.logrocket.com/building-adaptive-accessible-ui-library-react-aria/)

[problem with existing state machines](https://twitter.com/dan_abramov/status/1644759833550135299)

[away from Elm](https://lobste.rs/s/pvrcob/on_endings_why_how_we_retired_elm_at)

[benefits of useReducer](https://twitter.com/housecor/status/1645055575909072896)

[idea for decoupling](https://twitter.com/sebastienlorber/status/1645786038097559553)

[how React, Suspense, and cache mutations fit together](https://twitter.com/brian_d_vaughn/status/1646524735667453956)

[importance of react component composition](https://twitter.com/kentcdodds/status/1646860631805685760)

[Un-Suck Your React Components](https://www.youtube.com/watch?v=vPRdY87_SH0)

[why onSuccess is bad](https://twitter.com/TkDodo/status/1648916857842180097)

[form thoughts](https://twitter.com/tannerlinsley/status/1649481124807319552)

> - Form state is not only global state management, but also very fine-grained, cross cutting, and hot out of the gate (think keystrokes). Most form UX assumes reactive UI around form values and for good reason.
> - Add in validation timing that changes over the course of a form session  and you've got a pretty crazy cocktail of challenges.
> - React Hook Form appears to handle most of this really well, no wonder people love it! I'm not sure if it's the right fit yet though. We'll see.

[Client state often needs to be made globally available because you need it for your QueryKey](https://twitter.com/TkDodo/status/1650197183692431362). [Query is not made to manage synchronous state](https://twitter.com/TkDodo/status/1650153977374187521)

[use client](https://twitter.com/dan_abramov/status/1650216626631983105)

[RSC makes server-client waterfalls a compile error](https://twitter.com/dan_abramov/status/1651051101678977024). [it lets you split each component in two. a Server part which depends on data, and a Client part which depends on state](https://twitter.com/dan_abramov/status/1651699851120242689)

[useEffect interview question](https://twitter.com/NckLcs/status/1651210550049685504)

[is the container component pattern obsolete?](https://blog.bitsrc.io/implementing-the-container-pattern-using-react-hooks-f490a8492d05). [more](https://dev.to/ornio/container-view-pattern-in-react-inc-hooks-5404). [react-hooks-compose](https://www.npmjs.com/package/react-hooks-compose)

>  with the introduction of hooks there is no need to package components like this. Since hooks allow us to isolate logic inside them and then just call them on demand, the need for a container is slowly fading away.

> But as great as hooks are, they do not solve every problem, hence the reason why this approach is still widely used.

> This works fine, but you end up with an extra component just to connect the hook to the Presenter. [doesn't seem that bad...]

[don't read refs while rendering](https://twitter.com/TkDodo/status/1653418114531434498). [ref caveats](https://react.dev/reference/react/useRef#caveats)

[RCS, unintuitive?](https://twitter.com/t3dotgg/status/1654565825620344832)

[the power of forms](https://twitter.com/kentcdodds/status/1478882117425586176)

[JSX.Element vs React.ReactNode](https://twitter.com/mattpocockuk/status/1656285685987377152)

> ReactNode should be your default choice. But often you'll see components being inferred as (props) => JSX.Element

[The React.ReactNode type is a black hole](https://changelog.com/posts/the-react-reactnode-type-is-a-black-hole)

```
type ReactText = string | number;
type ReactChild = ReactElement | ReactText;

interface ReactNodeArray extends Array<ReactNode> {}
type ReactFragment = {} | ReactNodeArray;
type ReactNode = ReactChild | ReactFragment | ReactPortal | boolean | null | undefined;
```

> By default, boolean values don't render anything in React

[useEffect without cleanup](https://twitter.com/jacobmparis/status/1657381743433863170)

[react, ifs, style](https://twitter.com/dan_abramov/status/1657589889070710785)

[react from another dimension](https://twitter.com/vimtor_/status/1657416410514194434)

[react islands](https://twitter.com/dan_abramov/status/1659599923266961420). [additive and composable](https://twitter.com/dan_abramov/status/1659634041153368065).

[you might not need react query](https://twitter.com/TkDodo/status/1659908975502950405)

[Radix + react-hook-form](https://twitter.com/jhooks/status/1659655528451284992)

[You don't have to go through the hoops of creating endpoints, adding fetch logic, etc...](https://twitter.com/CompuIves/status/1660660884534902784)

[the compound component React pattern](https://twitter.com/kyleshevlin/status/1663579666278645761)

[rsc & the container component pattern](https://twitter.com/dan_abramov/status/1663726883341586432). [concerns](https://twitter.com/ryanflorence/status/1663698112274403328)

[Thinking in React Query](https://twitter.com/TkDodo/status/1667279661980610565)

[Good Bye Spinners: Enhancing UX with Optimistic UI](https://www.youtube.com/watch?v=TR_wn2y-SYQ)

[awesome Prometheous alerts](https://twitter.com/MariuszMichaow3/status/1667066786217426944)

[controller inputs are uncool](https://twitter.com/mjackson/status/1667258271655251978)

[Radix's asChild is SUCH a smart abstraction to a tough problem](https://twitter.com/mattpocockuk/status/1666080643216990210)

[asChild in React, Svelte, Vue, and Solid for render delegation](https://medium.com/@bryanmylee/aschild-in-react-svelte-vue-and-solid-for-render-delegation-645c73650ced)

[You Can Stop Hating React.FC](https://www.totaltypescript.com/you-can-stop-hating-react-fc) maybe?

[pre-fill some local state (e.g. the selection of a Dropdown component) with server state](https://twitter.com/TkDodo/status/1672168421339938818)

[React: The Most Common Mistakes in 2023](https://twitter.com/housecor/status/1671976925273661443)

[Bad React Advice You Should Ignore](https://www.youtube.com/watch?v=YlU9vznPWIk)

[boundaries](https://twitter.com/JoshWComeau/status/1674531358339678209)

[Avoiding useEffect with callback refs](https://tkdodo.eu/blog/avoiding-use-effect-with-callback-refs)

[Is it safe to use ref.current as useEffect's dependency when ref points to a DOM element?](https://stackoverflow.com/questions/60476155/is-it-safe-to-use-ref-current-as-useeffects-dependency-when-ref-points-to-a-dom)

[(1) Rendering, (2), Reconciliation, and (3) Committing.](https://twitter.com/bobziroll/status/1679120964280541184)

[Router context](https://twitter.com/notBachitter/status/1680933830495174656)

[Reusable Modals with Radix UI](https://www.youtube.com/watch?v=VM6YRrUsnUY)

[Where to put app logic](https://twitter.com/DavidKPiano/status/1685047651400626176). [more](https://twitter.com/tannerlinsley/status/1685102542710308864).

[Using FormData Objects](https://developer.mozilla.org/en-US/docs/Web/API/FormData/Using_FormData_Objects)

[on the popularity of react-router](https://twitter.com/mattpocockuk/status/1690476430788796416). [react-router and react-query](https://tkdodo.eu/blog/react-query-meets-react-router). [All remix apps use react router so it’s not just SPAs](https://twitter.com/jacobmparis/status/1690533396349411328). [remixing react-router](https://remix.run/blog/remixing-react-router). [The Web’s Next Transition](https://www.epicweb.dev/the-webs-next-transition).

> Remix is changing the game, and they are bringing their data fetching concepts (loaders and actions) to purely client side rendered applications with React Router 6.4. I went through their great tutorial that shows the concept very well and demonstrates how you can quickly build a small, but feature-rich app.

> With React Router coming into the data fetching game, it is naturally interesting to understand how this competes or correlates with existing data fetching and caching libraries like React Query.

> To recap: React Router will allow you to define loaders on each route, which will be called when the route is visited. In the route component itself, you can useLoaderData() to get access to that data. Updating data is as simple as submitting a Form, which will call an action function. Actions invalidate all active loaders, so you'll automagically see updated data on your screen.

> If this sounds very similar to queries and mutations - you are right, it does. So the questions that have been popping up after the announcement of Remixing React Router are:

> All the data components, hooks, and nitty gritty async data management from Remix are coming to React Router 

> When you fetch inside of components, you create what we call render+fetch chains that artificially slow down your page loads and transitions by fetching several data dependencies in sequence instead of in parallel.

[and managing interruptions and race conditions while you display the loading states](https://twitter.com/ryanflorence/status/1696585626794197486)

[vite -> next , SSR](https://twitter.com/youyuxi/status/1696868733728530716). [another tweet](https://twitter.com/leeerob/status/1696863585740152960).

[Things I wish I knew before moving 50K lines of code to React Server Components](https://news.ycombinator.com/item?id=37345727)

[Avoid customizing components only through props. Instead embrace composition](https://twitter.com/_georgemoller/status/1699586420455645263)

[client updates taking over on hydration](https://twitter.com/AdamRackis/status/1700684750220873806)   

[htmx vs. React](https://twitter.com/htmx_org/status/1703819465308197296)

[The Uphill Battle of Memoization](https://tkdodo.eu/blog/the-uphill-battle-of-memoization). [composition](https://twitter.com/dev_bogdan/status/1708147138851451030). [what's the moral](https://overreacted.io/before-you-memo/#whats-the-moral). [One simple trick to optimize React re-renders](https://kentcdodds.com/blog/optimize-react-re-renders).

> React.memo is the imperative way to stop re-renderings. Composition is declarative. Doing it imperatively may break of course because is almost impossible to take charge of all edge cases.

[url state is underrated](https://twitter.com/leeerob/status/1708280997488333078)

[Accessible, Typesafe, Progressively Enhanced Modern Web Forms](https://www.epicweb.dev/accessible-typesafe-progressively-enhanced-modern-web-forms)

[flushSync](https://twitter.com/ryanflorence/status/1710000218543096230)

[crosscut of the absence of god](https://twitter.com/YungKark/status/1709999491560915257)

[when apps don't use urls effectively](https://twitter.com/housecor/status/1717152910713278544)

> If I share a URL and someone doesn't see what I'm seeing, that's typically a problem.

[what and when to fetch](https://twitter.com/mjackson/status/1720566067754684787)

[how to use react-query](https://twitter.com/housecor/status/1724066962433528210)

[component slots in react](https://sandroroth.com/blog/react-slots). 

[tying stuff to routes](https://twitter.com/ryanflorence/status/1725564994077761913)

[Why You Want Need React Query](https://tkdodo.eu/blog/why-you-want-react-query)

[Remix optimistic UIs](https://www.youtube.com/watch?v=d0p95C3Kcsg)

[The Menu/MenuItem](https://twitter.com/javierwchavarri/status/1727186763515625602)

[Recursive components conditional on children](https://twitter.com/kentcdodds/status/1727171008757641698)

[How to cope with a fragile React codebase](https://www.reddit.com/r/reactjs/comments/1816e9v/how_to_cope_with_a_fragile_react_codebase/). [tweet](https://twitter.com/DavidKPiano/status/1727481770445045895)

[Thinking in react query](https://tkdodo.eu/blog/thinking-in-react-query)

[initiate the fetch in the owner component, but await it in the child](https://twitter.com/ryanflorence/status/1728429997072015532)

[another form library](https://twitter.com/BHolmesDev/status/1732950888996573542)

[the history of Redux](https://twitter.com/acemarke/status/1740912269796790679)

[React Server Components: the Good, the Bad, and the Ugly](https://www.mayank.co/blog/react-server-components/)

[The two Reacts](https://twitter.com/dan_abramov2/status/1743038981002969389). [more](https://overreacted.io/the-two-reacts/). [more](https://twitter.com/dan_abramov2/status/1743441693225988485). [video](https://www.youtube.com/watch?v=KuhfT6-I3QU).

[chache invalidation is hard](https://twitter.com/housecor/status/1744449177960992854)

[React Server Components does not require a server](https://twitter.com/dan_abramov2/status/1745795274977493317)

[tweetz](https://twitter.com/dan_abramov2/status/1746117807639609770). [more](https://twitter.com/ryanflorence/status/1746193166259372446). [more](https://twitter.com/dan_abramov2/status/1746283919467487299). [more](https://x.com/AdamRackis/status/1745943372798267600). [more](https://twitter.com/dan_abramov2/status/1746244422092661230). [more](https://twitter.com/dan_abramov2/status/1746250961448763569). [drama](https://twitter.com/AdamRackis/status/1746571911805419987).

[Using TanStack router in preference to React Router](https://twitter.com/housecor/status/1747778158424678437)

[Adding form validation to your React app? Try the "reward early, punish late" pattern](https://twitter.com/BHolmesDev/status/1746911677440774274)

[RCS from scratch](https://twitter.com/BHolmesDev/status/1747797384946487529)

[starting React apps in 2024](https://twitter.com/housecor/status/1747979474413474075)

[Remix client loaders](https://twitter.com/ryanflorence/status/1748024678764183620)

[How to REALLY validate React forms](https://www.youtube.com/watch?v=DwEkvie79xI)

[the output of rendering Server Components is a tree of Client Components](https://twitter.com/samselikoff/status/1749829002909401186)

[Here's how to do server-side table filtering like @linear](https://twitter.com/jacobmparis/status/1706469083078709635)
 
[RCS spinner](https://twitter.com/crutchcorn/status/1754174851936629225)


