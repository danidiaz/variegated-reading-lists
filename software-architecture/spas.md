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

[How does it know I want CSV?](https://news.ycombinator.com/item?id=34410072)

[ Why doesn't the fetch API reject on 404/500/etc](https://twitter.com/jaffathecake/status/1622936551234609154)

[What is a CDN? How do CDNs work? ](https://news.ycombinator.com/item?id=34690656)

[Why I'm not the biggest fan of Single Page Applications](https://www.matuzo.at/blog/2023/single-page-applications-criticism/)

[morphdom](https://github.com/patrick-steele-idem/morphdom)

> Fast and lightweight DOM diffing/patching (no virtual DOM needed)

[hx-trigger](https://htmx.org/attributes/hx-trigger/)

[Writing Javascript without a build system](https://lobste.rs/s/0jzgzb/writing_javascript_without_build_system)

[Modern SPAs without bundlers, CDNs, or Node.js](https://news.ycombinator.com/item?id=34829039)

[Password protect a static HTML page](https://news.ycombinator.com/item?id=34849024)

[Toasts notifications in Thymeleaf with Shoelace and htmx](https://www.wimdeblauwe.com/blog/2023/02/20/toasts-notifications-in-thymeleaf-with-shoelace-and-htmx/)

[Storing Ephemeral UI State with Kredis for Rails](https://blog.appsignal.com/2023/02/22/storing-ephemeral-ui-state-with-kredis-for-rails.html)

[The client-side-templates Extension for htmx](https://htmx.org/extensions/client-side-templates/). [Haskell library](https://hackage.haskell.org/package/stache). [HTMX for ASP.NET Core Developers](https://www.youtube.com/watch?v=uS6m37jhdqM). [jetbrains](https://www.jetbrains.com/dotnet/guide/tutorials/htmx-aspnetcore/clientside-templating/). 

[I suggest splitting your JSON API and your HTML end-points](https://www.reddit.com/r/htmx/comments/ykzy9t/htmx_alongside_an_existing_minimal_json_api/). [Splitting Your Data & Application APIs: Going Further](https://htmx.org/essays/splitting-your-apis/). [Don’t Build A General Purpose API To Power Your Own Front End ](https://max.engineer/server-informed-ui). [Hypermedia APIs vs. Data APIs](https://htmx.org/essays/hypermedia-apis-vs-data-apis/).

[load polling in htmx](https://htmx.org/docs/#ajax)

> an element specifies a load trigger along with a delay, and replaces itself with the response

[hyperscript and htmx](https://htmx.org/docs/#hyperscript)

> Hyperscript is not required when using htmx, anything you can do in hyperscript can be done in vanilla JS or with another javascript library like jQuery, but the two technologies were designed with one another in mind and play well together.

[if you prefer, you can use the `data-` prefix when using htmx](https://news.ycombinator.com/item?id=25233872)

> I don't know why people who make frameworks either prefer invalid HTML, or if they do allow people to write valid HTML they seem to show the invalid code in the docs

> You are not allowed to invent any old attributes you want and add them to any element and have it be valid HTML, but you can invent any attribute you want so long as it begins with `data-`. 

[HTMLElement: change event](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/change_event)

> When the element loses focus after its value was changed: for elements where the user's interaction is typing rather than selection, such as a <textarea> or the text, search, url, tel, email, or password types of the <input> element.

[Your Client Side State is a Lie](https://marcellerusu.com/your_client_side_state_is_a_lie.html). [lobsters](https://lobste.rs/s/69qu6p/your_client_side_state_is_lie)

[a purely client-side SPA (no Node.js server, 100% static bundle) with Next.js](https://twitter.com/dan_abramov/status/1636886736784457734)

[future flags in remix](https://twitter.com/brophdawg11/status/1636808899360706561)

[Reusable htmx components with custom elements](https://cprohm.de/blog/htmx-custom-elements/)

[Dialogs, modality and popovers seem similar. How are they different?](https://hidde.blog/dialog-modal-popover-differences/)

[template fragments](https://twitter.com/htmx_org/status/1649784039568449538) in [htmx](https://htmx.org/essays/template-fragments/)

> w/ htmx composition is moved to the back end via server-side inclusion, custom tags, etc

[The Web’s Next Transition](https://www.epicweb.dev/the-webs-next-transition)

[Htmx Is the Future](https://news.ycombinator.com/item?id=35829733)

[You don't need a modal window](https://youdontneedamodalwindow.dev/)

[more about htmx](https://news.ycombinator.com/item?id=36078709)

[wireframes](https://twitter.com/andybudd/status/1661981838221385729). [motion design](https://twitter.com/andybudd/status/1661985377698172929).

[Content Security Policy (CSP)](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP). [tweet](https://twitter.com/kentcdodds/status/1667297188555419653?).

[use the url](https://twitter.com/housecor/status/1667206997513519112). [it should be central to the design](https://twitter.com/royalicing/status/1667220655954366464). [the problems of not having deep linking](https://twitter.com/fsp_bgd/status/1667441818013712384). [post](https://hachyderm.io/@DiazCarrete/110525098664615724).

[a small talk on remix forms, and what we are looking at going forward with uncontrolled forms](https://twitter.com/VivekLokhande99/status/1668220008533753856)

[Should a POST request render HTML or redirect?](https://stackoverflow.com/questions/12151551/should-a-post-request-render-html-or-redirect)

[forms are hypermedia controls, too](https://twitter.com/htmx_org/status/1668716037745901568). [video mentioning the same](https://youtu.be/Mk8xjRR6qEU?t=170)

> these hypermedia controls, forms & anchors *are why HTML is a hypermedia*

[CSRF protection in Epic Stack](https://twitter.com/kentcdodds/status/1669089812853444609)

[Micro-Frontends in AWS](https://www.youtube.com/watch?v=Wn1Cj7785i8). [Micro-Frontends in Just 10 Minutes](https://www.youtube.com/watch?v=s_Fs4AXsTnA).

[Which HTTP status code means "Not Ready Yet, Try Again Later"?](https://stackoverflow.com/questions/9794696/which-http-status-code-means-not-ready-yet-try-again-later). [HTTP Response code for "Please wait a little bit"](https://stackoverflow.com/questions/12449538/http-response-code-for-please-wait-a-little-bit). [http 204 status code for polling for a resource after a 201 Created](https://stackoverflow.com/questions/21853498/rest-http-204-status-code-for-polling-for-a-resource-after-a-201-created).

[browsers are cool](https://cohost.org/tef/post/1794038-special-interest-inf)

[Route-based dialogs are not great](https://twitter.com/kentcdodds/status/1679936799291084801)

[some REST links](https://hachyderm.io/@DiazCarrete/110735703547058305)

[HTTP has become the default, universal communication protocol](https://lobste.rs/s/hq1sdr/http_has_become_default_universal)

> Over the course of my career, I’ve come across something like O(100) custom protocols for service-to-service communication, all built with the assumption that e.g. JSON-over-HTTP would be too inefficient. These protocols were almost always underspecified, fragile, and fiendishly difficult to maintain. (No shade to their authors on these points – protocol design is hard!)

[SPAs added incidental network complexity vs. traditional HTML + HTTP](https://twitter.com/ryanflorence/status/1682051143319552000)

[htmx](https://twitter.com/BHolmesDev/status/1682037065767329798).

[islands and partial hydration](https://twitter.com/greg_johnston/status/1682751410700447744)

[cache-control : private](https://developer.mozilla.org/en-US/docs/Web/HTTP/Caching). [What is Cache-Control: private?](https://stackoverflow.com/questions/12908766/what-is-cache-control-private). [great answer](https://stackoverflow.com/a/49637255/1364288).

> In the HTTP Caching spec, there are two main types of caches: private caches and shared caches.

> A private cache is a cache tied to a specific client — typically a browser cache. Since the stored response is not shared with other clients, a private cache can store a personalized response for that user.

> On the other hand, if personalized contents are stored in a cache other than a private cache, then other users may be able to retrieve those contents — which may cause unintentional information leakage.

> If a response contains personalized content and you want to store the response only in the private cache, you must specify a private directive.

[Content type for HTML fragments](https://stackoverflow.com/questions/19303361/content-type-for-html-fragments)

[htmx requests and responses](https://htmx.org/docs/)

> Htmx expects responses to the AJAX requests it makes to be HTML, typically HTML fragments (although a full HTML document, matched with a hx-select tag can be useful too)

[Do modern browsers cache ajax responses?](https://stackoverflow.com/questions/41892700/do-modern-browsers-cache-ajax-responses)

[How to let the browser or PHP cache a fetch() request?](https://stackoverflow.com/questions/73271516/how-to-let-the-browser-or-php-cache-a-fetch-request)

> fetch() behaves the same as a regular HTTP request, so you can just apply the standard HTTP rules regarding caching.

[A deep dive into caching REST APIs](https://stellate.co/blog/deep-dive-into-caching-rest-apis)

[Using Cache-Control header with react-query](https://stackoverflow.com/questions/76562503/using-cache-control-header-with-react-query)

> React Query has no knowledge of response headers. It's promise based, and you can use any way you want to produce a promise. So by that definition, it cannot know about network headers.

> Imo there also isn't much value in syncing these two things - they are different layers of caches that build upon each other. If you have browser caching enabled via the Cache-Control header, you can just as well keep staleTime to zero and let the background refetches trigger when necessary, because they will read from the browser cache anyways.

[url with dialog](https://twitter.com/housecor/status/1685269087457329153)

[If Web Components are so great, why am I not using them? ](https://lobste.rs/s/jes0ss/if_web_components_are_so_great_why_am_i_not)

[text fragments API](https://twitter.com/simonw/status/1688931466737303553)

[The Epic Stack now has built-in rate limiting](https://github.com/epicweb-dev/epic-stack/discussions/381)

[RPC – Move Fast and Break Nothing. End-to-end typesafe APIs made easy](https://news.ycombinator.com/item?id=37098875)

[Multipart HTTP response (unusual)](https://stackoverflow.com/questions/47067312/multipart-http-response)

[SSO with the Epic Stack](https://twitter.com/kentcdodds/status/1691643061707878516)

[throttling for performance testing](https://twitter.com/ryanflorence/status/1692166308576850325)

[Don’t build a general purpose API to power your own front end (2021)](https://news.ycombinator.com/item?id=37197257)

[More than you want to know about caching](https://www.youtube.com/watch?v=amflVh0CZ78&list=PLV5CVI1eNcJgNqzNwcs4UKrlJdhfDjshf)

[Content-Disposition](https://developer.mozilla.org/es/docs/Web/HTTP/Headers/Content-Disposition)

[use *events* to integrate your islands of interactivity w/ htmx](https://twitter.com/htmx_org/status/1698333688080298157)

[If your tooling isn't fingerprinting your assets on file changes then you're gonna have caching surprises in production](https://twitter.com/ryanflorence/status/1691911564092404144)

[topt](https://twitter.com/kentcdodds/status/1700685506999361907)

> This library is great for more than just 2FA. If you want to verify a user's email/phone number, you can use this to securely generate a short code for that, this library can do it.

[bulk exports & file management implemented in htmx](https://twitter.com/leiffoged/status/1702473686895517803)

> The first thing I did was wrap the entire file management UI in one big HTML <form> and inserted a checkbox ✅ for each row.

> Then I added 3 buttons (export/move/delete). These buttons open 3 corresponding dialogs (invisible by default w/ a generic loading state baked in).

[every exercise in http://EpicWeb.dev](https://twitter.com/kentcdodds/status/1702546710210511288)

[server-driven UIs](https://twitter.com/samnewman/status/1704113514250490009)

[implement OpenID connect with Google](https://twitter.com/kentcdodds/status/1704939686903652697)

[Why the number input is the worst input](https://stackoverflow.blog/2022/12/26/why-the-number-input-is-the-worst-input/)

[Cache headers could probably be more aggressive (macarthur.me)](https://news.ycombinator.com/item?id=37581646)

[progressive enhancement](https://twitter.com/kentcdodds/status/1705374438001393773)

[error messages](https://dev.to/stripe/designing-apis-for-humans-error-messages-94p)

[REST-endpoints for the UI](https://twitter.com/housecor/status/1709199282878693837). [ split your data & app apis](https://twitter.com/htmx_org/status/1709214306909536330). [backend/frontend split](https://twitter.com/ryanflorence/status/1709212381916876968). [monorepos](https://twitter.com/mattpocockuk/status/1709218143199952994). [backend for frontend](https://twitter.com/DiazCarrete/likes). 

[If-Match](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/If-Match). [lost update problem](https://www.w3.org/1999/04/Editing/#3.1).

[Django things you want with HTMX](https://www.bitecode.dev/p/django-things-you-want-with-htmx)

[Web forms — Working with user data](https://developer.mozilla.org/en-US/docs/Learn/Forms). [Web.FormUrlEncoded.parseAll](https://hackage.haskell.org/package/http-api-data-0.6/docs/Web-FormUrlEncoded.html#v:parseAll). [multipage web forms (2010)](https://www.uxmatters.com/mt/archives/2010/03/pagination-in-web-forms-evaluating-the-effectiveness-of-web-forms.php)

[<input type="checkbox">](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox)

[Accessible, Typesafe, Progressively Enhanced Modern Web Forms](https://www.epicweb.dev/accessible-typesafe-progressively-enhanced-modern-web-forms)

[search params](https://twitter.com/tannerlinsley/status/1714343894626996337)

> - Being able to functionally maintain search params through links and navigate() calls is a critical architecture requirement, but is a footgun as a leaf-node API. Further abstraction is required to make it safe for anyone who isn't a vigilant code surgeon.

[form horror](https://twitter.com/htmx_org/status/1714701042494112026). [more form horror](https://twitter.com/housecor/status/1714960732373049682).

[react-query v5](https://news.ycombinator.com/item?id=37940311)

[MSW 2.0 – Mock Service Worker](https://news.ycombinator.com/item?id=37985777)

[Web components will outlive JavaScript frameworks](https://news.ycombinator.com/item?id=38012662)

[How to use JavaScript's FormData to collect form fields without refs or state](https://twitter.com/ReactTraining/status/1716822590533353817). [FormData/URLSearchParams](https://twitter.com/buildsghost/status/1717288813284991286)

[Updating Other Content](https://htmx.org/examples/update-other-content/)

[honeypot fields in forms](https://twitter.com/kentcdodds/status/1722024476379152706)

[My Favorite State Manager Is...URLs](https://www.youtube.com/watch?v=t3FUkq7yoCw)

[HTMX. respect content download headers #474](https://github.com/bigskysoftware/htmx/issues/474). [Not able to download a file using htmx](https://www.reddit.com/r/htmx/comments/15zst5k/not_able_to_download_a_file_using_htmx/). [Handle file download from ajax post](https://stackoverflow.com/questions/16086162/handle-file-download-from-ajax-post).

[HTMX: Web 1.0 with the benefits of Web 2.0 without the grift of Web 3.0-at JFall 2023 (slides)](https://martijndashorst.com/blog/2023/11/09/jfall-htmx-presentation)

[enum router that uses htmx and a service worker to intercept /frontend routes and runs rust wasm on the client instead](https://twitter.com/swlkr/status/1723447707560485144)

[render close to the data](https://twitter.com/mjackson/status/1724155643152740441)

[HTML First](https://html-first.com/). [hn](https://news.ycombinator.com/item?id=38241304)

[Why I Tend Not To Use Content Negotiation](https://htmx.org/essays/why-tend-not-to-use-content-negotiation/)

[the platform should do more](https://twitter.com/luke_warlow/status/1726000865142599707)

[missing on React aria](https://twitter.com/deeprosa_/status/1726159661009969405)

[In-Place Optimistic UI](https://www.youtube.com/watch?v=Z07vhWKpfXs). [User Feedback with Busy Indicators](https://www.youtube.com/watch?v=agYaOQEFPns). [Optimistic Add](https://www.youtube.com/watch?v=-0Qi0yMyLwQ).

[the subtleties of htmx redirects](https://github.com/bigskysoftware/htmx/issues/2001#issuecomment-1814519590). [Reddit](https://www.reddit.com/r/htmx/comments/18wpe54/comment/kg149ep/).

[htmx archiver example](https://www.youtube.com/watch?v=uLUMM1Y-dd8). [chapter in the hypermedia systems book](https://hypermedia.systems/a-dynamic-archive-ui/)

[Every screen you interact with has multiple personalities](https://www.linkedin.com/feed/update/urn:li:activity:7144604919721783297/). [How to fix a bad user interface](https://www.scotthurff.com/posts/why-your-user-interface-is-awkward-youre-ignoring-the-ui-stack/). [The Nine States of Design](https://medium.com/swlh/the-nine-states-of-design-5bfe9b3d6d85).

[htmx optimistic update tricks](https://twitter.com/htmx_org/status/1744019425404084453). [htmx and scripting](https://twitter.com/htmx_org/status/1744020227715690874). 

[htmx discord: http errors and surface messages](https://discord.com/channels/725789699527933952/1156332851093065788/1156583068749012992)

> error event 

["stateless only on the *server*](https://discord.com/channels/725789699527933952/975839826559508510/1158442937026367498)

[restful way to handle downloads](https://stackoverflow.com/a/38562708/1364288)

[htmx as a layered api](https://twitter.com/htmx_org/status/1744411538826420403)

[ the browser event system is basically a built-in pubsub system](https://twitter.com/ralex1993/status/1745790936808837331). [You can scope these custom events to any DOM node.](https://frontendmasters.com/blog/vanilla-javascript-reactivity/#pubsub-pattern-publish-subscriber)

[HATEOAS: absolute or relative URLs?](https://stackoverflow.com/questions/2239405/hateoas-absolute-or-relative-urls). [Building links in Spring MVC](https://docs.spring.io/spring-hateoas/docs/current/reference/html/#server.link-builder.webmvc). [htmx](https://news.ycombinator.com/item?id=38954800).

[HTMX playground](https://lassebomh.github.io/htmx-playground/). [polly.js](https://netflix.github.io/pollyjs). [mock service worker](https://netflix.github.io/pollyjs).

[components (web or otherwise) for htmx should be components for _HTML_ & use the std integration points w/it: events + input values](https://twitter.com/htmx_org/status/1746995079766835503)

[htmx dropdown trick](https://twitter.com/htmx_org/status/1747383145920643283)

[jsx-for-your-favorite-programming-language](https://twitter.com/htmx_org/status/1750853395831767294)

[presigned POST](https://twitter.com/t3dotgg/status/1750260662042075453)

> What are the advantages of using signed upload URLs to upload files from the browser instead of uploading files through your own backend?

[post-redirect-get](https://hachyderm.io/@DiazCarrete/111841132226571708)

[async auth in HTMX](https://htmx.org/examples/async-auth/)

[How to check and uncheck all checkboxes by clicking one checkbox using alpine js](https://stackoverflow.com/questions/61470556/how-to-check-and-uncheck-all-checkboxes-by-clicking-one-checkbox-using-alpine-js). [reddit](https://www.reddit.com/r/alpinejs/comments/ptgfpd/selectdeselect_all_checkboxes/)

[presigned url flow in htmx?](https://www.reddit.com/r/htmx/comments/1ahb9mq/can_htmx_support_a_presigned_url_flow/)

[persist plugin for Alpine.js](https://alpinejs.dev/plugins/persist)

> Alpine's Persist plugin allows you to persist Alpine state across page loads.

> This is useful for persisting search filters, active tabs, and other features where users will be frustrated if their configuration is reset after refreshing or leaving and revisiting a page.

[How Alpine.js keeps track of x-data/state](https://codewithhugo.com/alpinejs-inspect-component-data-from-js/). [keeping layout state on the client](https://www.reddit.com/r/htmx/comments/1aizay4/keeping_layout_state_on_the_client/).

> The short story of how Alpine.js tracks component state (or “data”) is that when it initialises, it runs the content of x-data, wraps it in a proxy (which allows for reactive view updates) and stores it on the component’s root node.

[Where do you draw the line between doing something on the server vs. client?](https://www.reddit.com/r/htmx/comments/1ajcw51/where_do_you_draw_the_line_between_doing/). [master-detail page situation](https://www.reddit.com/r/htmx/comments/1ajbj13/question_about_master_detail_page_situation/). [Keeping layout state on the client](https://www.reddit.com/r/htmx/comments/1aizay4/keeping_layout_state_on_the_client/).

[client-side scripting](https://hypermedia.systems/client-side-scripting/)

[Just enough CORS to not get stuck](https://lobste.rs/s/gwlpuu/just_enough_cors_not_get_stuck)

[How I write HTTP services in Go after 13 years](https://news.ycombinator.com/item?id=39318867)

[A common case of needless state: Dialog visibility.](https://twitter.com/housecor/status/1756682543624077355)

[CORS-safelisted request header](https://developer.mozilla.org/en-US/docs/Glossary/CORS-safelisted_request_header)

[a bad idea: query params in cookie](https://twitter.com/t3dotgg/status/1758300512955560322)

> when I open a new tab to search for things on this site, it breaks the other tabs

[Easily add authentication for users to your website using Auth0](https://www.youtube.com/watch?v=KN80fZjjzpk). [100 things you can do on your personal website](https://jamesg.blog/2024/02/19/personal-website-ideas/).

[Alpine and CSPs](https://news.ycombinator.com/item?id=34366454)

[GET forms are awesome](https://twitter.com/ryanflorence/status/1759947521521041880?s=03)

[Vanilla JavaScript, Libraries, And The Quest For Stateful DOM Rendering](https://www.smashingmagazine.com/2024/02/vanilla-javascript-libraries-quest-stateful-dom-rendering/)

[I don't care how fast your servers are, don't ignore pending UI.](https://twitter.com/kentcdodds/status/1762554375900430797)

[use](https://twitter.com/kentcdodds/status/1762553022574645372)

[No Outer margin](https://kyleshevlin.com/no-outer-margin/)

[How Shadcn/ui ACTUALLY Works](https://www.youtube.com/watch?v=AqmMx_JidGo)

[htmx templating languages](https://twitter.com/david_syer/status/1771182660347412975)

[RFC 7578 - Returning Values from Forms: multipart/form-data](https://datatracker.ietf.org/doc/html/rfc7578#section-4.3)

[url with multiple forward slashes](https://stackoverflow.com/questions/10161177/url-with-multiple-forward-slashes-does-it-break-anything). [RFC3986](https://datatracker.ietf.org/doc/html/rfc3986).

[protocol deflation](https://twitter.com/myrrlyn/status/1782395245163876714)

[A relative reference that begins with a single slash character is termed an absolute-path reference.](https://webmasters.stackexchange.com/questions/56840/what-is-the-purpose-of-leading-slash-in-html-urls)

[No Abstractions: our API design principle](https://news.ycombinator.com/item?id=40161794)

[the problems of compiled languages for quick feedback while developing](https://twitter.com/htmx_org/status/1783916750339448900)

[TypeSpec: A new language for API-centric development](https://news.ycombinator.com/item?id=40206124)

[Service compatibility is determined based on policy](https://blog.ploeh.dk/2024/04/29/service-compatibility-is-determined-based-on-policy/).

[disadvantages of file-based routing](https://twitter.com/housecor/status/1784757498207154436)

[why your framework doesn't matter](https://news.ycombinator.com/item?id=40155294)

[avoid SDKs?](https://x.com/kentcdodds/status/1798018124769640492). [post](https://www.epicweb.dev/skip-sdks-in-simple-integrations)

[edge servers and databases](https://x.com/kentcdodds/status/1798798692843229588)

[Building a SaaS product with Htmx](https://news.ycombinator.com/item?id=40618841)

[datalist and options bug](https://x.com/htmx_org/status/1800580638644519361)

[HTMX drama](https://x.com/AdamRackis/status/1801291309107269904)

[The Life & Death of htmx](https://www.youtube.com/watch?v=inRB6ull5WQ)

[how to design complex tables](https://www.linkedin.com/pulse/how-design-complex-data-tables-figma-kits-vitaly-friedman-spaue/)

[the demise of the mildly dynamic website](https://news.ycombinator.com/item?id=40729671)

[HTMX and CSP](https://news.ycombinator.com/item?id=40855122)

[Django + Alpine.js + htmx Ups & Downs](https://www.youtube.com/watch?v=AVqjbUqT8ck)

[Following up "Mother of all htmx demos"](https://david.guillot.me/en/posts/tech/following-up-mother-of-all-htmx-demos/)

[Demystifying Cookies and Tokens](https://news.ycombinator.com/item?id=41033042)

[Third-party cookies have got to go](https://lobste.rs/s/hat2if/third_party_cookies_have_got_go)

[What we got wrong about HTTP imports](https://lobste.rs/s/vfnby3/what_we_got_wrong_about_http_imports)

[great URL design](https://news.ycombinator.com/item?id=41243992)

[CORS is Stupid](https://lobste.rs/s/98rp8f/cors_is_stupid)

[table sorting in HTMX](https://x.com/htmx_org/status/1827708511188640179)

[The Life & Death of htmx](https://www.youtube.com/watch?v=inRB6ull5WQ)

[the cost of JS-heavy frameworks](https://x.com/htmx_org/status/1825571929882816837)

[spas with TanStack](https://x.com/AdamRackis/status/1830069281146495267)

[ "fetch on render" vs "render as you fetch"](https://x.com/t3dotgg/status/1829988532489793957)

[web components and encapsulation](https://x.com/justinfagnani/status/1829949589153345564)

[htmx drama](https://x.com/code_department/status/1833477948676182408)

[Hypermedia Controls: From Feral to Formal](https://dl.acm.org/doi/pdf/10.1145/3648188.3675127)

[Who uses Accept-Language header?](https://news.ycombinator.com/item?id=41497139)

[htmx - Having trouble with how to structure the backend](https://www.reddit.com/r/htmx/comments/1fdrqnt/having_trouble_with_how_to_structure_the_backend/)

> The problem is when the user wants to navigate directly to a specific page. For example, if the user types "site.com/page/projects" into their browser, I then have to use a templating engine to pre-render the entire page and send it as one big chunk of HTML. In my current implementation, this leads to really messy code on the backend really fast, as I have to have two separate routes: one for the full webpage, and one for the snippet for HTMX to swap out. This also leads to some gross code duplication that I'd just rather not deal with.

[How to send partial form data back to user if validation fails?](https://www.reddit.com/r/htmx/comments/1fhy5ks/how_to_send_partial_form_data_back_to_user_if/)

[all local](https://x.com/BHolmesDev/status/1835437914479841744)

[Analyzing the OpenAPI Tooling Ecosystem](https://news.ycombinator.com/item?id=41612002)

[PerformanceObserver](https://x.com/kentcdodds/status/1837633389475909716)

[All my projects are published to CDNs because most of them don't require a real server.](https://x.com/nullvoxpopuli/status/1837499779514835216)

[Building a robust frontend using progressive enhancement](https://news.ycombinator.com/item?id=41686715). [Do not build your Gov.uk service as a single-page application](https://news.ycombinator.com/item?id=41686715)

[web components are not the future](https://lobste.rs/s/1jj1er/web_components_are_not_future)

[REST API design pitfalls](https://speakerdeck.com/victorrentea/rest-api-design-pitfalls)

[fast site](https://x.com/ethanniser/status/1848442717925171658)

[You Can't Build Interactive Web Apps Except as Single Page Applications... And Other Myths](https://htmx.org/essays/you-cant/). [HN](https://news.ycombinator.com/item?id=42164154).

[Handling cookies is a minefield](https://news.ycombinator.com/item?id=42206556)

[to slash or not to slash](https://developers.google.com/search/blog/2010/04/to-slash-or-not-to-slash). [RESTful URI trailing slash or no trailing slash](https://stackoverflow.com/questions/61547014/restful-uri-trailing-slash-or-no-trailing-slash)

```
The following urls:

http://example/foo
http://example/foo/
Are NOT the same url. Caches will store them separately. So in that sense there is a real difference. Normalizing URLs will not strip them.
```

```
/users/
This URI has a path /users/ which includes two segments: "users" and an empty segment.
```

[lots of little html pages](https://lobste.rs/s/csr4mw/building_websites_with_lots_little_html)

[Why Do We Have a Cache-Control Request Header?](https://csswizardry.com/2025/03/why-do-we-have-a-cache-control-request-header/)

[cache rules everything about me](https://speakerdeck.com/csswizardry/cache-rules-everything). [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Reference/Headers/Cache-Control).




