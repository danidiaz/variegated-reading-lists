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


