# Literature_for_logical_reasoning_generation

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
* [Inductive Logic Programming At 30: A New Introduction](https://arxiv.org/pdf/2008.07912.pdf)

## Literature for soft reasoning & neural reasoning
* Bostrom's line of research 
  * [Flexible Generation of Natural Language Deductions](https://arxiv.org/pdf/2104.08825.pdf)
  * [Natural Language Deduction through Search over Statement Compositions](https://arxiv.org/pdf/2104.08825.pdf):
* Allen's AI:
  * [Transformers as Soft Reasoners over Language](https://arxiv.org/pdf/2002.05867.pdf)[IJCAI 2020, P. Clark] They collect datasets, which are binary classification task of format consisting context(rule, fact) + statement + answer(T/F).
* [Reasoning about Entailment with Neural Attention](https://arxiv.org/pdf/1509.06664.pdf)
* [Towards Neural Network-based reasoning](https://arxiv.org/pdf/1508.05508.pdf)[2015, Baolin Peng] Neural Reasoner can infer over multiple supporting facts and find an answer to the question in specific forms

## Literature for Natural logic(Lambda Logical Forms LLFs)
* [NaturalLI: Natural Logic Inference for Common Sense Reasoning*](https://nlp.stanford.edu/pubs/angeli2014-emnlp-naturalli.pdf)(EMNLP 2014, G. Angeli and C. Manning): Natural Logic inference cast as search. Each step of the search tree has branches of all relations types (MacCartney relations). The sequence of logic relations can be expressed as a finite state automaton.
* [Natural Solution to FraCaS Entailment Problems](https://aclanthology.org/S16-2007.pdf)(SEM 2016, L. Abzianidze)
* [LANGPRO: Natural Language Theorem Prover](https://aclanthology.org/D17-2020.pdf)(EMNLP 2017, L. Abzianidze): Based on analytic tableau method designed for natural logic. Pipeline includes CCG parser, LLF generator and NLogProver. However, rules used by the prover are manually collected according to the development data (might suggest bad at generalization). Good performance on FraCaS and SICK textual entailment dataets.
* [Natural Language Inference with Monotonicity](https://aclanthology.org/W19-0502.pdf)(ACL 2019, H. Hu and L. Moss)
* [Exploring End-to-End Differentiable Natural Logic Modeling](https://aclanthology.org/2020.coling-main.101.pdf)(COLING 2020, Yufei Feng and Xiaodan Zhu)
* [A Logic-Driven Framework for Consistency of Neural Models](https://aclanthology.org/D19-1405.pdf)(EMNLP 2019, Tao Li and V. Srikumar)

## Logical fact verification 
* [LOREN: Logic-Regularized Reasoning for Interpretable Fact Verification](https://arxiv.org/pdf/2012.13577.pdf) (AAAI 2022): Decompose the verification of the whole claim at phrase-level. The veracity of each phrase is 3-valued. The veracity of the whole claim is based on rules over veracities of all phrases.
* [ProoFVer: Natural Logic Theorem Proving for Fact Verification](https://arxiv.org/pdf/2108.11357.pdf) (2021): Using Natural Logic and a deterministic finite state automaton. The veracity of a claim is determined based on the seqeunce of natural logic relations in the proof. Each natural logic relation is got by comparing a span in the claim and spans in a set of retrieved evidence.

## Neuro-Symbolic Reasoning
* [An Interpretable Neuro-Symbolic Reasoning Framework for Task-Oriented Dialogue Generation](https://arxiv.org/pdf/2203.05843.pdf) (ACL 2022): They focus on task-oriented dialogue system. Apply logic chain reasoning with a hypothesis generator and a reasoner(chain verfication). The chains and dialogue responses are triples with entities from dialogue and KB.

## Generation sampling
* [CGMH: Constrained Sentence Generation by Metropolis-Hastings Sampling](https://arxiv.org/pdf/1811.10996.pdf)

## Datasets
* Recognising Textual Entailment tasks
  * [LogiQA: A Challenge Dataset for Machine Reading Comprehension with Logical Reasoning](https://arxiv.org/pdf/2007.08124.pdf)
  * [CLUTRR: A Diagnostic Benchmark for Inductive Reasoning from Text](https://arxiv.org/pdf/1908.06177.pdf)
  * FraCaS
  * SICK
* Entailment Generation tasks
