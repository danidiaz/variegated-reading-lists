[Templating in HTML](https://twitter.com/KittyGiraudel/status/1575815588047253504)

[learn forms](https://web.dev/learn/forms/)

[How to Build a Personal Webpage from Scratch](https://rutar.org/writing/how-to-build-a-personal-webpage-from-scratch/). [HN](https://news.ycombinator.com/item?id=33017056).

[WASM, why?](https://twitter.com/mattaningram/status/1576012476365557760). [another tweet](https://twitter.com/simonw/status/1576001019296636928)

[<dialog> on MDN](https://developer.mozilla.org/en-us/docs/web/html/element/dialog). [HTML spec](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-dialog-element). [DOM interface](https://html.spec.whatwg.org/multipage/interactive-elements.html#the-dialog-element) 

[HTML living standard](https://html.spec.whatwg.org/multipage/)

[innerText](http://perfectionkills.com/the-poor-misunderstood-innerText/)

[openapi 3.1](https://spec.openapis.org/oas/v3.1.0)

    - [path item object](https://spec.openapis.org/oas/v3.1.0#pathItemObject)

      > In case a Path Item Object field appears both in the defined object and the referenced object, the behavior is undefined. See the rules for resolving Relative References.

    - [schema object](https://spec.openapis.org/oas/v3.1.0#schemaObject)

[The hidden depths of the input element](https://lobste.rs/s/iq3wbg/hidden_depths_input_element)

[Building a Good Download… Button?](https://css-tricks.com/building-good-download-button/). [Links vs. Buttons in Modern Web Applications
(2016)](https://marcysutton.com/links-vs-buttons-in-modern-web-applications)

> the whole purpose of a link has always been to download content.

> Buttons perform actions, but they don’t inherently “get” documents. While they can be used to get data, it’s often to change state of a current document, not to retrieve and render a new one. They can get data, in regards to the functionality of forms, but it continues to be within the context of updating a web document, not downloading an individual file.

> Long story short, the download attribute is unique to anchor links for a reason. download augments the inherent functionality of the link retrieving data. It side steps the attempt to render the file in the browser and instead says, “You know what? I’m just going to save this for later…”

[What are pros/cons of using buttons instead of plain links to download a document?](https://ux.stackexchange.com/questions/140744/what-are-pros-cons-of-using-buttons-instead-of-plain-links-to-download-a-documen)

[HTML Templates Instead of Reactivity](https://guseyn.com/html/posts/templates-instead-of-reactivity.html)

[Downloading files from Ajax POST Requests](https://stackoverflow.com/a/67004804/1364288)

[parts of an URL](https://web.dev/articles/url-parts)

[A Button Per form or One Form with Multiple Buttons](https://kentcdodds.com/calls/04/33/a-button-per-form-or-one-form-with-multiple-buttons). [spotify](https://open.spotify.com/episode/1WvzOGnSSN7GGQiAHnhde7)

[footer](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/footer). [sectioning content](https://developer.mozilla.org/en-US/docs/Web/HTML/Content_categories#sectioning_content). [from the spec](https://www.w3.org/TR/2010/WD-html5-20101019/content-models.html#sectioning-content-0). [Is it ok to have section tag within footer tag in HTML5?](https://stackoverflow.com/questions/25945068/is-it-ok-to-have-section-tag-within-footer-tag-in-html5).

> represents a footer for its nearest ancestor sectioning content or sectioning root element

> Sectioning content, a subset of flow content, creates a section in the current outline defining the scope of <header> and <footer> elements.

> <section> can be a descendant of <footer>, however <header>, <footer>, and <main> cannot.

[main doesn't seem to be sectioning content!](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/main). [why <main> tag of html is not a sectioning content but <aside> is](https://stackoverflow.com/questions/59762687/why-main-tag-of-html-is-not-a-sectioning-content-but-aside-is)

> Content categories Flow content, palpable content.

> The content of a <main> element should be unique to the document. Content that is repeated across a set of documents or document sections such as sidebars, navigation links, copyright information, site logos, and search forms shouldn't be included unless the search form is the main function of the page.

[header element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/header)

> The <header> element has an identical meaning to the site-wide banner landmark role, unless nested within sectioning content. Then, the <header> element is not a landmark.

> Otherwise, it is a section in the accessibility tree, and usually contains the surrounding section's heading (an h1 – h6 element) and optional subheading, but this is not required.

[HTML 5: When to use <article>, <aside>, <section> & <DIV>](https://www.sitepoint.com/community/t/html-5-when-to-use-article-aside-section-div/5742)

[article element](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/article). [spec](https://www.w3.org/TR/2011/WD-html5-author-20110809/the-article-element.html). [article vs section](https://www.smashingmagazine.com/2022/07/article-section-elements-accessibility/). [more](https://www.smashingmagazine.com/2020/01/html5-article-section/).

> A given document can have multiple articles in it; for example, on a blog that shows the text of each article one after another as the reader scrolls, each post would be contained in an <article> element, possibly with one or more <section>s within.

> When an <article> element is nested, the inner element represents an article related to the outer element. For example, the comments of a blog post can be <article> elements nested in the <article> representing the blog post.

[section element in the HTML living standard](https://html.spec.whatwg.org/#the-section-element)

[cancelling events with `preventDefault`](https://developer.mozilla.org/en-US/docs/Web/API/Event/cancelable). [cancel event (not the same thing)](https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/cancel_event)

[indeterminate state checkboxes](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/input/checkbox#indeterminate_state_checkboxes). [css tricks](https://css-tricks.com/indeterminate-checkboxes/). [example helper library](https://npm.io/package/select_all).

> In addition to the checked and unchecked states, there is a third state a checkbox can be in: indeterminate. This is a state in which it's impossible to say whether the item is toggled on or off. This is set using the HTMLInputElement object's indeterminate property via JavaScript (it cannot be set using an HTML attribute)

> There are not many use cases for this property. The most common is when a checkbox is available that "owns" a number of sub-options (which are also checkboxes). If all of the sub-options are checked, the owning checkbox is also checked, and if they're all unchecked, the owning checkbox is unchecked. If any one or more of the sub-options have a different state than the others, the owning checkbox is in the indeterminate state.

> The indeterminate state is visual only. The checkbox is still either checked or unchecked as a state. That means the visual indeterminate state masks the real value of the checkbox, so that better make sense in your UI!

[Web APIs](https://developer.mozilla.org/en-US/docs/Web/API)

[matching event listeners for removal](https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/removeEventListener#matching_event_listeners_for_removal)

[boolean attributes](https://developer.mozilla.org/en-US/docs/Glossary/Boolean/HTML)

[Introduction to events](https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Building_blocks/Events). [event handling attributes](https://developer.mozilla.org/en-US/docs/Web/HTML/Attributes#event_handler_attributes).

> The earliest method of registering event handlers found on the Web involved event handler HTML attributes (or inline event handlers) like the one shown above — the attribute value is literally the JavaScript code you want to run when the event occurs. 

> You can find HTML attribute equivalents for many of the event handler properties; however, you shouldn't use these — they are considered bad practice. It might seem easy to use an event handler attribute if you are doing something really quick, but they quickly become unmanageable and inefficient.

> All event handler attributes accept a string. The string will be used to synthesize a JavaScript function like function name(/*args*/) {body}, where name is the attribute's name, and body is the attribute's value. The handler receives the same parameters as its JavaScript event handler counterpart — most handlers receive only one event parameter

[Why you should say HTML classes, CSS class selectors, or CSS pseudo-classes, but not CSS classes](https://tantek.com/2012/353/b1/why-html-classes-css-class-selectors)

[vertical form controls](https://news.ycombinator.com/item?id=39757394)

[demystifying the shadow DOM](https://news.ycombinator.com/item?id=39967685)

[popovertarget](https://twitter.com/jdevalk/status/1780511519941300474)

[Page Structure Tutorial](https://www.w3.org/WAI/tutorials/page-structure/)

[HTML attributes vs DOM properties](https://jakearchibald.com/2024/attributes-vs-properties/). [HN](https://news.ycombinator.com/item?id=40152682).

> Attributes serialise to HTML, whereas properties don't

[Switching It Up With HTML’s Latest Control](https://www.smashingmagazine.com/2024/05/switching-it-up-html-latest-control/)

[the basics](https://thebasics.dev/)

[Custom HTML Has Levels To It](https://unplannedobsolescence.com/blog/custom-html-has-levels/)

[microfeatures in blogs](https://lobste.rs/s/ju9yby/microfeatures_i_love_blogs_personal)

[HTML5 Differences from HTML4 (2014)](https://news.ycombinator.com/item?id=40887480)

[the UX of HTML](https://news.ycombinator.com/item?id=41310921)

[Hypermedia Controls: Feral to Formal](https://dl.acm.org/doi/10.1145/3648188.3675127)

[insertAdjacentHTML](https://x.com/WebReflection/status/1829556513469321564)

[web components. yay or nay?](https://x.com/JLarky/status/1830283524760621456). [reddit](https://www.reddit.com/r/reactjs/comments/1fjhxte/are_you_using_web_componentsor_have_you_given_up/).

[web components are ok](https://nolanlawson.com/2024/09/28/web-components-are-okay/). [hn](https://news.ycombinator.com/item?id=41686722).

[Make Your Own Website](https://web.pixelshannon.com/make/). [hn](https://news.ycombinator.com/item?id=43008315).

[remove tags from HEAD](https://lobste.rs/s/hnqkhk/remove_these_tags_from_head)

[plain vanilla web](https://plainvanillaweb.com/index.html)

[The Server Doesn't Render Anything](https://unplannedobsolescence.com/blog/the-server-doesnt-render/). [Who's Afraid of a Hard Page Load?](https://unplannedobsolescence.com/blog/hard-page-load/). [word](https://unplannedobsolescence.com/blog/why-insist-on-a-word/).

[list vs. table](https://ux.stackexchange.com/questions/119962/confused-with-what-to-use-list-vs-table). [more](https://stackoverflow.com/questions/51636238/confused-with-what-to-use-list-vs-table).

[breakpoints directly on DOM elements](https://www.youtube.com/shorts/NqCFDLr5sJE)

[Just fucking use HTML](https://justfuckingusehtml.com/)

[The <output> Tag](https://news.ycombinator.com/item?id=45547566). [hn](https://news.ycombinator.com/item?id=45547566).

[<selectedcontent>](https://www.youtube.com/watch?v=tNBufpGQihY)

[A modern approach to preventing CSRF in Go](https://news.ycombinator.com/item?id=45581288)

[Marko](https://news.ycombinator.com/item?id=45858905)

[W3C—Tables with Multi-Level Headers](https://www.w3.org/WAI/tutorials/tables/multi-level/). [the spec](https://www.w3.org/TR/html401/struct/tables.html#edef-THEAD)

> Table rows may be grouped into a table head, table foot, and one or more table body sections, using the THEAD, TFOOT and TBODY elements, respectively. 

[always plan](https://hanlho.com/p/implementing-an-urgent-feature-with-llms-and-zed/).

[DOMContentLoaded event](https://developer.mozilla.org/en-US/docs/Web/API/Document/DOMContentLoaded_event)

> A different event, load, should be used only to detect a fully-loaded page. It is a common mistake to use load where DOMContentLoaded would be more appropriate.

[Replacing JS with just HTML](https://www.htmhell.dev/adventcalendar/2025/27/). [hn](https://news.ycombinator.com/item?id=46407337).

> > Or you use HTMX... and you still end up with just as many (partial) views, but now with so much implicit state that you're veering into write-only code.

> You're overthinking htmx then. I do some fairly complex stuff with no extra partials. Trick is just always rerender and use hx-select and hx-target to slice out the bits you want to update on the current page.

[Targeting by Reference in the Shadow DOM](https://meyerweb.com/eric/thoughts/2025/12/19/targeting-by-reference-in-the-shadow-dom/)


