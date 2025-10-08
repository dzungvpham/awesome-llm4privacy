# Awesome LLMs for Privacy

This is a collection of papers (and projects) related to the use of LLMs for privacy that I curate for my research.
The focus is on privacy applications powered by modern, decoder-only LLMs (GPT, Llama, etc.),  **not** on training data privacy (e.g., membership inference attacks, data extraction), and **not** on pre-GPT LLMs like BERT.

All of these papers are from 2023 onward.
I try to include paper links from the official publication venues whenever possible, falling back to OpenReview and then to arXiv.
I also try to include the earliest date when a paper was first submitted to arXiv.
I categorize the papers based on their goals/domains (e.g., detection vs anonymization) and further add the following tags:
- `CO` (constructive) if they are building something new or on top of some other existing work
- `EV` (evaluation) if they are evaluating/benchmarking (usually there's a novel accompanying dataset)
- `PO` (position) if they are primarily presenting a position or opinion
- `CI` if they involve the Contextual Integrity theory.

Please feel free to open an issue or a pull request if you would like to share an interesting paper that uses LLMs for privacy.
I will try to read and update the list whenever I have the time.

## Table of Contents
- [Detection](#detection)
  - [General](#general)
  - [Named Entity Recognition](#named-entity-recognition)
- [Anonymization](#anonymization)
  - [General Evaluation](#general-evaluation)
  - [General Anonymizers](#general-anonymizers)
  - [Anonymizers for Chatbot Applications](#anonymizers-for-chatbot-applications)
  - [Anonymizers for Agents](#anonymizers-for-agents)
  - [Authorship Obfuscation](#authorship-obfuscation)
  - [Special Use Case: Abstractive Summarization](#special-use-case-abstractive-summarization)
- [Miscellaneous](#miscellaneous)

## Detection
Papers that focus on detecting/assessing privacy leakages/risks or privacy policy violations:

### General
- [8/2025] [Evaluating Language Model Reasoning about Confidential Information](https://arxiv.org/abs/2508.19980) (arXiv) `EV`
- [08/2025] [LLM-as-a-Judge for Privacy Evaluation? Exploring the Alignment of Human and LLM Perceptions of Privacy in Textual Data](https://arxiv.org/pdf/2508.12158) (arXiv) `EV`
- [08/2025] [Searching for Privacy Risks in LLM Agents via Simulation](https://arxiv.org/pdf/2508.10880) (arXiv) `EV, CO, CI`
- [08/2025] [PRvL: Quantifying the Capabilities and Risks of Large Language Models for PII Redaction](https://arxiv.org/pdf/2508.05545) (arXiv) `EV`
- [06/2025] [Automated Privacy Information Annotation in Large Language Model Interactions](https://arxiv.org/abs/2505.20910) (arXiv) `EV`
- [06/2025] [Leaky Thoughts: Large Reasoning Models Are Not Private Thinkers](https://arxiv.org/abs/2506.15674) (arXiv) `EV`
- [06/2025] [Privacy Reasoning in Ambiguous Contexts](https://arxiv.org/abs/2506.12241) (arXiv) `CO, CI`
- [05/2025] [Can Large Language Models Really Recognize Your Name?](https://arxiv.org/abs/2505.14549) (arXiv) `EV`
- [05/2025] [AgentDAM: Privacy Leakage Evaluation for Autonomous Web Agents](https://arxiv.org/abs/2503.09780) (arXiv) `EV`
- [10/2024] [CLEAR: Towards Contextual LLM-Empowered Privacy Policy Analysis and Risk Generation for Large Language Model Applications](https://dl.acm.org/doi/full/10.1145/3708359.3712156) (IUI '25)
- [08/2024] [Privacy Checklist: Privacy Violation Detection Grounding on Contextual Integrity Theory](https://aclanthology.org/2025.naacl-long.86/) (NAACL '25) `CO, CI`
- [07/2024] [Trust No Bot: Discovering Personal  Disclosures in Human-LLM Conversations in the Wild](https://openreview.net/forum?id=tIpWtMYkzU) (COLM '24) `EV`
- [06/2024] [GoldCoin: Grounding Large Language Models in Privacy Laws via Contextual Integrity Theory](https://aclanthology.org/2024.emnlp-main.195/) (EMNLP '24) `CO, CI`
- [04/2024] [Evaluating LLM-based Personal Information Extraction and Countermeasures](https://www.usenix.org/conference/usenixsecurity25/presentation/liu-yupei) (USENIX '25) `EV`
- [10/2023] [Beyond Memorization: Violating Privacy via Inference with Large Language Models](https://openreview.net/forum?id=kmn0BhQk7p) (ICLR '24) `EV`

### Named Entity Recognition
(While NER is not necessarily about sensitive data detection, it's very closely related)
- [02/2024] [LinkNER: Linking Local Named Entity Recognition Models to Large Language Models using Uncertainty](https://dl.acm.org/doi/10.1145/3589334.3645414) (WWW '24) `CO`
- [05/2023] [PromptNER: Prompt Locating and Typing for Named Entity Recognition](https://aclanthology.org/2023.acl-long.698/) (ACL '23) `CO`
- [05/2023] [PromptNER: Prompting For Named Entity Recognition](https://arxiv.org/abs/2305.15444) (arXiv) `CO`

## Anonymization
Papers that study the use of LLMs for data anonymization, de-identification, sanitization, authorship obfuscation, etc. (further sub-categorized by the target evaluation domain):

### General Evaluation
- [06/2025] [MAGPIE: A dataset for Multi-AGent contextual PrIvacy Evaluation](https://arxiv.org/abs/2506.20737) (arXiv) `EV, CI`
- [04/2025] [A False Sense of Privacy: Evaluating Textual Data Sanitization Beyond Surface-level Privacy Leakage](https://www.arxiv.org/abs/2504.21035) (arXiv) `EV`
- [01/2025] [Position: Contextual Integrity Washing for Language Models](https://arxiv.org/abs/2501.19173) (arXiv) `PO, CI`
- [08/2024] [PrivacyLens: Evaluating Privacy Norm Awareness of Language Models in Action](https://openreview.net/forum?id=CxNXoMnCKc) (NeurIPS '24) `EV, CI`
- [04/2024] [Can LLMs Get Help From Other LLMs Without Revealing Private Information?](https://aclanthology.org/2024.privatenlp-1.12/) (ACL '24 Workshop) `EV`
- [10/2023] [Can LLMs Keep a Secret? Testing Privacy Implications of Language Models via Contextual Integrity Theory](https://openreview.net/forum?id=gmg7t8b4s0) (ICLR '24) `EV, CI`

### General Anonymizers
- [09/2025] [Zero-Shot Privacy-Aware Text Rewriting via Iterative Tree Search](https://arxiv.org/abs/2509.20838) (arXiv) `CO`
- [08/2025] [1-2-3 Check: Enhancing Contextual Privacy in LLM via Multi-Agent Reasoning](https://arxiv.org/pdf/2508.07667) (arXiv) `CO`
- [06/2025] [AgentStealth: Reinforcing Large Language Model for Anonymizing User-generated Text](https://arxiv.org/abs/2506.22508) (arXiv) `CO`
- [06/2025] [Self-Refining Language Model Anonymizers via Adversarial Distillation](https://arxiv.org/abs/2506.01420) (arXiv) `CO`
- [05/2025] [Contextual Integrity in LLMs via Reasoning and Reinforcement Learning](https://arxiv.org/abs/2506.04245) (arXiv) `CO, CI`
- [12/2024] [Truthful Text Sanitization Guided by Inference Attacks](https://arxiv.org/abs/2412.12928) (arXiv) `CO`
- [07/2024] [IncogniText: Privacy-enhancing Conditional Text Anonymization via LLM-based Private Attribute Randomization](https://openreview.net/forum?id=JRifjkHove) (NeurIPS '24 SafeGenAI Workshop) `CO`
- [02/2024] [Language Models are Advanced Anonymizers](https://openreview.net/forum?id=82p8VHRsaK) (ICLR '25) `CO`
- [11/2023] [Reducing Privacy Risks in Online Self-Disclosures with Language Models](https://aclanthology.org/2024.acl-long.741/) (ACL '24) `CO`

### Anonymizers for Chatbot Applications
- [10/2025] [Operationalizing Data Minimization for Privacy-Preserving LLM Prompting](https://www.arxiv.org/abs/2510.03662) (arXiv) `CO`
- [06/2025] [Privacy-Preserving LLM Interaction with Socratic Chain-of-Thought Reasoning and Homomorphically Encrypted Vector Databases](https://arxiv.org/abs/2506.17336) (arXiv) `CO`
- [04/2025] [Preempt: Sanitizing Sensitive Prompts for LLMs](https://arxiv.org/abs/2504.05147) (arXiv) `CO`
- [02/2025] [Protecting Users From Themselves: Safeguarding Contextual Privacy in Interactions with Conversational Agents](https://arxiv.org/abs/2502.18509) (arXiv) `CO`
- [10/2024] [PAPILLON: Privacy Preservation from Internet-based and Local Language Model Ensembles](https://aclanthology.org/2025.naacl-long.173/) (NAACL '25) `CO`
- [10/2024] [Rescriber: Smaller-LLM-Powered User-Led Data Minimization for LLM-Based Chatbots](https://dl.acm.org/doi/10.1145/3706598.3713701) (CHI '25) `CO`
- [08/2024] [Casper: Prompt Sanitization for Protecting User Privacy in Web-Based Large Language Models](https://arxiv.org/abs/2408.07004) (arXiv) `CO`

### Anonymizers for Agents
- [09/2025] [PrivWeb: Unobtrusive and Content-aware Privacy Protection For Web Agents](https://arxiv.org/abs/2509.11939) (arXiv) `CO`
- [09/2025] [The Sum Leaks More Than Its Parts: Compositional Privacy Risks and Mitigations in Multi-agent Collaboration](https://arxiv.org/abs/2509.14284) (arXiv) `CI`
- [09/2025] [Privacy in Action: Towards Realistic Privacy Mitigation and Evaluation for LLM-Powered Agents](https://arxiv.org/abs/2509.17488) (arXiv) `CO, CI`
- [05/2025] [Firewalls to Secure Dynamic LLM Agentic Networks](https://arxiv.org/abs/2502.01822) (arXiv) `CO, CI`
- [09/2024] [CI-Bench: Benchmarking Contextual Integrity of AI Assistants on Synthetic Data](https://arxiv.org/abs/2409.13903) (arXiv) `EV, CI`
- [08/2024] [Privacy Awareness for Information-Sharing Assistants: A Case-study on Form-filling with Contextual Integrity](https://openreview.net/forum?id=l9rATNBB8Y) (TMLR '25) `EV, CI`
- [05/2024] [AirGapAgent: Protecting Privacy-Conscious Conversational Agents](https://dl.acm.org/doi/10.1145/3658644.3690350) (CCS '24) `CO, CI`

### Authorship Obfuscation
- [08/2024] [StyleRemix: Interpretable Authorship Obfuscation via Distillation and Perturbation of Style Elements](https://aclanthology.org/2024.emnlp-main.241/) (EMNLP '24) `CO`
- [05/2024] [Keep it Private: Unsupervised Privatization of Online Text](https://aclanthology.org/2024.naacl-long.480/) (NAACL '24) `CO`
- [02/2024] [JAMDEC: Unsupervised Authorship Obfuscation using Constrained Decoding over Small Language Models](https://aclanthology.org/2024.naacl-long.87) (NAACL '24) `CO`
- [02/2024] [ALISON: Fast and Effective Stylometric Authorship Obfuscation](https://ojs.aaai.org/index.php/AAAI/article/view/29901) (AAAI '24) `CO`

### Special Use Case: Abstractive Summarization
- [06/2025] [URANIA: Differentially Private Insights into AI Use](https://arxiv.org/abs/2506.04681) (arXiv) `CO`
- [12/2024] [Clio: Privacy-Preserving Insights into Real-World AI Use](https://arxiv.org/abs/2412.13678) (arXiv) `CO`
- [12/2024] [How Private are Language Models in Abstractive Summarization?](https://arxiv.org/abs/2412.12040) (arXiv) `EV`

## Miscellaneous
- Zotero group for everything related to Contextual Integrity: https://www.zotero.org/groups/2228317/privaci
- https://github.com/chawins/llm-sp: Another Github repo for more general LLM security and privacy papers
