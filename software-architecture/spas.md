[Escaping the SPA rabbit hole with modern Rails](https://medium.com/@jmanrubia/escaping-the-spa-rabbit-hole-with-turbolinks-903f942bf52c) [hn](https://news.ycombinator.com/item?id=17472485) [related video](https://youtu.be/SWEts0rlezA?t=284)

[If your CV only contains jQuery…](https://ayende.com/blog/183650-A/if-your-cv-only-contains-jquery)

[Vue.js: the good, the meh, and the ugly](https://medium.com/@Pier/vue-js-the-good-the-meh-and-the-ugly-82800bbe6684) [HN](https://news.ycombinator.com/item?id=17466400)

[the typescript tax](https://medium.com/javascript-scene/the-typescript-tax-132ff4cb175b)

[slugs](https://itnext.io/whats-a-slug-f7e74b6c23e0)

> An API shall not return the internal id used within the database, but return a slug instead,

[reinventing the browser](https://twitter.com/garybernhardt/status/1240024841895305216)

[Server-Sent Events: the alternative to WebSockets you should be using](https://news.ycombinator.com/item?id=30312897)

[CORS is not meant to secure an API endpoint](https://news.ycombinator.com/item?id=30320113)

> you can never prevent cross-site POST requests from being initiated, with or without CORS

[Best Practices - OAuth for Single Page Applications](https://curity.io/resources/learn/spa-best-practices/) (see also the security reading list).

> Storage mechanisms are unsafe

> Token lifetimes should be kept short

> Because of the issues outlined above, the best security recommendation for an
> SPA is to avoid keeping tokens in the browser at all. This can be achieved
> with the help of a lightweight back-end component, often described as a
> Backend-For-Frontend.

> The backend component can then be configured as a confidential OAuth client
> and used to keep tokens away from the browser. It can either be stateful and
> keep tokens in custom storage, or stateless and store the tokens in encrypted
> HTTP-only, same-site cookies. Whichever variant is chosen, the backend
> component creates a session for the SPA, using HTTP-only, secure, same-site
> cookies, thus enabling a high level of security. Such cookies cannot be read
> by scripts and are limited to the domain of the SPA

[How modern browsers work](https://twitter.com/addyosmani/status/1492398000500404227)

[Easiest way to build a CRUD app?](https://news.ycombinator.com/item?id=30320837)

[Server-Sent Events, WebSockets, and HTTP](https://news.ycombinator.com/item?id=30403438)

[Evolving your RESTful APIs](https://twitter.com/nicolas_frankel/status/1497982480367988736)

[req, an HTTP scripting language](https://andrewpillar.com/programming/2022/02/26/req-an-http-scripting-language/)

[SPAs were a mistake](https://gomakethings.com/spas-were-a-mistake/). [hn](https://news.ycombinator.com/item?id=30528473).

[Are SPAs better than MPAs?](https://www.youtube.com/watch?v=ivLhf3hq7eM)

[UX Patterns: Stale-While-Revalidate](https://www.infoq.com/news/2020/11/ux-stale-while-revalidate/). [http-stale-while-revalidate](https://datatracker.ietf.org/doc/html/draft-nottingham-http-stale-while-revalidate-01). [Keeping things fresh with stale-while-revalidate](https://web.dev/i18n/en/stale-while-revalidate/). 

[hydration is overhead](https://twitter.com/mhevery/status/1516844814792224770)

[Comparing Native Java REST API Frameworks](https://twitter.com/mraible/status/1517073408479137793). [ZalandoTech REST API guidelines](https://twitter.com/bmarwell/status/1516842447804014593)

[Web Development for Beginners](https://news.ycombinator.com/item?id=31299716)

[graphql = trap?](https://news.ycombinator.com/item?id=31284846)

[The balance has shifted away from SPAs](https://news.ycombinator.com/item?id=31459316)

[Are all popular APIs moving to Cursor based pagination?](https://news.ycombinator.com/item?id=31541070)

[Intersection Observer API](https://developer.mozilla.org/en-US/docs/Web/API/Intersection_Observer_API). [Intersection Observer](https://www.w3.org/TR/intersection-observer/). [Javascript. Intersection Observer](https://latteandcode.medium.com/javascript-intersection-observer-1410b743c991).

[SPAs: theory versus practice](https://nolanlawson.com/2022/06/27/spas-theory-versus-practice/).

[Firing up a screen reader to test your pages should become just as natural and habitual as resizing the browser to test your pages.](https://twitter.com/SaraSoueidan/status/1550040197630496768)

[complex ARIA patterns](https://twitter.com/hdv/status/1554437709929881602)

[cache your CORS](https://news.ycombinator.com/item?id=32907234)

[Documenting APIs: A guide for technical writers and engineers](https://idratherbewriting.com/learnapidoc/)

[stuff about Openapi 3.1](https://github.com/Kong/insomnia/issues/4732). [links](https://swagger.io/docs/specification/links/).

> Links are one of the new features of OpenAPI 3.0. Using links, you can describe how various values returned by one operation can be used as input for other operations. This way, links provide a known relationship and traversal mechanism between the operations. The concept of links is somewhat similar to hypermedia, but OpenAPI links do not require the link information present in the actual responses.

[What is the meaning of a Media Type Object with no schema defined?](https://github.com/OAI/OpenAPI-Specification/discussions/2874)

> When you define the media type, you're telling the user what is expected to go over the wire. The schema is there to help validate the actual content. However, in many cases, a schema doesn't make sense - PDFs, audio files, binary files and so on, so specifying the schema is pointless.

> At the moment, we only support JSON Schema for the Schema Object, meaning you can only describe JSON payloads (and to some limited extent XMLs). Had we supported things like XSD (which we may in the future), that would allow you to define schemas (or something similar) for additional media types.

[Progressively Enhanced Single Page Apps](https://twitter.com/kentcdodds/status/1579854003042516993)

[Modern frontends with Thymeleaf and htmx](https://www.youtube.com/watch?v=POK4Zp1oRN8)

[Remix technical explanation](https://remix.run/docs/en/v1/pages/technical-explanation)

[htmx demo](https://twitter.com/htmx_org/status/1583471247043592193)

[spas vs ssr](https://twitter.com/housecor/status/1601575828189753345)

[The state of HTTP in 2022](https://blog.cloudflare.com/the-state-of-http-in-2022/)


