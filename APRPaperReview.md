# APR Paper Review

***Title***: MORepair: Teaching LLMs to Repair Code via Multi-Objective Fine-tuning

***Conf/Jour***: TOSEM'2025

***Summary***: 训练时将<bug, patch>进化为<bug, patch, description>从而让LLM能够更深入理解修复逻辑

***Thinking***:
- llm生成的patch的performance有研究过么，相比较人类的，或者会不会引入performance bug
- test suite通过了就能认为patch是正确的么，这些test suite与bug之间的对应关系是什么样的；如果test suite不能覆盖这些bug，那应该考虑在生成patch的同时生成对应test，这是开源软件pr中的常见操作
- llm生成的description准确率不算高，有人做过用llm对patch做理解么(好像没什么实际价值，manybe从csedu的角度有点意义)

**************************************************

***Title***: A Survey of LLM-based Automated Program Repair: Taxonomies, Design Paradigms, and Applications

***Conf/Jour***: TBD

***Summary***: LLM-based APR主要分为Fine-tuning, prompting, procedural, agentic

***Thinking***:
- 2.1 Huang et al.: 既然需要"massive candidate patches",会不会有一种情况that patch1可以fix bug中的问题1 patch2可以fix bug中的问题2，我们只需要一种算法(有点像怎么做mutate?)去结合不同的patch从而让修复的收敛速度变快
- 3.1 AlphaRepair: "predicting the fixed codes directly instead of learning edit scripts" 这是否意味着相比起让llm看buggy code然后修复，直接把buggy code给mask然后让llm做completion会更好
- 4.2 HULA/6-Evaluation reliability: "beyond unit tests"/“produces a plausible patch that passes... but still contains hidden errors”所以到底这些APR benchmark中test suite对于patch or bug的覆盖率如何，真的能反应成功率么，引入的hidden error到底是指对原本bug修复不完全还是regression error；在Sys领域似乎不太会用test suite作为评价repair的metri
- 4.3 RAGFix: "projects that rely on proprietary APIs may ..."结合一下documentation呢
- 4.5: "prioritizing feedback according to its information value" 能不能先让llm理解bug然后生成一个test case作为oracle，从而用execution result 作为feedback去guide llm的patch生成
- 6-Security and trust: "slow the program" patch的质量问题

**************************************************

***Title***: Unlocking LLM Repair Capabilities in Low-Resource Programming Languages Through Cross-Language Translation and Multi-Agent Refinement

***Conf/Jour***: TBD

***Summary***: 遇到修复不了的bug，先转译成别的语言，借助别的语言的特性(rust的安全性、C的底层操作)尝试修复，再转译回来

***Thinking***:
- 2.2: "AgentCoder integrates specialized .. for ... test generation" 这是指他们会同步生成test来辅助repair么，有空看一下⚠️
- 3: "Rust's language specific features..." 如果对于bug描述的足够清晰，比如对于fig1的example说清楚performance issue，那原始语言修复不可以么？是不是问题其实是出在对于bug的description不清晰导致很多时候llm的patch错误/不完善
- 4.2 Historical Data Storage & Retrieval: "problem difficulty" 这个是怎么量化的，这竟然对guide llm做patch generation有影响
- 现在的APR工具是否有能够同时生成包含多个语言的patch，因为在例如微服务系统往往是多语言的，一个bug可能是cross-language&multi-module(file)的

**************************************************

***Title***: AgentCoder: Multi-Agent Code Generation with Effective Testing and Self-optimisation

***Conf/Jour***: TBD

***Summary***: 一个agent生成code一个agent生成test，用test execution feedback来refine code

***Thinking***:
- test和patch的两个generation agent互相不知道对方生成了什么，从而避免互相干扰
- 这篇其实不是APR而是为了code generation，test是为了矫正生成的code，所以pipeline没有为repair做特别设计
- test generation通过prompt指明了需要注意corner case

**************************************************

***Title***: Repair-R1: Better Test Before Repair

***Conf/Jour***: TBD

***Summary***: 思路和MORepair很像，训练时将<bug, patch>进化为<bug, patch, test case>从而让LLM能够更深入理解修复逻辑

***Thinking***:
- Figure3: 从prompt看出其实所谓的test只包含assertion(assert func(input_paras) cmp_op expected_res)，在真实系统的bug里仅通过不同input_paras是不会能够cover所有path的，只使用这种assertion忽略了系统状态且只能用于单元测试
- 不是特别清楚引入Reference Model计算这个KL对于结果的意义是什么，基于什么样的motivation，或许是RL里的常见做法(?)
- AgentCoder和Repair-R1两篇都是思考如何利用test code去提升，一个在推理阶段一个在训练阶段，但是1)没有看到generated tests的覆盖率且2)Repair-R1并没有生成完全的test case，assertion能力有限


**************************************************

***Title***: RepairAgent: An Autonomous, LLM-Based Agent for Program Repair

***Conf/Jour***: 

***Summary***: 

***Thinking***:

**************************************************

***Title***: Input Reduction Enhanced LLM-based Program Repair

***Conf/Jour***: 

***Summary***: 

***Thinking***:

**************************************************

***Title***: APRMCTS: Improving LLM-based Automated Program Repair with Iterative Tree Search

***Conf/Jour***: ASE'25

***Summary***: 

***Thinking***:


