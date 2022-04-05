# Literature_for_logical_reasoning_generation

## Literature for logical reasoning
* Johan Bos's line of research
  * [Recognising Textual Entailment with Logical Inference](https://aclanthology.org/H05-1079.pdf)
  * Boxer: [Wide-Coverage Semantic Analysis with Boxer](https://aclanthology.org/W08-2222.pdf), brief description [Open-Domain Semantic Parsing with Boxer](https://aclanthology.org/W15-1841.pdf)

* [Reasoning Like Program Executors](https://arxiv.org/pdf/2201.11473.pdf)
* [Neural Unification for Logic Reasoning over Natural Language](https://arxiv.org/pdf/2109.08460.pdf)
* [Improving Coherence and Consistency in Neural Sequence Models with Dual-System, Neuro-Symbolic Reasoning](https://arxiv.org/pdf/2107.02794.pdf)

## Literature for DRS parsing 
* [Exploring Neural Methods for Parsing Discourse Representation Structures](https://aclanthology.org/Q18-1043.pdf)
* Jiangming Liu's line of reasearch:
  * [Discourse Representation Structure Parsing](https://aclanthology.org/P18-1040.pdf)
  * 
## Literature for FOL parsing
* [Exploring Neural Models for Parsing Natural Language into First-Order Logic](https://arxiv.org/pdf/2002.06544.pdf)(2020): A general purpose open-domain neural FOL parser. Treat as a Seq2Seq transduction problem. Encoder and decoder are both LSTM-based with attention. Results seem not good enough to work as a tool.

## Theorem Proving 
* [Towards Neural Theorem Proving at Scale](https://arxiv.org/pdf/1807.08204.pdf)

## Literature for soft reasoning & neural reasoning
* Bostrom's line of research 
  * [Flexible Generation of Natural Language Deductions](https://arxiv.org/pdf/2104.08825.pdf)
  * [Natural Language Deduction through Search over Statement Compositions](https://arxiv.org/pdf/2104.08825.pdf):
* Allen's AI:
  * [Transformers as Soft Reasoners over Language](https://arxiv.org/pdf/2002.05867.pdf)
* [Reasoning about Entailment with Neural Attention](https://arxiv.org/pdf/1509.06664.pdf)

## Logical fact verification 
* [LOREN: Logic-Regularized Reasoning for Interpretable Fact Verification](https://arxiv.org/pdf/2012.13577.pdf) (AAAI 2022): Decompose the verification of the whole claim at phrase-level. The veracity of each phrase is 3-valued. The veracity of the whole claim is based on rules over veracities of all phrases.
* [ProoFVer: Natural Logic Theorem Proving for Fact Verification](https://arxiv.org/pdf/2108.11357.pdf) (2021): Using Natural Logic and a deterministic finite state automaton. The veracity of a claim is determined based on the seqeunce of natural logic relations in the proof. Each natural logic relation is got by comparing a span in the claim and spans in a set of retrieved evidence.

## Generation sampling
* [CGMH: Constrained Sentence Generation by Metropolis-Hastings Sampling](https://arxiv.org/pdf/1811.10996.pdf)

## Datasets
* [LogiQA: A Challenge Dataset for Machine Reading Comprehension with Logical Reasoning](https://arxiv.org/pdf/2007.08124.pdf)
* [CLUTRR: A Diagnostic Benchmark for Inductive Reasoning from Text](https://arxiv.org/pdf/1908.06177.pdf)
