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

[function calling support in Claude](https://twitter.com/simonw/status/1775981308856193354). [hn](https://news.ycombinator.com/item?id=39936048).

[tutorial on the self-attention mechanism used in transformers.](https://twitter.com/aprilkhademi/status/1776346652241977375)

[stream-of-search](https://twitter.com/headinthebox/status/1777387903666246028)

[Embeddings are a good starting point ](https://news.ycombinator.com/item?id=40067486)

[Weeknotes Apr 23 2024: Llama 3, AI for Data Journalism, llm-evals and datasette-secrets](https://simonwillison.net/2024/Apr/23/weeknotes/)

[A guidance language for controlling large language models](https://github.com/guidance-ai/guidance). [video](https://www.youtube.com/watch?v=4Wz61w5zbCk)

[tokenizer playground](https://twitter.com/simonw/status/1782862006095343757)

[ LMSYS Chatbot Arena Leaderboard](https://chat.lmsys.org/?leaderboard). [tweet](https://twitter.com/simonw/status/1782872174967287999).

[llama 3](https://llama.meta.com/llama3/). [github](https://github.com/meta-llama/llama3)

[hugging face](https://huggingface.co/). [llama on hf](https://huggingface.co/meta-llama).

[Getting access to Claude](https://docs.anthropic.com/claude/docs/getting-access-to-claude)

[Apple CoreNet](https://twitter.com/simonw/status/1782970554611593683). [HN](https://github.com/apple/corenet/blob/main/projects/openelm/README-pretraining.md). [hn](https://news.ycombinator.com/item?id=40139398).

[getting unstuck](https://twitter.com/GergelyOrosz/status/1783124079844770045)

[ollama](https://ollama.com/library/llama3). [llamafile](https://twitter.com/JustineTunney/status/1783318018317271241)

[the little book of deep learning](https://fleuret.org/francois/lbdl.html)

[Berkeley Function-Calling Leaderboard](https://gorilla.cs.berkeley.edu/leaderboard.html). [tweet](https://twitter.com/shishirpatil_/status/1783960177051627706). [tweet](https://twitter.com/HamelHusain/status/1783999121927598369).

[different uses](https://twitter.com/vboykis/status/1784279327250485595)

[pydantic all you need?](https://twitter.com/latentspacepod/status/1781400226793673137)

[code assistance](https://twitter.com/vboykis/status/1785028286017368289)

[ differentiable wonderland](https://www.sscardapane.it/alice-book). [arxiv](https://arxiv.org/abs/2404.17625).

[System prompts are adding unnecessary complexity, change my mind!](https://www.reddit.com/r/LocalLLaMA/comments/19dscer/system_prompts_are_adding_unnecessary_complexity/). [ChatGPT-System-Prompts](https://github.com/mustvlad/ChatGPT-System-Prompts).

[LoRA+](https://news.ycombinator.com/item?id=40188511)

[GPT-4o](https://news.ycombinator.com/item?id=40345775)

[GPUs Go Brrr](https://news.ycombinator.com/item?id=40337936)

[replaced](https://twitter.com/BlancaWrites/status/1790403709119414321)

[function calling vs. ReAct](https://x.com/headinthebox/status/1791575481709707653)

[golden gate claude](https://www.anthropic.com/news/golden-gate-claude). [twitter](https://x.com/i/bookmarks?post_id=1793844076972015733). [twitter](https://x.com/raphaelmilliere/status/1793832549472743551). [tweet](https://x.com/zswitten/status/1793748330796978589).

[power users](https://x.com/max_paperclips/status/1799462483163332773). [compile C code](https://x.com/simonw/status/1799465170198310961)

[tool calling prompts](https://x.com/lgrammel/status/1801213236081004809). [page](https://sdk.vercel.ai/docs/ai-sdk-core/tools-and-tool-calling#prompt-engineering-with-tools).

[A Systematic Survey of Prompting Techniques](https://arxiv.org/abs/2406.06608). [tweet](https://x.com/sophiamyang/status/1801340351447203917). [a prompt](https://x.com/teej_m/status/1801388306627969126).

[Claude 3.5 Sonnet](https://x.com/simonw/status/1803819993416466573). [for coding](https://x.com/AndyMasley/status/1803981639736869108).

[LLMs for financial applications](https://arxiv.org/abs/2406.11903).

[Every Way To Get Structured Output From LLMs](https://www.boundaryml.com/blog/structured-output-from-llms). ["declarative prompting"](https://www.iqvia.com/blogs/2024/04/prompt-and-proper-how-iqvia-is-using-declarative-llm). [some notes](https://methexis.substack.com/p/some-llm-framework-lessons). [lmql constraints](https://lmql.ai/docs/language/constraints.html).

[claude Sonnet](https://www.anthropic.com/news/claude-3-5-sonnet)

[Building search-based RAG using Claude, Datasette and Val Town ](https://lobste.rs/s/iyq4pf/building_search_based_rag_using_claude). [tweet](https://x.com/sh_reya/status/1804572296855830602). [rag](https://x.com/sh_reya/status/1804572296855830602).

[LLM101n: Let's build a Storyteller](https://github.com/karpathy/LLM101n?tab=readme-ov-file). [generative AI for beginners](https://github.com/microsoft/generative-ai-for-beginners/tree/main).

[using artifacts with Claude](https://x.com/emollick/status/1804928079048946157). [cot](https://arxiv.org/html/2401.04925v3). [moar claude](https://x.com/BHolmesDev/status/1804530759165702594).

- 1) Ask it to create a design document first, it serves a CoT function
- 2) Just talk to it and ask for improvements
- 3) Show it screenshots

[suspicious lists](https://x.com/whitequark/status/1805543290185376244) 

["Explain it with gradually increasing complexity."](https://www.reddit.com/r/LocalLLaMA/comments/1dp378t/very_powerful_prompt_explain_it_with_gradually/)

[asking questions from code](https://x.com/penberg/status/1807064051966419338)

[building a web UI](https://x.com/simonw/status/1808233468175999127)

[home-cooked software](https://x.com/simonw/status/1810335524017877240)

[Long context windows don't replace RAG](https://x.com/simonw/status/1811060073806090742). [more](https://x.com/HamelHusain/status/1811413934420926970).

[art experiments](https://x.com/revhowardarson/status/1812388631996477691)

[Imitation Intelligence](https://x.com/simonw/status/1812498751535419742)

[role prompting superstition](https://x.com/simonw/status/1812699159625138543).

[promting useinstructor](https://python.useinstructor.com/prompting/).

[Awesome-LLM-Constrained-Decoding](https://github.com/Saibo-creator/Awesome-LLM-Constrained-Decoding)

[AI Search: The Bitter-er Lesson](https://www.reddit.com/r/reinforcementlearning/comments/1dgxmnj/ai_search_the_bitterer_lesson_mclaughlin/)

[EVALUATING RETRIEVAL IN RAGS: A PRACTICAL FRAMEWORK](https://www.tweag.io/blog/2024-03-21-evaluating-retrieval-in-rag-framework/)

[Prover-Verifier Games](https://openai.com/index/prover-verifier-games-improve-legibility/)

[guide to the Transformer architecture, with Keras code examples](https://x.com/fchollet/status/1813362217020219587)

[SpreadsheetLLM: Encoding Spreadsheets for Large Language Models](https://news.ycombinator.com/item?id=40985017)

[Converting Codebases with LLMs](https://news.ycombinator.com/item?id=41014052)

[Solving the out-of-context chunk problem for RAG](https://news.ycombinator.com/item?id=41034297)

[How do you automate your life using LLMs?](https://www.reddit.com/r/ClaudeAI/comments/1eflgf5/how_do_you_automate_your_life_using_llms/)

[llama workflows (like Rx?)](https://x.com/llama_index/status/1819048068798616058). 

[open ai structured outputs](https://simonwillison.net/2024/Aug/6/openai-structured-outputs/). [official post](https://openai.com/index/introducing-structured-outputs-in-the-api/). [tweet](https://x.com/simonw/status/1820926836135678409). [jsonformer](https://x.com/Yampeleg/status/1820890368457806065). [ast](https://x.com/headinthebox/status/1820968680135774554). [hn](https://news.ycombinator.com/item?id=41173223). [three solutions](https://x.com/burkov/status/1821759647994236943).

[pockets](https://x.com/GergelyOrosz/status/1821453959598313946)

[RLHF is just barely RL](https://news.ycombinator.com/item?id=41188647). [tweet](https://x.com/karpathy/status/1821277264996352246).

[how I program in 2024](https://news.ycombinator.com/item?id=41157494)

[Generative AI may be more useful to understand code rather than generate it](https://martinfowler.com/articles/exploring-gen-ai.html#memo-09)

[Language Models as Models of Language](https://arxiv.org/abs/2408.07144). [tweet](https://x.com/raphaelmilliere/status/1824116401893773700).

[good an unminifying](https://news.ycombinator.com/item?id=41389185)

[inherently unreliable ](https://x.com/simonw/status/1828074949330030893)

[joker or not](https://x.com/housecor/status/1827787642081329420). [cursor](https://x.com/chrisalbon/status/1827890375903809661). [more](https://x.com/Afinetheorem/status/1827406013739495724). [k](https://x.com/karpathy/status/1827192004117458973). [more](https://x.com/burkov/status/1827027880490016959). [more](https://x.com/fchollet/status/1826743094194438420). [more](https://x.com/ShengwuLi/status/1826392080517922962). [shared understanding](https://x.com/mipsytipsy/status/1826298635514208409). [tired of fixing](https://news.ycombinator.com/item?id=41315138).

[fast edit mode](https://x.com/simonw/status/1826022466319430098)

[Prompt Caching (beta)](https://docs.anthropic.com/en/docs/build-with-claude/prompt-caching). [hn](https://news.ycombinator.com/item?id=41284639).

> Prompt Caching is a powerful feature that optimizes your API usage by allowing resuming from specific prefixes in your prompts. This approach significantly reduces processing time and costs for repetitive tasks or prompts with consistent elements.

[debugging machine learning workflows](https://x.com/vboykis/status/1826045614452519261)

[base models](https://x.com/thesephist/status/1825404436828635494)

[ Anthropic interactive prompting tutorial ](https://x.com/simonw/status/1829352666142757365). [hn](https://news.ycombinator.com/item?id=41395921). [more](https://fedi.simonwillison.net/@simon/113049088115251541)

[Based on this documentation...](https://fedi.simonwillison.net/@simon/113049462303201018)

[Llama adoption](https://news.ycombinator.com/item?id=41391267)

[also for the questions](https://x.com/freganmitts/status/1828796730634330593)

[RHLF](https://x.com/yugu_nlp/status/1832138441657872436)

["a signal of seriousness"](https://x.com/fchollet/status/1831029432653599226)

[I already have approval from my ethics board](https://x.com/simonw/status/1830272530646708224)

[Building LLMs from the Ground Up: A 3-Hour Coding Workshop](https://news.ycombinator.com/item?id=41412256)

[How to Read Deep Learning Paper as a Software Engineer](https://news.ycombinator.com/item?id=41457206)

["I just throw my notes into chat"](https://x.com/tylerangert/status/1833168728327950481). [grug?](https://x.com/_deepfates/status/1832958028418855306)

[autoregressive](https://x.com/karpathy/status/1835024197506187617)

[Learning to Reason with LLMs](https://openai.com/index/learning-to-reason-with-llms/). [Notes on OpenAI’s new o1 chain-of-thought models](https://simonwillison.net/2024/Sep/12/openai-o1/). [hn](https://news.ycombinator.com/item?id=41527143). [lobsters](https://lobste.rs/s/sktjxk/openai_o1_model). [bitter-er lesson](https://x.com/dioscuri/status/1834291979355598980). [AI Search: The Bitter-er Lesson](https://yellow-apartment-148.notion.site/AI-Search-The-Bitter-er-Lesson-44c11acd27294f4495c3de778cd09c8d). [thoughts](https://x.com/Miles_Brundage/status/1834291595648377091). [scaling](https://x.com/lateinteraction/status/1834553612921446485).

[Is telling a model to "not hallucinate" absurd?](https://news.ycombinator.com/item?id=41497619). [tweet](https://x.com/yoavgo/status/1833240454617567630)

[Any RL approach is only as good as its environment/reward model.](https://x.com/pfau/status/1834362105811915184)

[LLM Evaluation Metrics: The Ultimate LLM Evaluation Guide ](https://www.confident-ai.com/blog/llm-evaluation-metrics-everything-you-need-for-llm-evaluation)

[instead of taking screenshots](https://x.com/RealGeneKim/status/1833298959890321503)

[how to prompt](https://x.com/alexalbert__/status/1831767526377963546)

[cat script.R | llm "what does this code do?"](https://x.com/MarcJBrooker/status/1831731866527039615)

[history | tail -n 2000 | llm -s "Write aliases for my zshrc based on my terminal history. Only do this for most common features. Don't use any specific files or directories"](https://x.com/__anjor/status/1830972847759729124)

[How to Read Deep Learning Paper as a Software Engineer ](https://news.ycombinator.com/item?id=41457206)

[In Defense of RAG in the Era of Long-Context Language Models](https://arxiv.org/abs/2409.01666)

[claude's prefilling](https://eugeneyan.com/writing/prompting/#prefill-claudes-responses)

[structuralism](https://x.com/jonothingEB/status/1830652235774394461)

[how to use LLMs](https://x.com/albrgr/status/1836100835719499799)

[generating tests](https://stackoverflow.blog/2024/09/10/gen-ai-llm-create-test-developers-coding-software-code-quality/)

[Awesome LLM Strawberry (OpenAI o1)](https://github.com/hijkzzz/Awesome-LLM-Strawberry)

[Contextual Retrieval (Anthropic)](https://news.ycombinator.com/item?id=41598119)

[podcasts from code with @GoogleAI NotebookLM](https://x.com/rseroter/status/1836519803802259732). [more](https://x.com/rakyll/status/1836955176911200719)

[hot takes about embedding-based RAG](https://x.com/sh_reya/status/1836427763605258384)

[Legacy Modernization meets GenAI](https://martinfowler.com/articles/legacy-modernization-gen-ai.html)

[Chain of Thought Empowers Transformers to Solve Inherently Serial Problems](https://news.ycombinator.com/item?id=41564611)

[You can tell the RL is done properly when the models cease to speak English ](https://x.com/karpathy/status/1835561952258723930)

[I hate language now](https://x.com/QiaochuYuan/status/1835811003453612345). [a machine called language](https://x.com/QiaochuYuan/status/1836157189070950554).

[g1: Using Llama-3.1 70B on Groq to create o1-like reasoning chains](https://news.ycombinator.com/item?id=41550364)

[experiences with a base model](https://x.com/GabriellaG439/status/1837736939791044895)

[OpenAI has released a new o1 prompting guide.](https://x.com/dr_cintas/status/1837192765555245384)

[poking around with the OpenAI, Anthropic and Google Gemini streaming APIs](https://x.com/simonw/status/1837604162453876873)

[how Cursor prompts were created](https://x.com/tom_doerr/status/1838001895207510380)

[issues with declarative composition](https://x.com/sh_reya/status/1838641761419432365)

[regularization](https://x.com/maksym_andr/status/1838530434793099617)

[generating lecture slides from a book](https://x.com/_alice_evans/status/1839199838367326378)

[how much miscellany is worth](https://x.com/peligrietzer/status/1840158458890383559)

[I'm tired of AI](https://www.ontestautomation.com/i-am-tired-of-ai/). [hn](https://news.ycombinator.com/item?id=41667652)

[experience with Cursor](https://x.com/SebAaltonen/status/1840347984094994658)

[creepy](https://hachyderm.io/@simon@simonwillison.net/113223718312619516). [recursion](https://fedi.simonwillison.net/@simon/113224231076888065). [fried rice](https://hachyderm.io/@simon@simonwillison.net/113228023656225911)

[Rhetoric as Codec: Machine Learning and the Facilitation of Reading and Writing](https://hannesbajohr.de/en/2024/10/03/rhetoric-as-codec-machine-learning-and-the-facilitation-of-reading-and-writing-with-an-aside-about-surfing-and-riding/)

[meta movie gen](https://x.com/Andrew__Brown__/status/1842262328617672725)

[partner to converse](https://x.com/_xjdr/status/1842329162402648338)

[They're a *set-processing* architecture](https://x.com/fchollet/status/1846263128801378616)

> Transformers are 100% order-agnostic (which was the big innovation compared to RNNs, back in late 2016 -- you compute the full matrix of pairwise token interactions instead of processing one token at a time)

> The way you add order awareness in a Transformer is at the *feature* level. You literally add to your token embeddings a position embedding / encoding that corresponds to its place in a sequence. The architecture itself just treats the input tokens as a set.

[scrapping gmail to json](https://x.com/simonw/status/1846300324392571107)

[giving notes to the hosts](https://x.com/raiza_abubakar/status/1846944566689353838)

[RAG with SpringAI](https://x.com/sergialmar/status/1847232223121957099)

[temperature, top_p and top_k](https://x.com/simonw/status/1847513454825132337)

[plateauing or not?](https://x.com/emollick/status/1848410341778035030)

[mini-apps with Claude Artifacts](https://x.com/simonw/status/1848372319548240371)

[Initial explorations of Anthropic’s new Computer Use capability](https://simonwillison.net/2024/Oct/22/computer-use/)

[Stanford CS229 I Machine Learning I Building Large Language Models (LLMs)](https://www.youtube.com/watch?v=9vM4p9NN0Ts)

> A concise overview of building a ChatGPT-like model, covering both pretraining (language modeling) and post-training (SFT/RLHF).

[Embeddings are underrated](https://technicalwriting.dev/data/embeddings.html)

[generative games](https://x.com/natanielruizg/status/1849807021131874583)

[XML vs JSON mixup](https://x.com/headinthebox/status/1851053618579063022)

[Unlock GitHub Copilot’s Full Potential](https://www.youtube.com/watch?v=SLMfhuptCo8). 

[copilot edits](https://x.com/code/status/1851336106588950817).

> Quickly iterate on large changes across multiple files, bringing the
> conversational flow of Copilot Chat and fast feedback from Inline Chat
> together in one experience.

[Copilot's new multi-file edits with @AnthropicAI 's Claude 3.5 Sonnet ](https://x.com/ashtom/status/1851316495336554663)

[github spark](https://x.com/ashtom/status/1851333075374051725)

[Embeddings are underrated ](https://news.ycombinator.com/item?id=42013762)

[Oasis: A Universe in a Transformer ](https://news.ycombinator.com/item?id=42014650). [tweet](https://x.com/mtrc/status/1852322790679965890).

[   What I've learned building with AI ](https://news.ycombinator.com/item?id=42008005)

[   ChatGPT Search](https://news.ycombinator.com/item?id=42008569). [but why](https://x.com/biblioracle/status/1852369013914870060).

[overfitting on small data sets](https://x.com/milos_ai/status/1852404429720330741)

[ how to create prompts that create prompts](https://x.com/emollick/status/1852842990655455522)

["do not hallucinate" doesn't work](https://x.com/GaryMarcus/status/1852500409572794816)

[the advantage of having evaluations](https://x.com/simonw/status/1853526689734852693)

[prompt patterns](https://x.com/headinthebox/status/1854267151894630630)

[NuExtract 1.5](https://simonwillison.net/2024/Nov/16/nuextract-15/)

> Structured extraction - where an LLM helps turn unstructured text (or image content) into structured data - remains one of the most directly useful applications of LLMs.

[Model Context Protocol (MCP)](https://x.com/simonw/status/1861082804228108717)

[structured data extraction running on an LLM that executes entirely in the browser](https://simonwillison.net/2024/Nov/29/structured-generation-smollm2-webgpu/). [tweet](https://x.com/simonw/status/1862605223791141362).

[second thoughts](https://simonwillison.net/2024/Nov/29/llm-flowbreaking/)

[Things we learned about LLMs in 2024](https://news.ycombinator.com/item?id=42560558)

> Drop your files in the context window; ask very precise questions explaining the background. They work great to explore what is at the borders of your knowledge.

[How I run LLMs locally](https://lobste.rs/s/kcjd1w/how_i_run_llms_locally)

[Example of searching for info and finding slop](https://www.youtube.com/watch?v=-opBifFfsMY)

["How I program with LLMs"](https://news.ycombinator.com/item?id=42617645)

[for spreadsheets](https://www.reddit.com/r/ClaudeAI/s/menuwo11bG)

[chat with codebase in Cursor](https://docs.cursor.com/chat/codebase)

[Github copilot overview](https://code.visualstudio.com/docs/copilot/overview)

[AI founders will learn The Bitter Lesson](https://lukaspetersson.com/blog/2025/bitter-vertical/)

Example of Copilot prompt that worked well in the `Copilot Edits` pane:

> In the file PagilaRel8, there are some data type and schema datatypes for interfacing with database tables. I want to fill the file PagilaEsqueleto with analogous definitions. But the ones in PagilaEsqueleto are different, they are in the form of a Template Haskell quasiquoter with a particular syntax. Nevertheless, the definitions in PagilaRel8 are relevant, because the list record field names and the database table and column names that we want to use (these in the schema definitions).

> There are a few definitions that have already been added to the PagilaEsqueleto file: author, address, city. You can guide yourself by these in order to translate the rest. Good luck!

Another one:

> In the PagilaEsqueleto file, I have a bunch of Esqueleto entity definitions
> in a quasiquotes. Entities like author, address, city. 

> I also have query definitions for some of these entities. Like
> "selectSomeActors" for actor, "selectSomeAddresses", "selectSomeCategories"
> and "selectSomeCities" for other entities.

> But there are still a lot of entities without a sample query. Please generate the queries for the missing entities. They all follow the same structure, so it should be easy.

[The prompt report](https://arxiv.org/abs/2406.06608). [blog](https://www.aihero.dev/the-prompt-report).

[The 2025 AI Engineer Reading List](https://www.latent.space/p/2025-papers)

[comparison](https://x.com/theo/status/1879121809850929583)

[I don't remember what my code does](https://www.youtube.com/shorts/4Q5ceNbNdew)

[code was expensive](https://simonwillison.net/2025/Jan/15/geoffrey-litt/#atom-everything)

[How I program with LLMs](https://crawshaw.io/blog/programming-with-llms)

> Avoid creating a situation with so much complexity and ambiguity that the LLM gets confused and produces bad results. This is why I have had little success with chat inside my IDE. My workspace is often messy, the repository I am working on is by default too large, it is filled with distractions. One thing humans appear to be much better than LLMs at (as of January 2025) is not getting distracted. That is why I still use an LLM via a web browser, because I want a blank slate on which to craft a well-contained request.

> Ask for work that is easy to verify.

> As LLMs do better with exam-style questions, more and smaller packages make it easier to give a complete and yet isolated context for a piece of work. This is true for humans too, which is why we use packages at all, but we trade off package size against the extra typing/plumbing/filing to make more readable code. With an LLM both doing and benefiting from a big chunk of that extra work, the tradeoff shifts. (As a bonus, we humans get more readable code!)

[better prompts = better code](https://www.youtube.com/shorts/NoWqPZIZnG4)

[Best practices for using GitHub Copilot](https://docs.github.com/en/enterprise-cloud@latest/copilot/using-github-copilot/best-practices-for-using-github-copilot)

[on the DeepSeek models](https://x.com/kmett/status/1882859216802902207). [for coding](https://bsky.app/profile/simonwillison.net/post/3lgqlbme7nk22).

[chain-of-thought](https://mastodon.gal/@Rataunderground@paquita.masto.host/113899626998205458)

[Emerging Patterns in Building GenAI Products](https://martinfowler.com/articles/gen-ai-patterns/)

[You could have invented transformers](https://hachyderm.io/@dpiponi@mathstodon.xyz/113909280494993298)

[paradox](https://bsky.app/profile/peligrietzer.bsky.social/post/3lh53odbbuk2k)

[a farewell to manual prompting](https://news.ycombinator.com/item?id=42861815)

[demystifying deepseq](https://www.thoughtworks.com/insights/blog/generative-ai/demystifying-deepseek)

[(WIP) A Little Bit of Reinforcement Learning from Human Feedback](https://rlhfbook.com/). [hn](https://news.ycombinator.com/item?id=42902936).

[compositional tasks](https://news.ycombinator.com/item?id=42905453).

[Chiang interview](https://news.ycombinator.com/item?id=42907268)

[LLMs: harmful to technical innovation?](https://evanhahn.com/llms-and-technical-innovation/)

[Chat is a bad UI pattern for development tools](https://news.ycombinator.com/item?id=42934190)

[Why LLMs still have problems with OCR](https://news.ycombinator.com/item?id=42966958)

[The LLM Curve of Impact on Software Engineers](https://news.ycombinator.com/item?id=42969100)

[Classic Data science pipelines built with LLMs](https://news.ycombinator.com/item?id=42990036)

[o'reilly](https://www.reddit.com/r/programming/comments/1ijlqpd/tim_oreilly_has_good_news_and_bad_news_about_your/)

[Rant about Language Mixing in <think> ... </think>](https://www.reddit.com/r/LocalLLaMA/comments/1iioooo/rant_about_language_mixing_in_think_think/)

[Emerging Patterns in Building GenAI Products](https://martinfowler.com/articles/gen-ai-patterns/)

[The DeepSeek Series: A Technical Overview](https://martinfowler.com/articles/deepseek-papers.html)

[GitHub Copilot: The agent awakens](https://github.blog/news-insights/product-news/github-copilot-the-agent-awakens/). [agent mode](https://youtu.be/KSxUr0BU9ig).

[LIMO: Less Is More for Reasoning](https://news.ycombinator.com/item?id=42991676)

[A Gentle Introduction to Positional Encoding in Transformer Models, Part 1](https://machinelearningmastery.com/a-gentle-introduction-to-positional-encoding-in-transformer-models-part-1/)

[Making Copilot Chat an expert in your workspace](https://code.visualstudio.com/docs/copilot/workspace-context)

[Introducing GitHub Copilot Next Edit Suggestions](https://www.youtube.com/watch?v=mbUnwaSllTY)

[Making Tea While AI Codes: A Practical Guide to AI-assisted programming (with Cursor Composer Agent in YOLO mode)](https://www.makingdatamistakes.com/making-tea-while-ai-codes-a-practical-guide-to-2024s-development-revolution/)

[stifling tech adoption?](https://www.reddit.com/r/programming/comments/1ioclg8/ai_is_stifling_tech_adoption/)

[is mathematics obsolete?](https://www.andrew.cmu.edu/user/avigad/Papers/obsolete.pdf)

[llm patterns: reranker](https://martinfowler.com/articles/gen-ai-patterns/#reranker)

[My LLM codegen workflow](https://news.ycombinator.com/item?id=43094006)

[vibe coding](https://mastodon.gal/@GossiTheDog@cyberplace.social/114088093941507129)

[ai patterns: fine-tuning](https://martinfowler.com/articles/gen-ai-patterns/#fine-tuning)

[MIT 6.S184: Introduction to Flow Matching and Diffusion Models](https://news.ycombinator.com/item?id=43238893)

[Getting the most out of GitHub Copilot's free tier](https://www.youtube.com/watch?v=z7JVTxiVcNk)

[Cursor experience](https://hachyderm.io/@testobsessed@ruby.social/114111592141545153)

[a ton of time-consuming chaos](https://hachyderm.io/@tao@mathstodon.xyz/114145014868441058)

[Here’s how I use LLMs to help me write code](https://simonwillison.net/2025/Mar/11/using-llms-for-code/)

[whishper](https://bsky.app/profile/ed3d.net/post/3lkguhkeae22x)

[from screenshot to code](https://youtube.com/shorts/QjvGFMTrHeQ?si=i2yx7SiLR6GkiHoL)

[AI Blindspots](https://ezyang.github.io/ai-blindspots/). [hn](https://news.ycombinator.com/item?id=43414393).

> agentic LLMs like Sonnet will proactively load files into its context, read them, and do planning based on what it sees

[Prompting Isn't Enough: What I Learned When Switching from ChatGPT to Claude's MCP](https://www.reddit.com/r/ClaudeAI/comments/1jgmrvi/prompting_isnt_enough_what_i_learned_when/)

[Latest Memo: The role of developer skills in agentic coding](https://martinfowler.com/articles/exploring-gen-ai.html#memo-13)

[AI agents: Less capability, more reliability, please](https://news.ycombinator.com/item?id=43535653)

[mcp servers explained](https://www.youtube.com/watch?v=Wp0p7iKH6ho).

[why I stopped](https://www.reddit.com/r/programming/s/c5elM8asNf)

[Reasoning models don't always say what they think](https://news.ycombinator.com/item?id=43572374)

[d on natural language programmign](https://news.ycombinator.com/item?id=43564386)

[fixing llm code](https://www.reddit.com/r/ExperiencedDevs/comments/1jqp3s3/i_now_spend_most_of_my_time_debugging_and_fixing/)

[Why you should maintain a personal LLM coding benchmark](https://bsky.app/profile/jalonso.bsky.social/post/3llyfwpbnwk2o)

[Latest Memo: The role of developer skills in agentic coding](https://martinfowler.com/articles/exploring-gen-ai.html#memo-13)

[talking with your logs](https://bsky.app/profile/gergely.pragmaticengineer.com/post/3lmezt5wjoc23)

[Obituary for Cyc | Lobsters](https://lobste.rs/s/ab6qap/obituary_for_cyc). [hn](https://news.ycombinator.com/item?id=43625474).

[VS Code Agent Mode](https://www.youtube.com/watch?v=dutyOc_cAEU). [Incorporación de instrucciones personalizadas del repositorio para GitHub Copilot](https://docs.github.com/es/copilot/customizing-copilot/adding-repository-custom-instructions-for-github-copilot). [references (how they differ from context?)](). [@workspace](https://code.visualstudio.com/docs/copilot/reference/workspace-context).

> Custom instructions are not visible in the Chat view or inline chat, but you can verify that they are being used by Copilot by looking at the References list of a response in the Chat view. 

[Ask questions about your project](https://docs.github.com/en/copilot/using-github-copilot/copilot-chat/getting-started-with-prompts-for-copilot-chat#ask-questions-about-your-project)

> To give Copilot the correct context, try some of these strategies:
>
> Highlight relevant lines of code.
> Use chat variables like #selection, #file, #editor, #codebase, or #git.
> Use the @workspace chat participant.

[How People Are Really Using Gen AI in 2025](https://hbr.org/2025/04/how-people-are-really-using-gen-ai-in-2025?ab=HP-hero-latest-2)

[we already copy-pasted a lot](https://bsky.app/profile/moultano.bsky.social/post/3lml55eprt22a)

[the bitter prediction](https://news.ycombinator.com/item?id=43662686)

[The Only 3 Videos You Need to Get Started with MCP!](https://www.youtube.com/watch?v=YRfOiB0Im64)

[Guiding an LLM for Robust Java ByteBuffer Code](https://martinfowler.com/articles/exploring-gen-ai/14-guiding-llm-java-bytebuffer.html)

[mcp 3 of 3](https://youtube.com/shorts/kcE14wp1qZQ?si=PTEqlI4f4kKJGqVc)

[VS Code Live: Coding with Gemini in GitHub Copilot](https://www.youtube.com/watch?v=anVJ3tktOh4)

[Watching o3 guess a photo’s location is surreal, dystopian and wildly entertaining](https://simonwillison.net/2025/Apr/26/o3-photo-locations/)   

[Avoiding skill atrophy in the age of AI](https://news.ycombinator.com/item?id=43791474)

[overbuilding evals](https://softwaredoug.com/blog/2025/04/26/stop-overbuilding-evals)

[Chain-of-Vibes](https://blog.thepete.net/blog/2025/04/14/chain-of-vibes/)

[Sycophancy in GPT-4o](https://news.ycombinator.com/item?id=43840842). [more](https://news.ycombinator.com/item?id=43870819)

[DeepSeek-Prover-V2](https://news.ycombinator.com/item?id=43847432)

[Ask, Edit, & Agent - In-depth Overview of GitHub Copilot Chat Modes](https://www.youtube.com/watch?v=s7Qzq0ejhjg)

[claude integrations](https://news.ycombinator.com/item?id=43859536)

[Cursor vs VSCode Copilot (May 2025 edition)](https://www.reddit.com/r/vscode/comments/1kd58ct/cursor_vs_vscode_copilot_may_2025_edition/)

[What are tools in agent mode?](https://www.youtube.com/shorts/Nsc1hI2wp7M)

[Transformer Circuits Thread](https://transformer-circuits.pub/). [post](https://bsky.app/profile/theophite.bsky.social/post/3lolzxgd3ks25).

[would it still be worth it?](https://bsky.app/profile/opinionhaver.bsky.social/post/3lorqadet422m)

[The Unreasonable Effectiveness of an LLM Agent Loop with Tool Use](https://sketch.dev/blog/agent-loop). [hn](https://news.ycombinator.com/item?id=43998472). [fomo](https://x.com/thorstenball/status/1922950526234226917). [moar fomo]().

[ai evals](https://x.com/sh_reya/status/1917274841440477335). [evaluation guidebook](https://github.com/huggingface/evaluation-guidebook).

[Embeddings are underrated (2024)](https://news.ycombinator.com/item?id=43963868)

[Writing an LLM from scratch, part 13 – attention heads are dumb](https://news.ycombinator.com/item?id=43931366)

[Build a Weather App with Agent Mode](https://youtu.be/uG5Vcjr5vxQ)

[VS Code, Live — Straight from Microsoft Build!](https://www.youtube.com/live/DH-5LuvRFqA). [2](https://www.youtube.com/watch?v=7DxfZFjHCCE). 

[Stop Building AI Tools Backwards](https://hazelweakly.me/blog/stop-building-ai-tools-backwards/)

[Claude Code SDK](https://docs.anthropic.com/en/docs/claude-code/sdk) [HN](https://news.ycombinator.com/item?id=44032777)

[LLM function calls don't scale; code orchestration is simpler, more effective](https://news.ycombinator.com/item?id=44053744)

A pattern: resort to RAG when a document is too big for the supported context.

[The Backstory of Backpropagation](https://yuxi-liu-wired.github.io/essays/posts/backstory-of-backpropagation/)

[ow much the big Other is synonymous with language itself](https://bsky.app/profile/jjoque.bsky.social/post/3lpxjqdc33k22)

[Using Veo 3 to create fictional product reviews](https://bsky.app/profile/emollick.bsky.social/post/3lpxx7g6hwk2y)

[Claude 4 System Cards Highlights](https://news.ycombinator.com/item?id=44085920). [Highlights from the Claude 4 system prompt](https://simonwillison.net/2025/May/25/claude-4-system-prompt/).

[My LLM codegen workflow atm](https://harper.blog/2025/02/16/my-llm-codegen-workflow-atm/). [resemble warehouse work](https://news.ycombinator.com/item?id=44087150). [claude code does our releases now](https://news.ycombinator.com/item?id=44093675).

[Infinite Tool Use](https://news.ycombinator.com/item?id=44086094)

[the genie has terrible timing for design](https://www.linkedin.com/posts/kentbeck_a-problem-im-having-augmented-coding-is-activity-7328422517025452032-Fwxi)

[What even is a small language model now?](https://news.ycombinator.com/item?id=44048751)

[Why Your AI Coding Assistant Keeps Doing It Wrong, and How To Fix It](https://blog.thepete.net/blog/2025/05/22/why-your-ai-coding-assistant-keeps-doing-it-wrong-and-how-to-fix-it/)

[A Survey on Mixture of Experts in Large Language Models](https://arxiv.org/abs/2407.06204).

[custom instrunctions in vscode](https://bsky.app/profile/vscode.dev/post/3lqfzyz3r7n2c)

[interacting with raw models](https://bsky.app/profile/theophite.bsky.social/post/3lqjadgijsk2w). [in your own voice](https://bsky.app/profile/theophite.bsky.social/post/3lqky37vfbk2w).

[reasoningGym](https://news.ycombinator.com/item?id=44157077)

[vibe coding example](https://blog.ezyang.com/2025/06/vibe-coding-case-study-scubaduck/)

[Claude Code Is My Computer](https://news.ycombinator.com/item?id=44170967).

[all nutz](https://news.ycombinator.com/item?id=44163063).

[ai & humanities](https://news.ycombinator.com/item?id=44166102)

[Video scraping: extracting JSON from a 35s screen capture for 1/10th of a cent](https://news.ycombinator.com/item?id=41869128)

[commit_delay for better performance: a PostgreSQL benchmark](https://www.cybertec-postgresql.com/en/commit_delay-performance-postgresql-benchmark/).

[agents example with Codex](https://martinfowler.com/articles/exploring-gen-ai/autonomous-agents-codex-example.html)

[the illusion of thinking](https://garymarcus.substack.com/p/a-knockout-blow-for-llms). [reddit](https://www.reddit.com/r/MachineLearning/comments/1l5hzhs/r_apple_research_the_illusion_of_thinking/). [more](https://x.com/BlackHC/status/1932193272484819345).

[mcp-server (Haskell)](https://www.reddit.com/r/haskell/comments/1l7eipe/ann_mcpserver_an_awesome_framework_for_building/). [langchain-hs](https://hackage.haskell.org/package/langchain-hs).

[Extending agent mode in VScode](https://www.youtube.com/watch?v=T44T55wvDD0)

[Tracking Copilot vs. Codex vs. Cursor vs. Devin PR Performance](https://news.ycombinator.com/item?id=44188839)

[content creation apocalypse](https://bsky.app/profile/zachweinersmith.bsky.social/post/3lrfv4ftw2k2g)

[debezium for RAG](https://debezium.io/blog/2025/05/19/debezium-as-part-of-your-ai-solution/)

[TDD agents and coding with Beck](https://newsletter.pragmaticengineer.com/p/tdd-ai-agents-and-coding-with-kent)

[weird o3](https://bsky.app/profile/theophite.bsky.social/post/3lrjb7clqrc2b)

[Q-learning is not yet scalable](https://seohong.me/blog/q-learning-is-not-yet-scalable/). [hn](https://news.ycombinator.com/item?id=44279850).

[Writing documentation for AI: best practices](https://docs.kapa.ai/improving/writing-best-practices). [about comments](https://bsky.app/profile/tonofcrates.bsky.social/post/3lrt6jgu5ic2m)

[MCP library and server for Haskell (by Claude)](https://www.reddit.com/r/haskell/comments/1lerjf4/mcp_library_and_server_for_haskell_by_claude/)

[ai curmudgeon](https://lobste.rs/s/imjzlb/why_i_won_t_use_ai)

[Programming Language Design in the Era of LLMs: A Return to Mediocrity?](https://kirancodes.me/posts/log-lang-design-llms.html)

[LLMs and PMs](https://bsky.app/profile/carnage4life.bsky.social/post/3lry3gl35q22j)

[well, hopefully](https://bsky.app/profile/hikikomorphism.bsky.social/post/3lryhqugsfc2o)

[Remote MCP Support in Claude Code](https://news.ycombinator.com/item?id=44312363)

[opinion](https://bsky.app/profile/eva.town/post/3ls7pnr2ug22m). [opinion](https://bsky.app/profile/theophite.bsky.social/post/3lsaxi4jgjk2a).

My success cases:
    - adding the skeleton of a tasty testsuite to a Haskell program.

[the bitter lesson is coming for tokenization](https://news.ycombinator.com/item?id=44366494)

[mcp is eating the world](https://news.ycombinator.com/item?id=44338793)

[Basic facts about GPUs](https://damek.github.io/random/basic-facts-about-gpus/). [hn](https://news.ycombinator.com/item?id=44365320).

[LLMs bring new nature of abstraction](https://martinfowler.com/articles/2025-nature-abstraction.html)

[Gemini CLI](https://news.ycombinator.com/item?id=44376919). [SW thoughts](https://hachyderm.io/@simon@simonwillison.net/114745287942496470). [the prompt](https://hachyderm.io/@simon@simonwillison.net/114745293831690891).

[anthropomorphize](https://bsky.app/profile/steveklabnik.com/post/3lsjnncpaes23)

[normalizing flows](https://news.ycombinator.com/item?id=44400105)

[life of an inference request](https://news.ycombinator.com/item?id=44407058)

[good or bad analogy?](https://bsky.app/profile/simonwillison.net/post/3lt2xbayttk2h)

[baba is eval](https://news.ycombinator.com/item?id=44455124)

[A non-anthropomorphized view of LLMs](https://news.ycombinator.com/item?id=44484682)

[Buenas prácticas para dominar GitHub Copilot Chat](https://www.youtube.com/watch?v=KRh1_ZU2g8E)

[example of debugging with Claude](https://bsky.app/profile/utopia-defer.red/post/3ltgbvflyvc25)

[how I build software quickly](https://lobste.rs/s/zlm4fp/how_i_build_software_quickly)

[role-playing in llms](https://bsky.app/profile/aelkus.bsky.social/post/3ltkdf26zy22m). [Role play with large language models](https://www.nature.com/articles/s41586-023-06647-8).

[ETH Zurich and EPFL to release a LLM developed on public infrastructure](https://ethz.ch/en/news-and-events/eth-news/news/2025/07/a-language-model-built-for-the-public-good.html). [hn](https://news.ycombinator.com/item?id=44535637).

[Leading your engineers towards an AI-assisted future](https://blog.thepete.net/blog/2025/06/26/leading-your-engineers-towards-an-ai-assisted-future/)

[Best way to share project structure with the LLMs?](https://www.reddit.com/r/softwarearchitecture/s/Npu9ZbSoCf)

[Understanding Tool/Function Calling in LLMs (Step-by-Step Examples in REST and Spring AI)](https://muthuishere.medium.com/understanding-tool-function-calling-in-llms-step-by-step-examples-in-rest-and-spring-ai-2149ecd6b18b)

[claude code for debugging](https://www.reddit.com/r/ClaudeAI/s/GfuPtz4A7k)

[LLM Inference Handbook](https://news.ycombinator.com/item?id=44527947)

[[r/ClaudeAI] Claude Code Tip Straight from Anthropic: Go Slow to Go Smart](https://www.reddit.com/r/ClaudeAI/s/mqMxRoSSG7)

[VScode custom chat mode](https://youtube.com/shorts/AbtzkXIkwCE)

[Is the doc bot docs, or not?](https://lobste.rs/s/iq4abk/is_doc_bot_docs_not)

[Adding a feature because ChatGPT incorrectly thinks it exists](https://news.ycombinator.com/item?id=44491071)


