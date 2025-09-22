[The Cache Replacement Problem](http://alexandrutopliceanu.ro/post/cache-replacement-problem/)

[is this a branch](https://news.ycombinator.com/item?id=26141047)

[	Measuring memory usage: virtual versus real memory](https://news.ycombinator.com/item?id=28007554)

[How a Single Line of Code Made a 24-core Server Slower Than a Laptop](https://pkolaczk.github.io/server-slower-than-a-laptop/)

[Saving a Third of Our Memory by Re-ordering Go Struct Fields](https://lobste.rs/s/oxtpfw/saving_third_our_memory_by_re_ordering_go)

[Using Device Tree Overlays, Example on BeagleBone Boards](https://news.ycombinator.com/item?id=30342948)

[Hotspot performance engineering fails](https://lemire.me/blog/2023/04/27/hotspot-performance-engineering-fails/)

[Performance Through Memory Layout](https://johnnysswlab.com/performance-through-memory-layout/)

[towards atomic writes](https://twitter.com/eatonphil/status/1698132893426434109)

[Cache Line Alignment in C++ — How It Makes Your Program Faster](https://ryonaldteofilo.medium.com/cache-line-alignment-in-c-1aac85e4482f). [tweet](https://twitter.com/kobi_ca/status/1702706567869813212).

[You (Probably) Shouldn't use a Lookup Table](https://specbranch.com/posts/lookup-tables/)

[favorite tracing tools](https://news.ycombinator.com/item?id=38538111)

[strlcpy and how CPUs can defy common sense](https://lobste.rs/s/bjx13v/strlcpy_how_cpus_can_defy_common_sense).

[DDR4 memory organization and how it affects memory bandwidth](https://blog.cloudflare.com/ddr4-memory-organization-and-how-it-affects-memory-bandwidth/)

[What is the best pointer tagging method?](https://coredumped.dev/2024/09/09/what-is-the-best-pointer-tagging-method/)

[Make Your Own CDN with NetBSD](https://news.ycombinator.com/item?id=41432245)

[terminal escape sequences](https://x.com/mitchellh/status/1839762056486281618)

> I should add that this is implemented using standard (but modern) escape sequences. 

[ASM lessons](https://github.com/FFmpeg/asm-lessons)

[Entity Component System Framework that is CPU cache friendly](https://stackoverflow.com/questions/23473783/entity-component-system-framework-that-is-cpu-cache-friendly). [How to benefit from cpu cache in a entity component system game engine?](https://gamedev.stackexchange.com/questions/66786/how-to-benefit-from-cpu-cache-in-a-entity-component-system-game-engine). [How are entity systems cache-efficient?](https://gamedev.stackexchange.com/questions/82030/how-are-entity-systems-cache-efficient)

> He basically used global, pre-allocated arrays for each distinct type of entity data (position, score and whatnot) and references each array in a distinct phase of his system-wide update() function. You can assume that the data for each entity would be at the same array index in each of these global arrays, so for instance, if the player is created first, it might have its data at [0] in each array.

> If you have interdependencies between components (data) such that you absolutely cannot afford to have some data separated from it's associated data (eg. Transform + Physics, Transform + Renderer) then you may opt to replicate Transform data in both the Physics and Renderer arrays, assuring that all pertinent data fits the cache line width for each performance-critical operation.

> Note on writing data Writing does not call out to main memory. By default, today's systems have write-back caching enabled: writing a value only writes it to cache (initially), not to main memory, so you will not be bottlenecked by this. It is only when data is requested from main memory (won't happen while it's in cache) and is stale, that main memory will be updated from cache.

> This is similar to how you have the Structure Of Arrays (SOA) being the recommended approach for HPC. The CPU and cache can deal with multiple linear arrays almost as well as it can deal with a single linear array, and far better than it can deal with random memory access.

> Another strategy used in some ECS implementations - including Unity ECS - is to allocate Components based on the Archetype of their corresponding Entity. That is, all Entities with precisely the set of Components (PhysicsBody, Transform) will be allocated separately from the Entities with different Components (e.g. PhysicsBody, Transform, and Renderable).

> Systems in such designs work by first finding all Archetypes that match their requirements (that have the required set of Components), iterating that list of Archetypes, and iterating the Components stored within each matching Archetype. This allows for completely linear and true O(1) component access within an Archetype and allows Systems to find compatible Entities with very low overhead (by searching a small list of Archetypes rather than searching potentially hundreds of thousands of Entities).

> — You could interleave your entity array instead of keeping separate arrays, but you're still wasting memory
> — This is antithetical to good cache usage. If all you care about are the transforms and graphics data, why make the machine spend time pulling in all that other data for physics and AI and input and debug and so on? For what it's worth, most "production-grade" ECS implementations of which I'm aware use interleaved storage. The popular Archetype approach I mentioned earlier (used in Unity ECS, for example) is very explicitly build to use interleaved storage for Components associated with an Archetype.

> I'm personally a relatively recent convert to the true power of ECS myself. Though for me, the deciding factor was something rarely mentioned about ECS: it makes writing tests for game systems and logic almost trivial compared to the tightly-coupled logic-laden component-based designs I've worked with in the past. Since ECS architectures put all logic in Systems, which just consume Components and produce Component updates, building a "mock" set of Components to test System behaviour is quite eas

[The plight of the misunderstood memory ordering](https://www.grayolson.me/blog/posts/misunderstood-memory-ordering/)

[Pointer Tagging in C++: The Art of Packing Bits into a Pointer](https://news.ycombinator.com/item?id=45328335)


