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


