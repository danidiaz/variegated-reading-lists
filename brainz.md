Things to try:

- generate text
- generate text from examples given in the prompt ittself (?)
- suggest improvements to existing text
- change style of existing text (?)
- summarize text (perhaps down to only a few words)

[The surprising ease and effectiveness of AI in a loop](https://interconnected.org/home/2023/03/16/singularity)

[the dreaded first steps](https://twitter.com/thorstenball/status/1637064266095239168)

[Using GPT-4 to measure the passage of time in fiction](https://tedunderwood.com/2023/03/19/using-gpt-4-to-measure-the-passage-of-time-in-fiction/)

[ChatGPT is aware of today's date](https://ai.stackexchange.com/questions/39686/chatgpt-is-aware-of-todays-date)

> For ChatGPT 3, the current date is inserted into a long pre-prompt, along
> with instructions like "this is a conversation between an AI chatbot and a
> human" plus "be nice" and "be truthful", which are part of the attempts to
> frame the next-word-predicting engine at the core of ChatGPT as a chatbot.
> OpenAI confirm this approach in their general GPT documentation.

> Inherently, the core of ChatGPT - the GPT large language model - is not a
> chatbot. It has some resemblance conceptually to an image inpainting system —
> it predicts text that is likely, given preceding text.

[ChatGPT plugins](https://twitter.com/OpenAI/status/1638952876281335813). [hn](https://news.ycombinator.com/item?id=35277677). [comment](https://hachyderm.io/@mitchellh/110073950210671765). [lock-in](https://twitter.com/rickasaurus/status/1638572469282918400)

[talking to docs](https://twitter.com/dan_abramov/status/1638674605635239938)

>  i was wondering how much i am writing for humans and how much for the model

[The whole thing is parasitic on a substrate of solid technical writing](https://twitter.com/kevinbaker/status/1638974920074960896)

> In the long term, I think this is going to reshape technical writing and code documenting practices. People are going to write targeting LLMs and not just users.

[q: how do I use TLS here?](https://www.reddit.com/r/haskell/comments/11z50ks/comment/jdd5qcs/)

[glad I never learned X](https://twitter.com/dan_abramov/status/1639253192926978050)

[increasingly absurd](https://twitter.com/birchlse/status/1639258703961415680)

[non-native speakers](https://twitter.com/KrebsVerena/status/1638965122390450176)

[for learning](https://twitter.com/simonw/status/1639707628778692608)

["It's fine not to provide direct answers"](https://twitter.com/bgavran3/status/1639326236487843855)

[an explanation](https://news.ycombinator.com/item?id=35312969)

> The pre-trained model is stage 1 - it has seen everything, but it is wild. If you ask it "What is the capital of US?" it will reply "What is the capital of Canada?"...

> Stage 2 is task solving practice. We use 1000-2000 supervised datasets, formatted as prompt-input-output texts. They could be anything: translation, sentiment classification, question answering, etc. We also include prompt-code pairs. This teaches the model to solve tasks (it "hires" this ability from the model). Apparently training on code is essential, without it the model doesn't develop reasoning abilities.

> But still the model is not well behaved, it doesn't answer in a way we like. So in stage 3 it goes to human preference tuning (RLHF). This is based on human preferences between pairs of LLM answers. After RLHF it learns to behave and to abstain from certain topics.

> You need stage 1 for general knowledge, stage 2 for learning to execute prompts, stage 3 to make it behave.

[you can ask LLMs to critique their outputs](https://twitter.com/ericjang11/status/1639882111338573824)

[put some relevant information in the prompt](https://twitter.com/Ted_Underwood/status/1640366868975308801). [prompt pattern catalog](https://medium.com/@gravity7/towards-gpt-design-patterns-4df8f892cf38)

[An Introduction to Autoencoders](https://www.pinecone.io/learn/autoencoders/)

[good at helping with writing `jq` queries](https://twitter.com/jbrancha/status/1641461163203477506). [the coolest thing is the iteration](https://twitter.com/dan_abramov/status/1641190842080665604)

> and then I used that context to iterate.

[more ambitious](https://news.ycombinator.com/item?id=35382698)

[why not use a decompiler here?](https://twitter.com/moyix/status/1641951052202123264)

[compression](https://twitter.com/alicemazzy/status/1643607089128898561). [not compression, but summary](https://twitter.com/Ted_Underwood/status/1643837637793382400).

[the philosophy of deep learning YouTube list](https://www.youtube.com/watch?v=x10964w00zk&list=PLY_s7b9LrR8W-AGC95PU43oYlERY2IQAk)

[The Post-Human Desert](https://www.project-syndicate.org/commentary/ai-post-human-future-by-slavoj-zizek-2023-04)

[Yaml is streamable](https://twitter.com/goodside/status/1644416197868363779)

[describe and prompt](https://twitter.com/sureailabs/status/1644430593185181723)

[I wish GPT4 had never happened](https://news.ycombinator.com/item?id=35492730)

[sunk cost fallacy](https://twitter.com/IgorBrigadir/status/1644686372966395904)

[Parquet: more than just "Turbo CSV"](https://twitter.com/gunnarmorling/status/1645065940323762177)

[a complex prompt](https://twitter.com/vboykis/status/1645033601392680961)

[baby GPT](https://twitter.com/karpathy/status/1645115622517542913)

[ pushing you to come up with good variable/function names](https://twitter.com/threepointone/status/1645411361038450688)

[creating a database benchmarking project](https://twitter.com/simonw/status/1645981621244534784). [code interpreter alpha](https://twitter.com/simonw/status/1645959248629886978)

[bye abstraction](https://twitter.com/rakyll/status/1645987860460482561)

[the wrong level of abstraction](https://twitter.com/kelseyhightower/status/1646538701818986501)

>  consider using a template to abstract away the details, and only expose the decisions a human needs to make

[if you do it fast enough](https://twitter.com/DavidKPiano/status/1646533664874831872)    

[prompt injection is difficult to fix](https://twitter.com/simonw/status/1645915352734507010). [prompt injection](https://twitter.com/simonw/status/1646931087195791360)

[so, is there a trick?](https://twitter.com/katelelkins/status/1646129651243270144)

> 1) Focus on tasks where you are an expert & get GPT to help
> 2) Give the AI context
> 3) Give it step-by-step directions
> 4) Get an initial answer. Ask for changes and edits
    
[An example of LLM prompting for programming](https://martinfowler.com/articles/2023-chatgpt-xu-hao.html). [tweet](https://twitter.com/martinfowler/status/1646505842416525314)

[explore / exploit](https://twitter.com/headinthebox/status/1647087929821650946)

[the output of the output of optimization](https://twitter.com/rickyflows/status/1648294899211714560)

[grandma exploit](https://twitter.com/jjvincent/status/1648594881198039040). [what's the worst that can happen?](https://twitter.com/migueljogja/status/1648643829845860352)

[why RL](https://twitter.com/Ted_Underwood/status/1649801405731930112)

[unusable](https://twitter.com/lurker_tech/status/1649513550665355264)

[role switching](https://twitter.com/lcamtuf/status/1652136156207923200)

[copilot chat leaked prompt](https://news.ycombinator.com/item?id=35921375)

[bard and json](https://twitter.com/goodside/status/1657396491676164096)

[second pair of eyes](https://twitter.com/JoshDesignNz/status/1657687559651340288)

[The Silent (R)evolution of SAT](https://news.ycombinator.com/item?id=36079115)

[positional encoding in transformers](https://twitter.com/moultano/status/1664691765624840193)

[Chain-of-Thought Prompting](https://twitter.com/bohang_zhang/status/1664695084875501579)

[GPT best practices](https://platform.openai.com/docs/guides/gpt-best-practices/strategy-write-clear-instructions). [hn](https://platform.openai.com/docs/guides/gpt-best-practices/strategy-write-clear-instructions).

> Delimiters like triple quotation marks, XML tags, section titles, etc. can help demarcate sections of text to be treated differently.

> Tactic: Specify the desired length of the output

[self-distillation](https://twitter.com/revhowardarson/status/1667316201977188353)

[Function calling](https://openai.com/blog/function-calling-and-other-api-updates). [the new openAI function call interface is basically 'make your reply confirm to a provided algebraic data type'](https://twitter.com/disconcision/status/1669082221964058624)

[Illustrating Reinforcement Learning from Human Feedback (RLHF)](https://huggingface.co/blog/rlhf)

[textbooks are all you need](https://news.ycombinator.com/item?id=36413768)

[but so are markets](https://twitter.com/henryfarrell/status/1671547591262191618)

Things for which I found ChatGPT useful:

    - identifying a dumb React component syntax issue (not using a props
      object) which would be difficult to Google. 
    - nomenclature: what is the type of web proxy that is the main alternative to "intercepting proxies"? (did I get the correct response?)
    - trying to gauge the consensus between two alternatives, according to some criterium: "should we expect shorter compile times with package-by-layer or with package-by-feature". 

[staying ahead](https://news.ycombinator.com/item?id=36586248)

[always expanding](https://twitter.com/bildoperationen/status/1678691294242041856)

[overuse?](https://twitter.com/hot_girl_spring/status/1681556263526707200). [more](https://twitter.com/hrstmr98/status/1681571051619356673).

[ review fatigue](https://martinfowler.com/articles/exploring-gen-ai.html#in-line-assistance---when-is-it-more-useful). [tweet](https://twitter.com/martinfowler/status/1687132532989661184).

[catching up](https://twitter.com/simonw/status/1687117410984431616)

[isn't that awful](https://twitter.com/masa_morioka/status/1689668427328241664)

[copilot and remembering the details](https://twitter.com/Rich_Harris/status/1690535688582651904) 

[the use-cases that you don't want](https://twitter.com/ShriramKMurthi/status/1690640165486616577)

[How Is LLaMa.cpp Possible? ](https://news.ycombinator.com/item?id=37140013)

[don't ask them about themselves](https://twitter.com/random_walker/status/1692863292178301110)

[wealth concentration](https://news.ycombinator.com/item?id=37210953)

[Changing my relationship with GitHub Copilot ](https://news.ycombinator.com/item?id=37303357)

[Making deep learning go brrrr from first principles (2022)](https://news.ycombinator.com/item?id=37361711)

[OpenAI Cookbook](https://twitter.com/simonpfish/status/1705255275488551213)

[German Large Language Model Released](https://laion.ai/blog/leo-lm/). [hn](https://news.ycombinator.com/item?id=37699465).

[extract Latex code from image](https://twitter.com/rasbt/status/1709173115245170741)

[for writing tests](https://twitter.com/rakyll/status/1708937806859624523)

[veggies](https://twitter.com/sherjilozair/status/1708604719881765111)

[prompting techniques](https://twitter.com/_jasonwei/status/1712551642275655770)   

[ChatGPT’s system prompts](https://news.ycombinator.com/item?id=37879077). [tweet](https://twitter.com/browserdotsys/status/1713330387852648685).

[internet big](https://twitter.com/rao2z/status/1713173089947890043)

[embeddings](https://simonwillison.net/2023/Oct/23/embeddings/). [tweet](https://twitter.com/simonw/status/1716449601505657224). [hn](https://news.ycombinator.com/item?id=37985489)

[v0](https://news.ycombinator.com/item?id=37974743)

[the human name schema](https://twitter.com/patio11/status/1720481037002608922)

[under pressure](https://news.ycombinator.com/item?id=38136863)

[An Introduction to Transformers](https://arxiv.org/abs/2304.10557)

[New models and developer products announced at DevDay (2023)](https://openai.com/blog/new-models-and-developer-products-announced-at-devday). [HN](https://news.ycombinator.com/item?id=38166420)

[storing data for Assistant](https://twitter.com/simonw/status/1721991569577009489)

[so simple](https://twitter.com/quantian1/status/1723421715391270923)

[a survery of techniques](https://www.youtube.com/watch?v=ahnGLM-RC1Y)

[Catching up on the weird world of LLMs](https://www.youtube.com/watch?v=h8Jth_ijZyY)

[an use for it](https://twitter.com/peligrietzer/status/1725932982920229307)

[some papers](https://twitter.com/jxmnop/status/1725949517940294055)

[The architecture of today’s LLM applications](https://github.blog/2023-10-30-the-architecture-of-todays-llm-applications/)

[posting screenshots](https://twitter.com/garybernhardt/status/1727441786040373696)

[intro to LLMs](https://www.reddit.com/r/LocalLLaMA/comments/181wiqg/intro_to_large_language_models_andrew_karpathy/)

[synthetic data and distillation](https://twitter.com/moultano/status/1727813093697474678)

[Generative AI for Beginners (Microsoft)](https://news.ycombinator.com/item?id=38405823). [hn](https://news.ycombinator.com/item?id=38405823)

>  with chain of thought attention starts being applied to the user input in a fundamentally different way than it normally is

[what the bitter lesson says](https://twitter.com/davidad/status/1728165673786847607)

["chain of thought" is just some weird form of continuation semantics for code written in natural language](https://twitter.com/headinthebox/status/1725336551427883420) ??

[create structured (genealogical) data using unstructured text](https://twitter.com/kishau/status/1728220318031052948)

[What does x mean here?](https://twitter.com/s_r_constantin/status/1728783142578725199).

[the "more and more" pattern](https://twitter.com/moultano/status/1729242982589792459). [another example](https://twitter.com/TobiasJolly/status/1729061707925069928)

[understanding deep learning](https://news.ycombinator.com/item?id=38424939)

[How to tackle unreliability of coding assistants](https://news.ycombinator.com/item?id=38456726)

[Seamless: Meta's New Speech Models](https://news.ycombinator.com/item?id=38487359)

[wishper](https://twitter.com/emollick/status/1730653385206968418)

[the linguistic echo chambers of LLMs](https://lobste.rs/s/suk9dd/multifaceted_linguistic_echo_chambers)

[Lena](https://news.ycombinator.com/item?id=38538122)

[what quants do](https://twitter.com/macrocephalopod/status/1732385664153358474)

[llama 2](https://www.youtube.com/watch?v=NvTSfdeAbnU)

[LLMs make Programming Language Learning Curves Shallower](https://lobste.rs/s/67brng/llms_make_programming_language_learning)

[prompt engineering guide](https://platform.openai.com/docs/guides/prompt-engineering/prompt-engineering)

[Pushing ChatGPT's Structured Data Support To Its Limits](https://minimaxir.com/2023/12/chatgpt-structured-data/). [openai reference](https://platform.openai.com/docs/guides/function-calling)

> OpenAI introduced function calling last June, but what’s *really* the big feature is ChatGPT’s ability to output structured data in, even complex nested schema!

[code for code's sake](https://twitter.com/BHolmesDev/status/1739037983334867009)

[Macondo](https://twitter.com/GrantSlatton/status/1741149378516263243)

[Stuff we figured out about AI in 2023](https://simonwillison.net/2023/Dec/31/ai-in-2023/)

[LLMs and Programming in the first days of 2024](http://antirez.com/news/140). [hn](https://news.ycombinator.com/item?id=38840626)

[ReAct-style reasoning is essentially continuation semantics](https://twitter.com/headinthebox/status/1748579429234901248)

[agents](https://twitter.com/revhowardarson/status/1748799648343687301)

[curating, synthesizing, and organizing knowledge](https://twitter.com/vboykis/status/1748839726470066396)

[translation](https://twitter.com/kendrictonn/status/1752004719440994793)

[post-redirect-get](https://twitter.com/colin_fraser/status/1750289872420815087)

[Prompt Design and Engineering: Introduction and Advanced Methods](https://arxiv.org/abs/2401.14423). [tweet](https://twitter.com/xamat/status/1752565060864704789). [tweet](https://twitter.com/zswitten/status/1752700765380997591)

[a multilingual paradox](https://twitter.com/Dorialexander/status/1752817852006990050)

[ditching copilot](https://twitter.com/mariofusco/status/1753800199116406968)

[what do people use LLMs for](https://twitter.com/vboykis/status/1754225996973158461)

[just putting in more stuff](https://nostalgebraist.tumblr.com/post/741247180226052096/i-dont-think-youre-drawing-the-right-lesson-from)

[self-attention](https://twitter.com/mattecapu/status/1756999384338670067)  

[describing potential errors](https://twitter.com/patio11/status/1757426785837298055). [language translation](https://twitter.com/tallinzen/status/1757202478683013544).

[how a transformer works](https://twitter.com/revhowardarson/status/1757304946788274391)

[Memory and new controls for ChatGPT](https://openai.com/blog/memory-and-new-controls-for-chatgpt). [hn](https://news.ycombinator.com/item?id=39360724).

[Representation Engineering: Mistral-7B on Acid](https://news.ycombinator.com/item?id=39414532)

[Claude 3's system prompt](https://twitter.com/AmandaAskell/status/1765207842993434880)

[The GPT-4 barrier has finally been broken](https://simonwillison.net/2024/Mar/8/gpt-4-barrier/)

[Claude for vuln analysis](https://twitter.com/ShriramKMurthi/status/1766484834841436227)

[#Claude3 does function calling purely in "user space".](https://twitter.com/headinthebox/status/1769187308006527135).

[overparameterization](https://twitter.com/revhowardarson/status/1774221186232369611)

> the idea of overparameterization beating any sort of domain understanding is genuinely embittering 

[put the question last](https://twitter.com/emollick/status/1774255147960430931)

[inhuman errors](https://twitter.com/qntm/status/1773779967521780169)

[RAG vs. finetuning](https://twitter.com/jerryjliu0/status/1772677211545543094)

[how self-attention & multi-head attention in transformers work](https://twitter.com/DanAkarca/status/1772565907350372651)

[better crap is worse](https://twitter.com/Lucretiel/status/1772763504577028119)

[A Very Gentle Introduction to Large Language Models without the Hype](https://mark-riedl.medium.com/a-very-gentle-introduction-to-large-language-models-without-the-hype-5f67941fa59e)

[standard transformer architecture](https://twitter.com/Muhtasham9/status/1772469982485438485)

[training a model vs building a RAG system](https://twitter.com/simonw/status/1772273715851473337)

[Compile from withing ChatGPT](https://twitter.com/simonw/status/1771684378990522575)

["hard to overstate the impact of LoRas"](https://twitter.com/francoisfleuret/status/1770704814910898630).

[When will LLMs be able to interrupt or interject?](https://news.ycombinator.com/item?id=39659087)

[offering a tip](https://news.ycombinator.com/item?id=39495476)

[function calling support in Claude](https://twitter.com/simonw/status/1775981308856193354)


