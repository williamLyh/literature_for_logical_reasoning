# Literature_for_logical_reasoning_generation
In particular, the ability to derive reasoned conclusions from stated knowledge suggests new opportunities for explainability, correctability/machine instruction, and counterfactual reasoning in question-answering. (quoted from *Transformers as Soft Reasoners over Language*)  

## Literature for logical reasoning
* Johan Bos's line of research
  * [Recognising Textual Entailment with Logical Inference](https://aclanthology.org/H05-1079.pdf)
  * Boxer: [Wide-Coverage Semantic Analysis with Boxer](https://aclanthology.org/W08-2222.pdf), brief description [Open-Domain Semantic Parsing with Boxer](https://aclanthology.org/W15-1841.pdf)(NODALIDA 2015)
   * Some helpful link to complie Boxer: [discussion](https://github.com/nltk/nltk/issues/1612)
   * [new candc installation](https://github.com/chrzyki/candc) 
   * [nltk boxer tool](https://www.nltk.org/_modules/nltk/sem/boxer.html)

* [Reasoning Like Program Executors](https://arxiv.org/pdf/2201.11473.pdf)
* [Neural Unification for Logic Reasoning over Natural Language](https://arxiv.org/pdf/2109.08460.pdf)
* [Improving Coherence and Consistency in Neural Sequence Models with Dual-System, Neuro-Symbolic Reasoning](https://arxiv.org/pdf/2107.02794.pdf)

## Literature for DRS parsing 
* [Exploring Neural Methods for Parsing Discourse Representation Structures](https://aclanthology.org/Q18-1043.pdf)
* Jiangming Liu's line of reasearch:
  * [Discourse Representation Structure Parsing](https://aclanthology.org/P18-1040.pdf)
  * [DRTS Parsing with Structure-Aware Encoding and Decoding](https://aclanthology.org/2020.acl-main.609.pdf)(acl 2020, Qiankun Fu and Jiangming Liu) Structure aware DRS parser (Likely the latest DRS parser).
## Literature for FOL parsing
* [Exploring Neural Models for Parsing Natural Language into First-Order Logic](https://arxiv.org/pdf/2002.06544.pdf)(2020): A general purpose open-domain neural FOL parser. Treat as a Seq2Seq transduction problem. Encoder and decoder are both LSTM-based with attention. Results seem not good enough to work as a tool.

## Theorem Proving 
* [Towards Neural Theorem Proving at Scale](https://arxiv.org/pdf/1807.08204.pdf)
* [End-to-End Differentiable Proving](https://arxiv.org/pdf/1705.11040.pdf)
* Symbolic theorem prover [Prolog](): Symbolic provers lack the ability to **learn subsymbolic representations** and similarities between them from large KBs, which limits their ability to generalize to queries with similar but not identical symbols.


## Inductive Logic Programming
ILP builds upon Symbolic Theorem Procers to learn interpretable rules from data and to exploit them for reasoning in KBs.  
* [Inductive Logic Programming At 30: A New Introduction](https://arxiv.org/pdf/2008.07912.pdf)[2022, Andrew Cropper]  ML induces a hypothesis (also called a model) that generalises training examples (observations). ILP uses logic programs to represent data and learns relations instead of functions.
* [Neural, Symbolic and Neural-Symbolic Reasoning on Knowledge Graphs](https://arxiv.org/pdf/2010.05446.pdf)[2021] Symbolic reasoning aims at deducing general logic
rules from the knowledge graphs. The entities derived from the given head entity and the query relation following the logic rules are returned as the answers.Existing symbolic reasoning methods are mainly the search-based ILP methods, which usually search and prune rules.

## Literature for soft reasoning & neural reasoning
* Bostrom's line of research 
  * [Flexible Generation of Natural Language Deductions](https://arxiv.org/pdf/2104.08825.pdf)[2021 EMNLP] An **interpretable system for open-domain reasoning** needs to express its reasoning process in a transparent form.
  * [Natural Language Deduction through Search over Statement Compositions](https://arxiv.org/pdf/2104.08825.pdf):
* Allen's AI:
  * [Transformers as Soft Reasoners over Language](https://arxiv.org/pdf/2002.05867.pdf)[IJCAI 2020, P. Clark][[demo](https://rule-reasoning.apps.allenai.org)] They collect datasets, which are binary classification task of format consisting context(rule, fact) + statement + answer(T/F). They take transformer directly as a neural theorem prover. As a result, the logical axioms and query can be replaced by natural language. On the contrary, the neural networks are fault-tolerant, as they learn the abstract semantics and further compare these embeddings instead of the literal meaning between entities and relations by symbolic representations.  

Typically, there are three main combination methodologies. The first kind targets at neural reasoning but leverages the logic rules to improve the embeddings in neural reasoning, named as *symbolic-driven neural reasoning*. The second kind replaces the neural reasoning with a probabilistic framework, i.e., builds a probabilistic
model to infer the answers, where the logic rules are designed as features in the probabilistic model, which is named as *symbolic-driven probabilistic reasoning*. And the third kind aims to infer rules by symbolic reasoning, but incorporates the neural networks to deal with the uncertainty and ambiguity of data. This kind of methods also reduces the search space in symbolic reasoning, which are named as *neural-driven symbolic reasoning*.
 
* [Reasoning about Entailment with Neural Attention](https://arxiv.org/pdf/1509.06664.pdf)
* [Towards Neural Network-based reasoning](https://arxiv.org/pdf/1508.05508.pdf)[2015, Baolin Peng] Neural Reasoner can infer over multiple supporting facts and find an answer to the question in specific forms

## Literature for Natural logic(Lambda Logical Forms LLFs)
* [NaturalLI: Natural Logic Inference for Common Sense Reasoning*](https://nlp.stanford.edu/pubs/angeli2014-emnlp-naturalli.pdf)(EMNLP 2014, G. Angeli and C. Manning): Natural Logic inference cast as search. Each step of the search tree has branches of all relations types (MacCartney relations). The sequence of logic relations can be expressed as a finite state automaton.
* [Natural Solution to FraCaS Entailment Problems](https://aclanthology.org/S16-2007.pdf)(SEM 2016, L. Abzianidze)
* [LANGPRO: Natural Language Theorem Prover](https://aclanthology.org/D17-2020.pdf)(EMNLP 2017, L. Abzianidze): Based on analytic tableau method designed for natural logic. Pipeline includes CCG parser, LLF generator and NLogProver. However, rules used by the prover are manually collected according to the development data (might suggest bad at generalization). Good performance on FraCaS and SICK textual entailment dataets.
* [Natural Language Inference with Monotonicity](https://aclanthology.org/W19-0502.pdf)(ACL 2019, H. Hu and L. Moss)
* [Exploring End-to-End Differentiable Natural Logic Modeling](https://aclanthology.org/2020.coling-main.101.pdf)(COLING 2020, Yufei Feng and Xiaodan Zhu)
* [A Logic-Driven Framework for Consistency of Neural Models](https://aclanthology.org/D19-1405.pdf)(EMNLP 2019, Tao Li and V. Srikumar)
* [Natural Language Inference in Context — Investigating Contextual Reasoning over Long Texts](https://arxiv.org/pdf/2011.04864.pdf)[2021 AAAI, Hanmeng Liu and Yue Zhang] They introduce ConTRoL dataset for contextual reasoning over long texts. The task has long premise and 3-way entailment classification. It can also serve as a testing-set for checking factual correctness of summaries.

## Logical fact verification 
* [LOREN: Logic-Regularized Reasoning for Interpretable Fact Verification](https://arxiv.org/pdf/2012.13577.pdf) (AAAI 2022): Decompose the verification of the whole claim at phrase-level. The veracity of each phrase is 3-valued. The veracity of the whole claim is based on rules over veracities of all phrases.
* [ProoFVer: Natural Logic Theorem Proving for Fact Verification](https://arxiv.org/pdf/2108.11357.pdf) (2021): Using Natural Logic and a deterministic finite state automaton. The veracity of a claim is determined based on the seqeunce of natural logic relations in the proof. Each natural logic relation is got by comparing a span in the claim and spans in a set of retrieved evidence.

## Neuro-Symbolic Reasoning
* [An Interpretable Neuro-Symbolic Reasoning Framework for Task-Oriented Dialogue Generation](https://arxiv.org/pdf/2203.05843.pdf) (ACL 2022): They focus on task-oriented dialogue system. Apply logic chain reasoning with a hypothesis generator and a reasoner(chain verfication). The chains and dialogue responses are triples with entities from dialogue and KB.
* [Neural-Symbolic Learning and Reasoning: A Survey and Interpretation](https://arxiv.org/pdf/1711.03902.pdf) [2017]

## Generation sampling
* [CGMH: Constrained Sentence Generation by Metropolis-Hastings Sampling](https://arxiv.org/pdf/1811.10996.pdf)

## Datasets
* Recognising Textual Entailment tasks
  * [LogiQA: A Challenge Dataset for Machine Reading Comprehension with Logical Reasoning](https://arxiv.org/pdf/2007.08124.pdf)
  * [CLUTRR: A Diagnostic Benchmark for Inductive Reasoning from Text](https://arxiv.org/pdf/1908.06177.pdf)
  * FraCaS
  * SICK
* Reasoning
  * [QASC: A Dataset for Question Answering via Sentence Composition](file:///C:/Users/51227/OneDrive/phd/papers/6319-Article%20Text-9544-1-10-20200517.pdf): 2-hop multiple choice questions. Need to retrieve knowledge from fact corpus. 
* [QuAC : Question Answering in Context](https://arxiv.org/pdf/1808.07036.pdf)[2018, Eunsol Choi, Yejin Choi, Percy Liang, Luke Zettlemoyer] Question Answering in Context, under dialog structure, 14K QA dialogs, 100K questions. 
 
* Entailment Generation tasks
* Story Generation datasets
  * [Counterfactual Story Reasoning and Generation](https://arxiv.org/pdf/1909.04076.pdf)[EMNLP 2019, Lianhui Qin, Yejin Choi] Given a premise (story background) and an alternative initial, the task is to rewrite the following stories according to the counterfactual initial. 
