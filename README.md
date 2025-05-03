# LLM-Agent-Safety-Paper-List

A curated collection of research papers, articles, and resources focused on the safety, trustworthiness, and robustness of autonomous agents driven by LLMs/LMMs. It covers key topics such as attacks, defenses, and evaluations of agents, spanning various types, including Web Agents, Tool Agents, Communicative Agents, RAG Systems, OS Agents, and more. This repository aims to serve as a reference for researchers, practitioners, and enthusiasts working in the field of Agent Safety.

## Table of Content
- Papers
    - [1. Web Agents](#1-web-agents)
    - [2. Tool Agents / RAG Systems](#2-tool-agents--rag-systems)
    - [3. Communicative Agents](#3-communicative-agents)
    - [4. OS Agents](#4-os-agents)
    - [5. Benchmark / Survey / Position Papers](#5-benchmark--survey--position-papers)
- Contributing
    - [1. Add Papers](#1-add-papers)
    - [2. Format Example](#2-format-example)
    - [3. Contributors](#3-contributors)

## Papers
### 1. Web Agents

- [EIA: Environmental Injection Attack on Generalist Web Agents for Privacy Leakage](https://arxiv.org/abs/2409.11295)
    - 🔑 Key: attack
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: This work conducts the first study on the privacy risks of generalist web agents in adversarial environments. It considers two adversarial targets: stealing users' specific PII or the entire user request. It proposes a novel attack method, termed Environmental Injection Attack (EIA). EIA injects malicious content designed to adapt well to environments where the agents operate and this work instantiates EIA specifically for privacy scenarios in web environments.
    - 📅 Date: Oct 04, 2024

- [AdvWeb: Controllable Black-box Attacks on VLM-powered Web Agents](https://arxiv.org/abs/2410.17401)
    - 🔑 Key: attack
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: This work provides AdvWeb, a novel black-box attack framework designed against web agents. AdvWeb trains an adversarial prompter model that generates and injects adversarial prompts into web pages, misleading web agents into executing targeted adversarial actions such as inappropriate stock purchases or incorrect bank transactions, actions that could lead to severe real-world consequences. With only black-box access to the web agent, they train and optimize the adversarial prompter model using DPO, leveraging both successful and failed attack strings against the target agent.
    - 📅 Date: Oct 29, 2024

- [Watch Out for Your Agents! Investigating Backdoor Threats to LLM-Based Agents](https://arxiv.org/abs/2402.11208)
    - 🔑 Key: attack
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: This work takes the first step to investigate one of the typical safety threats, backdoor attack, to LLM-based agents. They first formulate a general framework of agent backdoor attacks, then present a thorough analysis on the different forms of agent backdoor attacks. Specifically, from the perspective of the final attacking outcomes, the attacker can either choose to manipulate the final output distribution, or only introduce malicious behavior in the intermediate reasoning process, while keeping the final output correct. Extensive experiments show that LLM-based agents suffer severely from backdoor attacks, indicating an urgent need for further research on the development of defenses against backdoor attacks on LLM-based agents.
    - 📅 Date: Feb 17, 2024

- [Adversarial Attacks on Multimodal Agents](https://arxiv.org/abs/2406.12814)
    - 🔑 Key: attack
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: In this paper, they show that multimodal agents raise new safety risks, even though attacking agents is more challenging than prior attacks due to limited access to and knowledge about the environment. Their attacks use adversarial text strings to guide gradient-based perturbation over one trigger image in the environment: (1) the captioner attack attacks white-box captioners if they are used to process images into captions as additional inputs to the VLM; (2) the CLIP attack attacks a set of CLIP models jointly, which can transfer to proprietary VLMs.
    - 📅 Date: Jul 18, 2024

- [Refusal-Trained LLMs Are Easily Jailbroken As Browser Agents](https://arxiv.org/abs/2410.13886)
    - 🔑 Key: attack
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: This work introduces Browser Agent Red teaming Toolkit (BrowserART), a comprehensive test suite designed specifically for red-teaming browser agents. BrowserART is consist of 100 diverse browser-related harmful behaviors (including original behaviors and ones sourced from HarmBench [Mazeika et al., 2024] and AirBench 2024 [Zeng et al., 2024b]) across both synthetic and real websites. Our empirical study on state-of-the-art browser agents reveals that, while the backbone LLM refuses harmful instructions as a chatbot, the corresponding agent does not.
    - 📅 Date: Oct 21, 2024

- [Dissecting Adversarial Robustness of Multimodal LM Agents](https://openreview.net/forum?id=LjVIGva5Ct)
    - 🔑 Key: attack
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: This work conducts the adversarial evaluation the safety of multimodal LM agents. They manually create 200 targeted adversarial tasks and evaluation scripts in a realistic threat model on top of VisualWebArena. To examine the robustness of agents, they propose the Agent Robustness Evaluation (ARE) framework. ARE views the agent as a graph showing the flow of intermediate outputs between components and decomposes robustness as the flow of adversarial information on the graph. They find that they can successfully break various latest agents that use black-box frontier LLMs, including those that perform reflection and tree search. 
    - 📅 Date: Oct 30, 2024


### 2. Tool Agents / RAG Systems

- [TrustAgent: Towards Safe and Trustworthy LLM-based Agents](https://arxiv.org/abs/2402.01586)
    - 🔑 Key: defense
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: This paper presents an Agent-Constitution-based agent framework, TrustAgent, with a particular focus on improving the LLM-based agent safety. The proposed framework ensures strict adherence to the Agent Constitution through three strategic components: pre-planning strategy which injects safety knowledge to the model before plan generation, in-planning strategy which enhances safety during plan generation, and post-planning strategy which ensures safety by post-planning inspection. 
    - 📅 Date: Oct 03, 2024

- [LLM Agents can Autonomously Hack Websites](https://arxiv.org/abs/2402.06664)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: This work shows that LLM agents can autonomously hack websites, performing tasks as complex as blind database schema extraction and SQL injections without human feedback. Importantly, the agent does not need to know the vulnerability beforehand. This capability is uniquely enabled by frontier models that are highly capable of tool use and leveraging extended context. Namely, they show that GPT-4 is capable of such hacks, but existing open-source models are not. Finally, they show that GPT-4 is capable of autonomously finding vulnerabilities in websites in the wild.
    - 📅 Date: Feb 06, 2024


- [Identifying the Risks of LM Agents with an LM-Emulated Sandbox](https://arxiv.org/abs/2309.15817)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: This work introduces ToolEmu: a framework that uses an LM to emulate tool execution and enables the testing of LM agents against a diverse range of tools and scenarios, without manual instantiation. Alongside the emulator, they develop an LM-based automatic safety evaluator that examines agent failures and quantifies associated risks. 
    - 📅 Date: May 17, 2024


- [Not what you've signed up for: Compromising Real-World LLM-Integrated Applications with Indirect Prompt Injection](https://arxiv.org/abs/2302.12173)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent, RAG System
    - 📖 TLDR: This work argues that LLM-Integrated Applications blur the line between data and instructions. They reveal new attack vectors, using Indirect Prompt Injection, that enable adversaries to remotely (without a direct interface) exploit LLM-integrated applications by strategically injecting prompts into data likely to be retrieved. They derive a comprehensive taxonomy from a computer security perspective to systematically investigate impacts and vulnerabilities, including data theft, worming, information ecosystem contamination, and other novel security risks. 
    - 📅 Date: May 05, 2023

- [Breaking Agents: Compromising Autonomous LLM Agents Through
Malfunction Amplification](https://arxiv.org/pdf/2407.20859)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: This work introduces a new type of attack that causes malfunctions by misleading the agent into executing repetitive or irrelevant actions. They conduct comprehensive evaluations using various attack methods, surfaces, and properties to pinpoint areas of susceptibility. The experiments reveal that these attacks can induce failure rates exceeding 80\% in multiple scenarios. To mitigate such attacks, they propose self-examination detection methods. However, their findings indicate these attacks are difficult to detect effectively using LLMs alone, highlighting the substantial risks associated with this vulnerability.
    - 📅 Date: Jul 30, 2024

- [Large Language Model Sentinel: LLM Agent for Adversarial Purification](https://arxiv.org/abs/2405.20770)
    - 🔑 Key: defense
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: In this paper, they introduce a novel defense technique named Large LAnguage MOdel Sentinel (LLAMOS), which is designed to enhance the adversarial robustness of LLMs by purifying the adversarial textual examples before feeding them into the target LLM. Their method comprises two main components: a. Agent instruction, which can simulate a new agent for adversarial defense, altering minimal characters to maintain the original meaning of the sentence while defending against attacks; b. Defense guidance, which provides strategies for modifying clean or adversarial examples to ensure effective defense and accurate outputs from the target LLMs. Extensive experiments on both open-source and closed-source LLMs demonstrate that the method effectively defends against adversarial attacks, thereby enhancing adversarial robustness.
    - 📅 Date: May 24, 2024

- [Frontier Models are Capable of In-context Scheming](https://static1.squarespace.com/static/6593e7097565990e65c886fd/t/6751eb240ed3821a0161b45b/1733421863119/in_context_scheming_reasoning_paper.pdf)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: Frontier models are increasingly trained and deployed as autonomous agents, which significantly increases their potential for risks. One particular safety concern is that AI agents might covertly pursue misaligned goals, hiding their true capabilities and objectives – also known as scheming. This work studies whether models have the capability to scheme in pursuit of a goal that we provide in-context and instruct the model to strongly follow.
    - 📅 Date: Dec 05, 2024

- [GuardAgent: Safeguard LLM Agents by a Guard Agent via Knowledge-Enabled Reasoning](https://arxiv.org/abs/2406.09187)
    - 🔑 Key: defense
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: The rapid rise of large language models (LLMs) has introduced safety challenges for LLM-powered agents due to their diverse objectives and outputs. To address this, GuardAgent is proposed as a guardrail system for monitoring other LLM agents, creating task plans from user-defined guard requests and generating executable code to ensure compliance. It requires no additional training, uses an extendable toolbox, and demonstrates strong generalization and low operational overhead. GuardAgent achieves high accuracy (98.7% and 90.0%) on two benchmarks for privacy and safety, highlighting its adaptability and effectiveness in moderating invalid inputs and outputs.
    - 📅 Date: Jun 13, 2024

- [Unleashing Worms and Extracting Data: Escalating the Outcome of Attacks against RAG-based Inference in Scale and Severity Using Jailbreaking](https://arxiv.org/pdf/2409.08045)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent, RAG System
    - 📖 TLDR: This paper demonstrates how jailbreaking a GenAI model enables attackers to escalate the severity and scale of attacks on RAG-based GenAI-powered applications. It shows that attackers can escalate RAG membership inference and entity extraction attacks into full RAG document extraction, retrieving up to 99.8% of database content. Additionally, attackers can amplify RAG data poisoning attacks to compromise the entire GenAI ecosystem by crafting adversarial self-replicating prompts that propagate as worms, forcing affected applications to perform malicious activities. The paper evaluates the performance factors influencing these attacks and discusses guardrails to protect against RAG-based inference attacks, highlighting trade-offs.
    - 📅 Date: Sep 06, 2024

- [RedAgent: Red Teaming Large Language Models with Context-aware Autonomous Language Agent](https://arxiv.org/pdf/2407.16667)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: This paper addresses the safety concerns of jailbreak attacks on advanced LLMs like GPT-4, which expose vulnerabilities by inducing toxic responses through adversarial prompts. To improve red teaming methods, the authors propose RedAgent, a multi-agent LLM system that generates context-aware jailbreak prompts by modeling attacks into “jailbreak strategies” and using self-reflective learning from contextual feedback. Experiments show RedAgent efficiently jailbreaks most black-box LLMs in five queries and uncovers 60 severe vulnerabilities in real-world applications with only two queries per vulnerability. The findings have been reported to OpenAI and Meta for mitigation.
    - 📅 Date: Jul 23, 2024

- [Mitigating the Privacy Issues in Retrieval-Augmented Generation (RAG) via Pure Synthetic Data](https://arxiv.org/pdf/2406.14773)
    - 🔑 Key: defense
    - 🤖 Agent Type: Tool Agent, RAG System
    - 📖 TLDR: This paper addresses privacy risks in retrieval-augmented generation (RAG) systems that use private data for retrieval by proposing SAGE, a two-stage synthetic data generation paradigm. SAGE preserves key contextual information in stage-1 using attribute-based extraction and generation, and enhances privacy in stage-2 through agent-based iterative refinement. Experiments show that SAGE achieves comparable performance to original data while significantly reducing privacy risks. This work pioneers the development of high-utility, privacy-preserving synthetic data for safer RAG applications across various domains.
    - 📅 Date: Jun 13, 2024

- [PLeak: Prompt Leaking Attacks against Large Language Model Applications](https://arxiv.org/abs/2405.06823)
    - 🔑 Key: attack
    - 🤖 Agent Type: Tool Agent, RAG System
    - 📖 TLDR: This paper designs a novel, closed-box prompt leaking attack framework, called PLeak, to optimize an adversarial query such that when the attacker sends it to a target LLM application, its response reveals its own system prompt. They formulate finding such an adversarial query as an optimization problem and solve it with a gradient-based method approximately. The key idea is to break down the optimization goal by optimizing adversary queries for system prompts incrementally, i.e., starting from the first few tokens of each system prompt step by step until the entire length of the system prompt.
    - 📅 Date: May 10, 2024

- [Optimization-based Prompt Injection Attack to LLM-as-a-Judge](https://arxiv.org/pdf/2403.17710)
    - 🔑 Key: attack, defense
    - 🤖 Agent Type: Tool Agent, RAG System
    - 📖 TLDR: This work propose JudgeDeceiver, an optimization-based prompt injection attack to LLM-as-a-Judge. JudgeDeceiver injects a carefully crafted sequence into an attacker-controlled candidate response such that LLM-as-a-Judge selects the candidate response for an attacker-chosen question no matter what other candidate responses are. The extensive evaluation shows that JudgeDeceive is highly effective, and is much more effective than existing prompt injection attacks that manually craft the injected sequences and jailbreak attacks when extended to our problem. They also show the effectiveness of JudgeDeceiver in three case studies, i.e., LLM-powered search, RLAIF, and tool selection. Moreover, they consider defenses including known-answer detection, perplexity detection, and perplexity windowed detection. The results show these defenses are insufficient.
    - 📅 Date: Nov 15, 2024

- [Poisoning Retrieval Corpora by Injecting Adversarial Passages](https://arxiv.org/abs/2310.19156)
    - 🔑 Key: attack
    - 🤖 Agent Type: RAG System
    - 📖 TLDR: This work proposes an attack for dense retrieval systems in which a malicious user generates a small number of adversarial passages by perturbing discrete tokens to maximize similarity with a provided set of training queries. When these adversarial passages are inserted into a large retrieval corpus, they show that this attack is highly effective in fooling these systems to retrieve them for queries that were not seen by the attacker.
    - 📅 Date: Oct 29, 2023

### 3. Communicative Agents

- [Agent Smith: A Single Image Can Jailbreak One Million Multimodal LLM Agents Exponentially Fast](https://arxiv.org/abs/2402.08567)
    - 🔑 Key: attack
    - 🤖 Agent Type: Communicative Agent
    - 📖 TLDR: In this work, they report an even more severe safety issue in multi-agent environments, referred to as infectious jailbreak. It entails the adversary simply jailbreaking a single agent, and without any further intervention from the adversary, (almost) all agents will become infected exponentially fast and exhibit harmful behaviors. 
    - 📅 Date: Jun 03, 2024

- [Evil Geniuses: Delving into the Safety of LLM-based Agents](https://arxiv.org/abs/2311.11855)
    - 🔑 Key: attack
    - 🤖 Agent Type: Communicative Agent
    - 📖 TLDR: This paper elaborately conducts a series of manual jailbreak prompts along with a virtual chat-powered evil plan development team, dubbed Evil Geniuses, to thoroughly probe the safety aspects of these agents. Our investigation reveals three notable phenomena: 1. LLM-based agents exhibit reduced robustness against malicious attacks. 2. the attacked agents could provide more nuanced responses. 3. the detection of the produced improper responses is more challenging.
    - 📅 Date: Dec 03, 2023

- [PsySafe: A Comprehensive Framework for Psychological-based Attack, Defense, and Evaluation of Multi-agent System Safety](https://arxiv.org/abs/2401.11880)
    - 🔑 Key: attack
    - 🤖 Agent Type: Communicative Agent
    - 📖 TLDR: This work proposes a comprehensive framework grounded in agent psychology. The framework focuses on three aspects: identifying how dark personality traits in agents might lead to risky behaviors, designing defense strategies to mitigate these risks, and evaluating the safety of multi-agent systems from both psychological and behavioral perspectives. The experiments reveal several intriguing phenomena, such as the collective dangerous behaviors among agents, agents' propensity for self-reflection when engaging in dangerous behavior, and the correlation between agents' psychological assessments and their dangerous behaviors. 
    - 📅 Date: Jan 22, 2024

- [On the Resilience of Multi-Agent Systems with Malicious Agents](https://arxiv.org/abs/2408.00989)
    - 🔑 Key: attack, defense
    - 🤖 Agent Type: Communicative Agent
    - 📖 TLDR: This paper investigates the resilience of three multi-agent collaboration systems—linear, flat, and hierarchical—against malicious agents that produce erroneous or misleading outputs. Six systems are selected and evaluated on four downstream tasks, including code generation, math problem solving, translation, and text evaluation. They design two methods, AUTOTRANSFORM and AUTOINJECT, to transform any agent into a malicious one while preserving its functional integrity. Additionally, they show the promise of improving multi-agent system resilience by demonstrating that two defense methods, introducing a mechanism for each agent to challenge others' outputs, or an additional agent to review and correct messages.
    - 📅 Date: Sep 30, 2024

- [MultiAgent Collaboration Attack: Investigating Adversarial Attacks in Large Language Model Collaborations via Debate](https://arxiv.org/abs/2406.14711)
    - 🔑 Key: attack, defense
    - 🤖 Agent Type: Communicative Agent
    - 📖 TLDR: This work studies the vulnerabilities of language model collaborations via debate. They evaluate the behavior of a network of models collaborating through debate under the influence of an adversary. They introduce pertinent metrics to assess the adversary's effectiveness, focusing on system accuracy and model agreement. Additionally, they explore inference-time methods to generate more compelling arguments and evaluate the potential of prompt-based mitigation as a defensive strategy.
    - 📅 Date: Jun 26, 2024


### 4. OS Agents

- [Attacking Vision-Language Computer Agents via Pop-ups](https://arxiv.org/abs/2411.02391)
    - 🔑 Key: attack
    - 🤖 Agent Type: OS Agent
    - 📖 TLDR: This work demonstrates that VLM agents can be easily attacked by a set of carefully designed adversarial pop-ups, which human users would typically recognize and ignore. This distraction leads agents to click these pop-ups instead of performing the tasks as usual. Integrating these pop-ups into existing agent testing environments like OSWorld and VisualWebArena leads to an attack success rate (the frequency of the agent clicking the pop-ups) of 86% on average and decreases the task success rate by 47%. 
    - 📅 Date: Nov 04, 2024
 
- [Caution for the Environment: Multimodal Agents are Susceptible to Environmental Distractions](https://arxiv.org/pdf/2408.02544)
    - 🔑 Key: attack
    - 🤖 Agent Type: OS Agent / GUI Agent
    - 📖 TLDR: This paper investigates the faithfulness of multimodal large language model (MLLM) agents in the graphical user interface (GUI) environment, aiming to address the research question of whether multimodal GUI agents can be distracted by environmental context. Experimental results reveal that even the most powerful models, whether generalist agents or specialist GUI agents, are susceptible to distractions. Furthermore, we explore the adversarial perspective and implement environment injection, demonstrating that such unfaithfulness can be exploited, leading to unexpected risks.
    - 📅 Date: Aug 05, 2024


### 5. Benchmark / Survey / Position Papers

- [A Trembling House of Cards? Mapping Adversarial Attacks against Language Agents](https://arxiv.org/abs/2402.10196)
    - 🔑 Key: position
    - 🤖 Agent Type: Web Agent, Tool Agent, Communicative Agent
    - 📖 TLDR: In this position paper, they present the first systematic effort in mapping adversarial attacks against language agents. They first present a unified conceptual framework for agents with three major components: Perception, Brain, and Action. Under this framework, they present a comprehensive discussion and propose 12 potential attack scenarios against different components of an agent, covering different attack strategies (e.g., input manipulation, adversarial demonstrations, jailbreaking, backdoors). They also draw connections to successful attack strategies previously applied to LLMs.
    - 📅 Date: Feb 15, 2024

- [Prioritizing Safeguarding Over Autonomy: Risks of LLM Agents for Science](https://arxiv.org/abs/2402.04247)
    - 🔑 Key: position
    - 🤖 Agent Type: Scientific Agent
    - 📖 TLDR: This position paper fills this gap by conducting a thorough examination of vulnerabilities in LLM-based agents within scientific domains, shedding light on potential risks associated with their misuse and emphasizing the need for safety measures. They begin by providing a comprehensive overview of the potential risks inherent to scientific LLM agents, taking into account user intent, the specific scientific domain, and their potential impact on the external environment. Then, they delve into the origins of these vulnerabilities and provide a scoping review of the limited existing works.
    - 📅 Date: Feb 07, 2024

- [The Emerged Security and Privacy of LLM Agent: A Survey with Case Studies](https://arxiv.org/abs/2407.19354)
    - 🔑 Key: survey
    - 🤖 Agent Type: General LLM Agent
    - 📖 TLDR: This survey aims to provide a comprehensive overview of the newly emerged privacy and security issues faced by LLM agents. They begin by introducing the fundamental knowledge of LLM agents, followed by a categorization and analysis of the threats, then discuss the impacts of these threats on humans, environment, and other agents. Subsequently, they review existing defensive strategies, and finally explore future trends. Additionally, the survey incorporates diverse case studies to facilitate a more accessible understanding. By highlighting these critical security and privacy issues, the survey seeks to stimulate future research towards enhancing the security and privacy of LLM agents, thereby increasing their reliability and trustworthiness in future applications.
    - 📅 Date: Jul 28, 2024

- [AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents](https://arxiv.org/abs/2410.09024)
    - 🔑 Key: benchmark
    - 🤖 Agent Type: Tool Agent
    - 📖 TLDR: This work proposes a new benchmark called AgentHarm. The benchmark includes a diverse set of 110 explicitly malicious agent tasks (440 with augmentations), covering 11 harm categories including fraud, cybercrime, and harassment. In addition to measuring whether models refuse harmful agentic requests, scoring well on AgentHarm requires jailbroken agents to maintain their capabilities following an attack to complete a multi-step task. They evaluate a range of leading LLMs, and find (1) leading LLMs are surprisingly compliant with malicious agent requests without jailbreaking, (2) simple universal jailbreak templates can be adapted to effectively jailbreak agents, and (3) these jailbreaks enable coherent and malicious multi-step agent behavior and retain model capabilities. They publicly release AgentHarm to enable simple and reliable evaluation of attacks and defenses for LLM-based agents.
    - 📅 Date: Oct 11, 2024

- [R-Judge: Benchmarking Safety Risk Awareness for LLM Agents](https://arxiv.org/abs/2401.10019)
    - 🔑 Key: benchmark
    - 🤖 Agent Type: Tool Agent, Communicative Agent
    - 📖 TLDR: This work introduces R-Judge, a benchmark crafted to evaluate the proficiency of LLMs in judging and identifying safety risks given agent interaction records. R-Judge comprises 569 records of multi-turn agent interaction, encompassing 27 key risk scenarios among 5 application categories and 10 risk types.
    - 📅 Date: Oct 05, 2024

- [Testing Language Model Agents Safely in the Wild](https://arxiv.org/abs/2311.10538)
    - 🔑 Key: benchmark
    - 🤖 Agent Type: Tool Agent, Communicative Agent
    - 📖 TLDR: This work introduces a framework for creating safe open-world tests of LMAs. They review the security challenges posed by in-the-wild testing of LMAs, and use the conclusions to motivate the rest of the work. They introduce a dataset of 57 unsafe or off-task agent outputs, and outline the design of an early-stage LLM-based test monitor which can be easily adapted to different contexts.
    - 📅 Date: Dec 03, 2023

- [AI Agents Under Threat: A Survey of Key Security Challenges and Future Pathways](https://arxiv.org/abs/2406.02630)
    - 🔑 Key: survey
    - 🤖 Agent Type: General LLM Agent
    - 📖 TLDR: This survey delves into the emerging security threats faced by AI agents, categorizing them into four critical knowledge gaps: unpredictability of multi-step user inputs, complexity in internal executions, variability of operational environments, and interactions with untrusted external entities. By systematically reviewing these threats, this paper highlights both the progress made and the existing limitations in safeguarding AI agents.
    - 📅 Date: Sep 06, 2024

- [Navigating the Risks: A Survey of Security, Privacy, and Ethics Threats in LLM-Based Agents](https://arxiv.org/pdf/2411.09523)
    - 🔑 Key: survey
    - 🤖 Agent Type: General LLM Agent
    - 📖 TLDR: This survey focuses on the various threats faced by LLM-based agents. They propose a new taxonomy of these threats and summarize their technical advancements and limitations based on this framework and taxonomy. Subsequently, they select four real-world agents (WebGPT, Voyager, PReP, ChatDev) as case studies to analyze the types of threats these agents may encounter in practical use and their underlying causes. 
    - 📅 Date: Nov 14, 2024

- [Agent Security Bench (ASB): Formalizing and Benchmarking Attacks and Defenses in LLM-based Agents](https://arxiv.org/abs/2410.02644)
    - 🔑 Key: benchmark
    - 🤖 Agent Type: Tool Agent, RAG System
    - 📖 TLDR: This work introduces Agent Security Bench (ASB), a comprehensive framework designed to formalize, benchmark, and evaluate the attacks and defenses of LLM-based agents, including 10 scenarios (e.g., e-commerce, autonomous driving, finance), 10 agents targeting the scenarios, over 400 tools, 23 different types of attack/defense methods, and 8 evaluation metrics. Based on ASB, we benchmark 10 prompt injection attacks, a memory poisoning attack, a novel Plan-of-Thought backdoor attack, a mixed attack, and 10 corresponding defenses across 13 LLM backbones with nearly 90,000 testing cases in total.
    - 📅 Date: Oct 03, 2024

- [Evaluating Cultural and Social Awareness of LLM Web Agents](https://arxiv.org/pdf/2410.23252)
    - 🔑 Key: benchmark
    - 🤖 Agent Type: Web Agent
    - 📖 TLDR: This work introduces CASA, a benchmark designed to evaluate the cultural and social awareness of LLM agents across two web-based tasks: online shopping and social discussion forums. CASA assesses LLM agents’ ability to detect and appropriately respond to norm-violating user queries and observations. The evaluation framework measures awareness coverage, helpfulness in managing user queries, and the violation rate when facing misleading web content. Benchmarking experiments reveal that LLM agents perform significantly worse in web-based environments, with less than 10% awareness coverage and over 40% violation rates. To enhance performance, we explore prompting and fine-tuning, finding that fine-tuning on culture-specific datasets improves generalization across regions, while prompting enhances task navigation. These findings highlight the necessity of benchmarking LLM agents' cultural and social awareness throughout their development.
    - 📅 Date: Feb 09, 2025
    

## Contributing
We welcome contributions to expand and improve this repository! Here’s how you can help:

### 1. Add Papers

- Fork the repository, add a paper on README, and submit a pull request.
- In your PR, please include a few keywords describing the paper, such as the agent type and paper category (e.g., attack, defense, evaluation, benchmark, survey, or position paper).

### 2. Format Example

```
- [title](paper link)
    - 🔑 Key: e.g., attack/defense/evaluation/benchmark/survey/position
    - 🤖 Agent Type: e.g., Web Agent/Tool Agent/Communicative Agent/OS Agent
    - 📖 TLDR: Brief summary of the paper.
    - 📅 Date: e.g., Jan 01, 2025
```

### 3. Contributors

- [Lingbo Mo](https://molingbo.github.io/)
- [Zeyi Liao](https://lzy37ld.github.io/)
