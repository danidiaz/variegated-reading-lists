[Things I hate about Rust ](https://lobste.rs/s/znzqur/things_i_hate_about_rust)

[Common Rust Lifetime Misconceptions](https://github.com/pretzelhammer/rust-blog/blob/master/posts/common-rust-lifetime-misconceptions.md). [lobsters](https://lobste.rs/s/dypnoa/common_rust_lifetime_misconceptions)

[c++](https://news.ycombinator.com/item?id=23278954)

> i start most of my big objects by deleting the copy constructor and adding a clone member func

> Things like "It is the programmer's responsibility to ensure that std::string_view does not outlive the pointed-to character array."

[Rust's runtime](https://blog.mgattozzi.dev/rusts-runtime/)

[haskell vs. rust for compiler implementations](https://www.reddit.com/r/haskell/comments/gok70o/simple_haskell_is_best_haskell/frj9hty/)

[How to build a WebSocket server with Rust](https://blog.logrocket.com/how-to-build-a-websocket-server-with-rust/)

[strings](https://octobus.net/blog/2020-06-05-not-everything-is-utf8.html)

[Rust vs. C++](https://news.ycombinator.com/item?id=23509916)

[baby steps in rust](https://donsbot.wordpress.com/2020/07/04/back-to-old-tricks-or-baby-steps-in-rust/)

[Statically Sized Higher-kinded Polymorphism](https://lobste.rs/s/vlndlq/statically_sized_higher_kinded)

[Concurrency Patterns in Embedded Rust](https://ferrous-systems.com/blog/embedded-concurrency-patterns/)

[Allow specifying dependencies for individual artifacts](https://github.com/rust-lang/cargo/issues/1982)

[Rust package with both a library and a binary?](https://stackoverflow.com/questions/26946646/rust-package-with-both-a-library-and-a-binary)

[Rust package with both a library and a binary?](https://stackoverflow.com/questions/26946646/rust-package-with-both-a-library-and-a-binary). [path clarity (2018)](https://doc.rust-lang.org/edition-guide/rust-2018/module-system/path-clarity.html)

    // main.rs
    use hello_pack::foo;
    fn main() {
        println!("Hello, world!");
        foo::weex();
    }    
    // lib.rs
    mod lolailo;

    pub mod foo {
        pub fn foo_func() -> u32 {
            return 2
        }

        pub fn weex() {
            crate::lolailo::wee();
            println!("This is a func");
        }
    }    
    // lib.rs alternate
    mod lolailo;

    pub mod foo {
        use crate::lolailo::wee; // can't be outside
        pub fn foo_func() -> u32 {
            return 2
        }

        pub fn weex() {
            wee();
            println!("This is a func");
        }
    }    
    // lolailo.rs
    pub fn wee() {
        println!("wee!");
    }    
    
[crate level visibility for modules in Rust? (2015)](https://www.reddit.com/r/rust/comments/2ls452/crate_level_visibility_for_modules_in_rust/)

[Zero To Production: a WIP book on writing a practical backend project in Rust](https://www.reddit.com/r/programming/comments/hokvxf/zero_to_production_a_wip_book_on_writing_a/)

[Enum or trait object](https://www.possiblerust.com/guide/enum-or-trait-object)

[Why can’t I have more than one mutable reference to a value?](https://users.rust-lang.org/t/why-cant-i-have-more-than-one-mutable-reference-to-a-value/29773)

[What are Rust's exact auto-dereferencing rules?](https://stackoverflow.com/questions/28519997/what-are-rusts-exact-auto-dereferencing-rules)

[Why doesn't dereferencing transfer ownership?](https://www.reddit.com/r/rust/comments/cc5484/why_doesnt_dereferencing_transfer_ownership/)

[Why do we need dereferencing? Could not every use of a reference be understood as using the underlying data](https://www.reddit.com/r/rust/comments/6if67g/why_do_we_need_dereferencing_could_not_every_use/)

[The Rust module system for Python users](https://blog.waleedkhan.name/rust-modules-for-python-users/) [Clear explanation of Rust’s module system](https://www.reddit.com/r/rust/comments/htzkq7/clear_explanation_of_rusts_module_system/) [Rust module system explained](https://www.youtube.com/watch?v=4KsAsGhFo4U&feature=emb_logo&ab_channel=RustCast).

[structuring and handling errors in 2020](https://news.ycombinator.com/item?id=25805340)

[setting the record straight on async](https://news.ycombinator.com/item?id=26410487)

[microsoft Rust course](https://news.ycombinator.com/item?id=27632108)

[inline in Rust](https://matklad.github.io//2021/07/09/inline-in-rust.html)

[a tcp proxy](https://lobste.rs/s/swud1f/tcp_proxy_30_lines_rust)

[Rust n Lisp](https://news.ycombinator.com/item?id=27810193)

[Why not let the OS take care of this?](https://news.ycombinator.com/item?id=28722139)

> On the other hand the OS does know about memory pressure from IO and from heap memory for the whole system. This crate will only know about cache pressure within a single process.

[Rust Iterator Items](https://estebank.github.io/rust-iterator-item-syntax.html)

[What does &mut &[T] mean?](https://lobste.rs/s/w0buyv/what_does_mut_t_mean)

> I’ve also found &mut &[T] helpful for parsers when I want to store the changing “remainder” of what’s left to be parsed, and I want some inner function to mutate that remainder in its own scope.o

[branch forward only](https://news.ycombinator.com/item?id=29350875)

[Async Rust: Panics vs. Cancellation](https://news.ycombinator.com/item?id=30114822)

[Uninitialized Memory: Unsafe Rust is Too Hard](https://lobste.rs/s/bkjsde/uninitialized_memory_unsafe_rust_is_too)

[Some mistakes Rust doesn't catch](https://lobste.rs/s/5jrhuk/some_mistakes_rust_doesn_t_catch)

[prefix sum with SIMD](https://news.ycombinator.com/item?id=30311112)

[JITted, statically-typed AWK written in Rust](https://news.ycombinator.com/item?id=30343373)

[Request Coalescing in Async Rust](https://news.ycombinator.com/item?id=30580797). Includes description of OpenTelemetry.

[Things I hate about Rust, redux](https://lobste.rs/s/bcfxjw/things_i_hate_about_rust_redux)

[Rust is hard](https://news.ycombinator.com/item?id=31601040)

[Async destructors, async genericity and completion futures](https://news.ycombinator.com/item?id=31580627)

[Unsafe Rust is not C](https://twitter.com/steveklabnik/status/1577692166570352641)

[comprehensive Rust](https://news.ycombinator.com/item?id=34091271)

[A taste of pavex, an upcoming Rust web framework](https://news.ycombinator.com/item?id=34195291)

[   Should Small Rust Structs be Passed by-copy or by-borrow?](https://news.ycombinator.com/item?id=34196294)

[Rust atomics and locks](https://twitter.com/m_ou_se/status/1611057658244792320)

[Vulkan tutorial in Rust](https://news.ycombinator.com/item?id=34356060)

[Rust concepts I wish I learned earlier](https://rauljordan.com/rust-concepts-i-wish-i-learned-earlier/)

[htmx and Rust](https://twitter.com/mbvisti/status/1616539940006887447)

[Do references to mutable references need to be mutable?](https://users.rust-lang.org/t/do-references-to-mutable-references-need-to-be-mutable/44049)

> to create a mutable reference to a variable, the variable itself must be marked mut

> if you have an &&mut Vec<i32>, it can be turned into a &Vec<i32>, but not into a &mut Vec<i32>

[Reference to a Reference](https://users.rust-lang.org/t/reference-to-a-reference/44753)

[intro to Rust for FP programmers](https://twitter.com/snoyberg/status/1638896824487493633). [for Scala](https://twitter.com/etorreborre/status/1638826612828393472)

[modular errors in Rust](https://sabrinajewson.org/blog/errors). [thiserror](https://lobste.rs/s/f61udz/modular_errors_with_rust_s_thiserror)

[iterator, generator](https://without.boats/blog/iterator-generator/)

[the Rust I wanted had no future](https://news.ycombinator.com/item?id=36193326)

[error handling, also in C++](https://twitter.com/sadisticsystems/status/1682422067830898692)

[Rust Server Components](https://lobste.rs/s/kilt3o/rust_server_components)

[A JVM in Rust part 5 - Executing instructions](https://andreabergia.com/blog/2023/08/a-jvm-in-rust-part-5-executing-instructions/)

[6 Months of Cooking Up Rust TUIs](https://lobste.rs/s/vlmsti/from_tui_rs_ratatui_6_months_cooking_up)

[Owned values and Futures in Rust](https://www.snoyman.com/blog/owned-values-and-futures/)

[taming the wildcards](https://people.cs.umass.edu/~yannis/variance-extended2011.pdf) [tweet](https://twitter.com/seanbax/status/1700561352534655322)

[A Grounded Conceptual Model for Ownership Types in Rust](https://arxiv.org/abs/2309.04134). [why only a mutable borrow?](https://twitter.com/timClicks/status/1702188487859142952). [post](https://blog.brownplt.org/2023/09/17/rust-ownership.html)

[profiles](https://smallcultfollowing.com/babysteps/blog/2023/09/30/profiles/)

[exceptions yay or nay](https://twitter.com/SusanPotter/status/1709933194135613828)

[The dark side of inlining and monomorphization](https://nickb.dev/blog/the-dark-side-of-inlining-and-monomorphization/)

[Some useful types for database-using Rust web apps](https://boinkor.net/2024/04/some-useful-types-for-database-using-rust-web-apps/)

[Rust stream API](https://news.ycombinator.com/item?id=40156890)

[issues with Rust](https://news.ycombinator.com/item?id=40172033). [tweet](https://twitter.com/khyperia/status/1784234032827371921)

>  one thing I found quite neat is how a very large portion of issues can be solved by reserving entity ids ahead of time (e.g. World::reserve in hecs, note the &world and not &mut world), combined with a command buffer. 

[references are like jumps](https://www.reddit.com/r/haskell/comments/1crzvcn/references_are_like_jumps/)

[high-level rust](https://dioxus.notion.site/Dioxus-Labs-High-level-Rust-5fe1f1c9c8334815ad488410d948f05e)

[Don't write Rust like it's Java](https://lobste.rs/s/nunnw3/don_t_write_rust_like_it_s_java) (?)

[nesting arena allocators](https://lobste.rs/s/scrue4/nesting_arena_allocators_rust)

[shadcdn yay or nay](https://x.com/phuctm97/status/1835352805483352525)

[flattening ASTs](https://www.cs.cornell.edu/~asampson/blog/flattening.html)

[Tracing Large Memory Allocations in Rust with BPFtrace](https://readyset.io/blog/tracing-large-memory-allocations-in-rust-with-bpftrace)

[Thinking like a compiler: places and values in Rust](https://steveklabnik.com/writing/thinking-like-a-compiler-places-and-values-in-rust/)


