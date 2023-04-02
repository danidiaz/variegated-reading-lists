Stuff about testing persistence repositories

https://softwareengineering.stackexchange.com/questions/301479/are-database-integration-tests-bad
https://softwareengineering.stackexchange.com/questions/185326/why-do-i-need-unit-tests-for-testing-repository-methods
https://softwareengineering.stackexchange.com/questions/348661/should-i-use-a-layer-between-service-and-repository-for-a-clean-architecture-s
https://softwareengineering.stackexchange.com/questions/111193/hooking-up-a-business-layer-and-repository-using-unit-of-work-pattern?rq=1
https://softwareengineering.stackexchange.com/questions/294561/repository-pattern-with-service-layer-too-much-separation?rq=1
https://softwareengineering.stackexchange.com/questions/282033/how-do-you-scale-your-integration-testing/283067#283067
https://softwareengineering.stackexchange.com/a/283067/76774 fake repositories.
https://www.baeldung.com/spring-boot-testing
https://grokonez.com/testing/datajpatest-with-spring-boot

> By default, @DataJpaTest will configure an in-memory embedded database, scan for @Entity classes and configure Spring Data JPA repositories. It is also transactional and rollback at the end of each test. 

https://blog.philipphauer.de/dont-use-in-memory-databases-tests-h2/ https://www.baeldung.com/spring-testing-separate-data-source https://www.baeldung.com/spring-jpa-test-in-memory-database https://medium.com/@joeclever/integration-testing-multiple-datasources-in-spring-boot-and-spring-data-with-spock-f88e1428ce9f https://medium.com/@harittweets/how-to-connect-to-h2-database-during-development-testing-using-spring-boot-44bbb287570 https://vladmihalcea.com/how-to-run-database-integration-tests-20-times-faster/ https://memorynotfound.com/unit-test-jpa-junit-in-memory-h2-database/ https://stackoverflow.com/questions/42943447/spring-boot-integration-test-with-h2-inmemory-database 

[In-memory database tests with Querydsl](https://dev.to/brightdevs/in-memory-database-tests-with-querydsl-1mij)

> Fortunately the EntityQueries abstraction is very easy to implement using POJO in-memory collections.

[Test Doubles — Fakes, Mocks and Stubs](https://blog.pragmatists.com/test-doubles-fakes-mocks-and-stubs-1a7491dfa3da)

> Fakes are objects that have working implementations, but not same as production one. Usually they take some shortcut and have simplified version of production code.

> An example of this shortcut, can be an in-memory implementation of Data Access Object or Repository. This fake implementation will not engage database, but will use a simple collection to store data. This allows us to do integration test of services without starting up a database and performing time consuming requests.

[Testing Real Repositories](https://stackoverflow.com/questions/1501385/testing-real-repositories). [When unit testing, do you have to use a database to test CRUD operations?](https://stackoverflow.com/questions/1484542/when-unit-testing-do-you-have-to-use-a-database-to-test-crud-operations). [Data Access Component Testing Redux](https://blogs.msdn.microsoft.com/ploeh/2008/01/31/data-access-component-testing-redux/).

> The most important thing to keep in mind is to avoid the temptation to create a General Fixture with some 'representative data' and attempt to reuse this across all tests. Instead, you should fill in data as part of each test and clean it up after.

https://news.ycombinator.com/item?id=18740246 Turning GraphQL diagrams to mock back end

[farewell to fsync](https://pythonspeed.com/articles/faster-db-tests/). [lobsters](https://lobste.rs/s/urhsse/farewell_fsync_10x_faster_database_tests).

[verified fakes](https://pythonspeed.com/articles/verified-fakes/)

[From interaction-based to state-based testing](http://blog.ploeh.dk/2019/02/18/from-interaction-based-to-state-based-testing/). [mocks for commands, stubs for queries](http://blog.ploeh.dk/2013/10/23/mocks-for-commands-stubs-for-queries/). [State vs Interaction Based Testing](http://natpryce.com/articles/000342.html). [An example of interaction-based testing in C#](http://blog.ploeh.dk/2019/02/25/an-example-of-interaction-based-testing-in-c/).

[property-based testing](https://wickstrom.tech/programming/2019/03/02/property-based-testing-in-a-screencast-editor-introduction.html). [Building on developers' intuitions to create effective property-based tests](https://www.youtube.com/watch?v=NcJOiQlzlXQ&list=PLvL2NEhYV4ZvCRCVlXTfB6-d09K3r0Sxa&index=5).

[don'w write tests](https://www.youtube.com/watch?v=hXnS_Xjwk2Y). [Find the best properties for Property Based Testing](https://medium.com/@nicolasdubien/find-the-best-properties-for-property-based-testing-ee2ed9d442e1). [Introduction to Property Based Testing](https://medium.com/criteo-labs/introduction-to-property-based-testing-f5236229d237). [Building on developers' intuitions](https://www.youtube.com/watch?v=NcJOiQlzlXQ)

[testing in production](https://www.youtube.com/watch?v=nIlFmja65_g). [Testing in Production, the safe way](https://medium.com/@copyconstruct/testing-in-production-the-safe-way-18ca102d0ef1).

[JUnit 5: The Next Step in Automated Testing](https://www.infoq.com/presentations/junit-5-automated-testing).

[about consumer-driven contracts](https://twitter.com/BootifulPodcast/status/1124384142269882369)

[Nicolas Frankel on application security, integration testing, Kotlin and more](https://soundcloud.com/a-bootiful-podcast/nicolas-frankel-on-application-security-integration-testing-kotlin-and-more)



[Hypothesis for web developers](https://web.hypothes.is/blog/hypothesis-for-web-developers/). [tweet](https://twitter.com/michaelbolton/status/1124433787188928517).

[80% CODE COVERAGE IS NOT ENOUGH](http://adambien.blog/roller/abien/entry/80_code_coverage_is_not).

[Integrated versus Manual Shrinking](https://www.reddit.com/r/haskell/comments/bo1m53/new_blog_post_integrated_versus_manual_shrinking/)

(State machine testing - LambdaJam 2018)[https://twitter.com/Jose_A_Alonso/status/1129325840662224902].

[Testing Java Microservices: From Development to Production](https://www.youtube.com/watch?v=V80MztOCCjo)

[nines](https://twitter.com/tacertain/status/1132391299733000193)

[cloud native observability](https://speakerdeck.com/tylertreat/cloud-native-observability)

[test data generation with faker](https://www.tonic.ai/post/how-to-generate-simple-test-data-with-faker/)

[docker for integration tests](https://twitter.com/_JamesWard/status/1139550763246481410)

[most unit testing is a waste](https://news.ycombinator.com/item?id=20309815)

> storybook and react-testing

[How to Specify it! A Guide to Writing Properties of Pure Functions](https://www.dropbox.com/s/tx2b84kae4bw1p4/paper.pdf?dl=0)

> This is the most obvious approach to writing properties—to replicate the implementation in the test code—and it is deeply unsatisfyin

[Real World Scenario Testing using Azure DevOps and automated UI tests](https://channel9.msdn.com/Shows/DevOps-Lab/Real-World-Scenario-Testing-using-Azure-DevOps-and-automated-UI-tests)

[test telemetry](https://twitter.com/copyconstruct/status/1154204037518020608). [event log](https://twitter.com/SamirTalwar/status/1154315503592235013)

[state machine testing with Hedgehog](https://github.com/qfpl/state-machine-testing-course). [scala](https://twitter.com/charlesofarrell/status/1172009394315202560)

[Hedgehog vs Quickcheck](https://twitter.com/rob_rix/status/1157350511034675201)

[GOTO 2019 • Millisecond Full Stack Acceptance Tests • Aslak Hellesøy](https://www.reddit.com/r/programming/comments/d2qvch/goto_2019_millisecond_full_stack_acceptance_tests/)

[runtime monitoring](https://twitter.com/mfeathers/status/1172880333076713472)

[Better Integration Tests for Performance Monitoring](https://www.youtube.com/watch?v=j0PJhD5XNJ8&feature=youtu.be)

[Thoughts on efficient enterprise testing (1/6)](https://blog.sebastian-daschner.com/entries/thoughts-on-efficient-testing). [2](https://blog.sebastian-daschner.com/entries/thoughts-on-efficient-testing-unit).

[tests that touch files](https://twitter.com/MarcJBrooker/status/1175105839440355328)

[Testing in Production: the hard parts](https://twitter.com/copyconstruct/status/1178194135729070080)

[testing sql](https://twitter.com/lukaseder/status/1196122412833787909)

> We have a ton of unit tests covering expected API/parser/renderer input/output pairs, but most functionality is covered in ~1000 integration tests running ~20k SQL queries against each supported RDBMS, mostly in-memory or Docker, sometimes VMWare run database instances.

[Automation testing is not working](https://www.reddit.com/r/programming/comments/dya8dd/automation_testing_is_not_working/) disagree

[Testing Microservices, the sane way](https://medium.com/@copyconstruct/testing-microservices-the-sane-way-9bb31d158c16)

[Conventional wisdom says you need a comprehensive set of regression tests to go green before you release code](https://twitter.com/sarahmei/status/868928631157870592)

[Time zone integration testing life hack](https://twitter.com/gunnarmorling/status/1430445009350823939)

[Why We Killed Our End-to-End Test Suite](https://building.nubank.com.br/why-we-killed-our-end-to-end-test-suite/). [hn](https://news.ycombinator.com/item?id=28643848)

[The fundamentals of testing with persistence layers](https://twitter.com/InfoQ/status/1447534118523318274)

[One should be careful about these mega-interfaces that define an entire subsystem of your application (DB in this case)](https://news.ycombinator.com/item?id=29314941). [rant](https://github.com/golang/go/wiki/CodeReviewComments#interfaces).

[cleaning the database or not](https://news.ycombinator.com/item?id=29764792)

[Backtracking Generators for Random Testing](https://www.youtube.com/watch?v=dfZ94N0hS4I). [Generating Good Generators for Inductive Relations](https://zoep.github.io/GeneratingGoodGenerators.pdf). [Random Testing For Language Design](https://repository.upenn.edu/cgi/viewcontent.cgi?article=4665&context=edissertations). 

[SmallCheck and Lazy SmallCheck](https://www.cs.york.ac.uk/fp/smallcheck/smallcheck.pdf).

[The Design and Use of QuickCheck](https://begriffs.com/posts/2017-01-14-design-use-quickcheck.html). 

[Shrinking and showing functions (pearl)](https://dl.acm.org/doi/10.1145/2430532.2364516). [video](https://www.youtube.com/watch?v=CH8UQJiv9Q4).

[a case study on correctness and safety testing of stateful systems](https://www.tweag.io/blog/2022-01-26-property-based-testing-of-monadic-code/)

[QuickCheck, Hedgehog, Validity](https://www.fpcomplete.com/blog/quickcheck-hedgehog-validity/) 

[compiler test framework](https://twitter.com/wilbowma/status/1488733730495631364)

[When Behaviour Driven Development Goes WRONG!](https://www.youtube.com/watch?v=YAZr3LsCzn0)

> Confusing UI interactions with behavior.

[file-driven testing in Go](https://lobste.rs/s/sgk1nn/file_driven_testing_go)

[How do you supply a ClockProvider to Spring v5 (Spring Boot v2)?](https://stackoverflow.com/questions/48335736/how-do-you-supply-a-clockprovider-to-spring-v5-spring-boot-v2)

[Testing with Spring Boot's @TestConfiguration Annotation](https://reflectoring.io/spring-boot-testconfiguration/)

[Spring Boot: @TestConfiguration Not Overriding Bean During Integration Test](https://stackoverflow.com/questions/50607285/spring-boot-testconfiguration-not-overriding-bean-during-integration-test)

[ArgumentMatchers (Mockito 2.2.7 API)](https://site.mockito.org/javadoc/current/org/mockito/ArgumentMatchers.html)

[Mockito Argument Matchers - any(), eq()](https://www.journaldev.com/21876/mockito-argument-matchers-any-eq)

[Injecting Mockito Mocks in to Spring Beans](https://www.baeldung.com/injecting-mocks-in-spring)

[Overriding beans in Integration tests](https://stackoverflow.com/questions/35742920/overriding-beans-in-integration-tests)

[Mockito.mock() vs @Mock vs @MockBean](https://www.baeldung.com/java-spring-mockito-mock-mockbean)

[Getting Started with Mockito @Mock, @Spy, @Captor and @InjectMocks](https://www.baeldung.com/mockito-annotations)

[Difference between @Mock, @MockBean and Mockito.mock()](https://stackoverflow.com/questions/44200720/difference-between-mock-mockbean-and-mockito-mock)

[Spring Boot testing](https://docs.spring.io/spring-boot/docs/current/reference/html/features.html#features.testing)

> JUnit 5, AssertJ, Hamcrest, Mockito, JSONassert, JsonPath

[Spring Boot Wiremock](https://wiremock.org/docs/spring-boot/)

> One of the major advantages of dependency injection is that it should make your code easier to unit test. You can instantiate objects by using the new operator without even involving Spring. You can also use mock objects instead of real dependencies.

> Often, you need to move beyond unit testing and start integration testing (with a Spring ApplicationContext). It is useful to be able to perform integration testing without requiring deployment of your application or needing to connect to other infrastructure.

[os-fuzz](https://twitter.com/argoproj/status/1498407699867860994)

[Unit testing - 9 design hints](https://www.slideshare.net/VictorRentea/unit-testing-9-design-hints)

[Still No Consensus On Testing Private Methods](https://lobste.rs/s/llx1s6/still_no_consensus_on_testing_private)

[Testing an application with a network delay](https://lobste.rs/s/6s8jyp/testing_application_with_network_delay)

[It Doesn't Have to Be Arbitrary](https://tech.freckle.com/2022/04/07/it-doesnt-have-to-be-arbitrary/)

[The class on Argentian Tango was full](https://twitter.com/Bennett_AWOL/status/1514995060089176074)

[Acceptance Testing | Webinar](https://www.youtube.com/watch?v=SuDIYk9GBpE). [Acceptance Testing with Executable Specifications](https://www.youtube.com/watch?v=knB4jBafR_M).

[Introduction to Doctests in Haskell](https://www.reddit.com/r/haskell/comments/u70c4c/introduction_to_doctests_in_haskell/)

[testing microservices is hard](https://twitter.com/danielbryantuk/status/1517444565908611074)

[teaching debugging](https://twitter.com/wilcoxjay/status/1525176943523508224)

[Don’t mock what you don’t own](https://news.ycombinator.com/item?id=31822683)

[Testing in production as a major service is safe if you deploy your services in isolated cells with a reasonable blast radius.](https://twitter.com/rakyll/status/1562860808081530880)
    
[Playwright now has new APIs inspired by Testing Library](https://twitter.com/diegohaz/status/1578567655493193728). [tag](https://github.com/microsoft/playwright/releases/tag/v1.27.0). [guiding principles for Testing Library](https://testing-library.com/docs/guiding-principles).    

[no to snapshot tests](https://twitter.com/ksylor/status/1578503924218482688)

[ Mathematics of debugging a Haskell program](https://www.youtube.com/watch?v=b02ce8oKnNY&list=PLxxF72uPfQVRQXih84omWRmacz1lwejc6&index=4)

[Playwright Your Next Java Test Framework for automating Web tests](https://www.youtube.com/watch?v=9rVKe5vjVTs)

[Don’t Do E2E Testing](https://www.youtube.com/watch?v=QFCHSEHgqFE)

[Testing Without Mocks: A Pattern Language](https://lobste.rs/s/y9xf6i/testing_without_mocks_pattern_language)

[How to Test](https://matklad.github.io/2021/05/31/how-to-test.html). [Unit and Integration Tests](https://matklad.github.io/2022/07/04/unit-and-integration-tests.html).

[Load Testing Crash Course with Gatling](https://www.youtube.com/watch?v=RiM1GsVSbzM)

[Don’t Do E2E Testing!](https://www.youtube.com/watch?v=QFCHSEHgqFE). [wiremock](https://wiremock.org/).

[Efficient and Flexible Model-Based Testing](https://concerningquality.com/model-based-testing-theory/)

[Microservices Integration Done Right Using Contract-Driven Development](https://www.infoq.com/articles/contract-driven-development/)

[doctests](https://discourse.haskell.org/t/doctests-as-test-suite-without-custom-builds/5771/2)

[fault injection](https://github.com/stevana/property-based-testing-stateful-systems-tutorial/blob/921d7cb02735e006d9071c1c5b859f5a921e2427/docs/Part04FaultInjection.md)

[WireMock request matching](https://wiremock.org/docs/request-matching/). [stateful behavior](https://wiremock.org/docs/stateful-behaviour/)

> WireMock supports state via the notion of scenarios. A scenario is essentially a state machine whose states can be arbitrarily assigned. It starting state is always Scenario.STARTED. Stub mappings can be configured to match on scenario state, such that stub A can be returned initially, then stub B once the next scenario state has been triggered.

[XPath: difference between dot and text()](https://stackoverflow.com/questions/38240763/xpath-difference-between-dot-and-text). [string value](https://www.w3.org/TR/1999/REC-xpath-19991116/#dt-string-value)

[Testing text() nodes vs string values in XPath](https://stackoverflow.com/questions/34593753/testing-text-nodes-vs-string-values-in-xpath) good answer

[XPath in Selenium: How to Find & Write? (Text, Contains, AND)](https://www.guru99.com/xpath-selenium.html)

[memfd-create it's very handy for creating "mock" files in C when you need to](https://www.reddit.com/r/haskell/comments/120a3qt/comment/jdghgzz/)

[Basics of XPath](https://courses.ischool.berkeley.edu/i290-14/s05/lecture-4/allslides.html). [How can I find an element by CSS class with XPath?](https://stackoverflow.com/questions/1604471/how-can-i-find-an-element-by-css-class-with-xpath). [How to select first and last elements via XPath?](https://stackoverflow.com/questions/36415455/how-to-select-first-and-last-elements-via-xpath). [Difference between contains() predicate testing in XPath?](https://stackoverflow.com/questions/43048863/difference-between-contains-predicate-testing-in-xpath). 

> ../name parent::name
> name child::name
> //name descendant::name
> .  self::node()
> * child::*
> @* attribute::*
> @name attribute::name

[If double slash (//) is used 2 times in XPath, what does it mean?](https://stackoverflow.com/questions/36019544/if-double-slash-is-used-2-times-in-xpath-what-does-it-mean). [spec](https://www.w3.org/TR/1999/REC-xpath-19991116/). [Does Chrome use XPath 2.0? (no)](https://stackoverflow.com/questions/25455351/does-chrome-use-xpath-2-0). 

[abbreviated syntax](https://www.w3.org/TR/1999/REC-xpath-19991116/#path-abbrev)

> The most important abbreviation is that child:: can be omitted from a location step. In effect, child is the default axis. For example, a location path div/para is short for child::div/child::para.

> There is also an abbreviation for attributes: attribute:: can be abbreviated to @. For example, a location path para[@type="warning"] is short for child::para[attribute::type="warning"] and so selects para children with a type attribute with value equal to warning.

> // is short for /descendant-or-self::node()/. For example, //para is short for /descendant-or-self::node()/child::para and so will select any para element in the document (even a para element that is a document element will be selected by //para since the document element node is a child of the root node); div//para is short for div/descendant-or-self::node()/child::para and so will select all para descendants of div children.

> NOTE: The location path //para[1] does not mean the same as the location path /descendant::para[1]. The latter selects the first descendant para element; the former selects all descendant para elements that are the first para children of their parents.

> a node-set is true if and only if it is non-empty

[CSS Selector vs XPath: Your Pocket Cheat Sheet](https://testrigor.com/blog/css-selector-vs-xpath-your-pocket-cheat-sheet/)

> XPath also has predicates (always embedded in square brackets), that you can use to find any specific node, or a node with a certain value.

> /audio/file[position()>4]

[puppeteer wait for element disappear or remove from DOM](https://stackoverflow.com/questions/58833640/puppeteer-wait-for-element-disappear-or-remove-from-dom)

[Vitest](https://twitter.com/TkDodo/status/1639708582546493441)    

[don't mock entities or DTOs](https://twitter.com/maciejwalkowiak/status/1642060780999790593)

[Verifying requests in WireMock](https://wiremock.org/docs/verifying/)

> Verifying and querying requests relies on the request journal, which is an in-memory log of received requests. This can be disabled for load testing

[WireMock state machines - Google Groups]

> WM has a state machine per scenario, so it sounds like each team may be creating overlapping scenario names

[Wiremock studio](https://wiremock.org/studio/docs/)

> WireMock Studio has now been discontinued. Please check out WireMock Cloud instead.

[Wiremock Cloud](https://www.wiremock.io/)

> Build and test when the APIs you need aren't ready or stable

> Stable development against unstable 3rd party APIs

> Simulate edge cases and faults

> Eliminate unexpected performance testing bills

[Simulating faults on Wiremock](https://wiremock.org/docs/simulating-faults/)

> One of the main reasons it’s beneficial to use web service fakes when testing is to inject faulty behaviour that might be difficult to get the real service to produce on demand. 

[Revving up Continuous Integration with Parallel Testing](https://semaphoreci.com/blog/revving-up-continuous-integration-with-parallel-testing). [Test splitting and parallelism in Circle CI](https://circleci.com/docs/parallelism-faster-jobs/). [in Buildkite](https://buildkite.com/screencasts/parallel-testing) [more Buildkite](https://buildkite.com/docs/tutorials/parallel-builds)

> parallelism is an attribute on a single command step which causes it to be split into many jobs. Those jobs will be the same except for having a parallel index and count. They share the same dependencies and agent tags.

> Knapsack is a ruby gem for automatically dividing your tests between parallel jobs, as well as making sure each job runs in comparable time.

[Test splitting / sharding in Vitest](https://vitest.dev/guide/cli.html)

> https://vitest.dev/guide/cli.html#shard

[Using Testing Library with implicit ARIA roles](https://rafaelcamargo.com/blog/using-testing-library-with-implicit-aria-roles/). [ARIA selectors in Puppeteer](https://developer.chrome.com/blog/puppetaria/). [API](https://pptr.dev/guides/query-selectors#aria-selectors-aria). [useful video](https://www.youtube.com/watch?v=C_AYpwbZ1N4). [4 Implicit WAI-ARIA Semantics](https://www.w3.org/TR/wai-aria-1.2/#implicit_semantics)

> In case you are considering making those implicit role values explicit by setting aria-role attributes to those elements, be aware it is not recommended.

> If you have worked on a puppeteer project before you most likely ran into a problem that your selector no longer works. This could be caused by change in the DOM structure or dynamically generated classes. DOM structure changes too often when new features or fixes are introduced.

> Instead of queering elements by CSS or XPath, you could use the aria selector and query with accessible name.

> These host language features can be viewed as having "implicit WAI-ARIA semantics". User agent processing of features with implicit WAI-ARIA semantics would be similar to the processing for the WAI-ARIA feature. The processing might not be identical because of lexical differences between the host language feature and the WAI-ARIA feature, but generally the user agent would expose the same information to the accessibility API.

[WAI-ARIA Roles](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Roles)

> ARIA roles can be used to describe elements that don't natively exist in HTML or exist but don't yet have full browser support.

[aria-labelledby](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-labelledby). [official docs](https://w3c.github.io/accname/#dfn-accessible-name).

> Some elements get their accessible name from their inner content. For example, the accessible name for a <button>, <a>, or <td> comes from the text between the opening and closing tags. Other elements, such as form <textarea>, <fieldset>, and <table> get their accessible name from the content of associated elements; for these elements, the accessible name comes from the <label> with a for attribute, <legend>, and <caption> respectively.

[ARIA states and properties](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes).

[Radix UI Popover Adheres to the Dialog WAI-ARIA design pattern.](https://www.radix-ui.com/docs/primitives/components/popover#accessibility). [aria patterns](https://www.w3.org/WAI/ARIA/apg/patterns/)

[aria-hidden](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Attributes/aria-hidden)

> aria-hidden="true" should not be added when:

> The HTML hidden attribute is present
> The element or the element's ancestor is hidden with display: none
> The element or the element's ancestor is hidden with visibility: hidden
> In all three scenarios, the attribute is unnecessary to add because the element has already been removed from the accessibility tree. Visually hiding elements with display or visibility hides content from the screen and from assistive technologies.
 
> Visually hiding elements with display or visibility hides content from the screen and from assistive technologies. [useful for web testing?]

[Chrome Dev Tools Accessibility features reference](https://developer.chrome.com/docs/devtools/accessibility/reference/)

[Why You Should Avoid Testing React Components With Test IDs](https://betterprogramming.pub/why-you-should-avoid-testing-react-components-with-test-ids-ee50d20d37d2)

[Making your UI tests resilient to change](https://kentcdodds.com/blog/making-your-ui-tests-resilient-to-change). [priority](https://testing-library.com/docs/queries/about/#priority)

> In the spirit of the guiding principles, it is recommended to use this only after the other queries don't work for your use case. Using data-testid attributes do not resemble how your software is used and should be avoided if possible. That said, they are way better than querying based on DOM structure or styling css class names. Learn more about data-testids from the blog post "Making your UI tests resilient to change"

> This is why Testing Library has the queries that it does. The queries help you to find elements in the same way that users will find them. These queries allow you to find elements by their role, label, placeholder, text contents, display value, alt text, title, test ID.

> That's actually in the order of recommendation.

> getByRole Particularly useful with button elements, there are many other elements you can query by their role though, heading being one of them. 


