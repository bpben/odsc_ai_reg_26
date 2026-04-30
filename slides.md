---
theme: default
title: ODSC '26 - How I learned to stop worrying and love AI Regulation
css: style.css
info: |
  ODSC '26 talk deck — outline verbatim from source notes.
---
<div class="absolute inset-0">
  <img src="/images/slides/speaker_slide.png" alt="Speaker slide" class="h-full w-full object-cover" />
</div>

---
layout: default
class: h-full
---

<div class="grid h-full w-full min-h-0 grid-cols-[minmax(0,38%)_minmax(0,62%)] items-center gap-6">

<div class="min-w-0">

# How I learned to stop worrying and love AI Regulation

#### Ben Batorsky, ODSC '26

</div>

<div class="flex h-full min-h-0 min-w-0 items-center justify-center">

<img src="/images/slides/strange.gif" alt="" class="max-h-[85vh] w-full object-contain" />

</div>

</div>

---
layout: two-cols-header
layoutClass: gap-2
class: text-sm leading-tight
---
# About me

::left::
<div class="h-full min-h-0 flex flex-col gap-2">
<img src="/images/slides/me.png" alt="" class="max-h-[24vh] w-auto max-w-full object-contain mx-auto shrink-0" />

<div class="text-[0.9em] leading-tight">

- PhD, Policy Analysis/Economics
- City of Boston Analytics Team
- MIT, Food Supply Chain
- Ciox Health, Clinical NLP
- Northeastern EAI, Data Science strategy + solutions

</div>
</div>

::right::

<div class="h-full min-h-0 flex flex-col gap-2">
<img src="/images/slides/philips-logo.png" alt="" class="max-h-[24vh] w-auto max-w-full object-contain mx-auto shrink-0" />

<div class="text-[0.9em] leading-tight">

- Responsible AI Office - Building tools to support development of AI products
- RAI Lead for the US

</div>
</div>

---
layout: image-right-caption
image: /images/slides/02-intro.png
backgroundSize: contain
---

# No more AI regulation!

- Executive Order (12/2025): "Ensuring a national policy framework for artificial intelligence"
- Pre-empts state regulations
- Creates task force to overturn "onerous" regulations
- Focus is on "innovation"

::caption::

Peter Hoskins & Lily Jamali, [“Trump signs order blocking states from enforcing own AI rules”](https://www.bbc.com/news/articles/crmddnge9yro), *BBC News*, 11 Dec. 2025.

---
layout: image-right-caption
image: /images/slides/iapp-state-ai-legislation-2026.png
backgroundSize: contain
---

# Why this is a silly take
- 6 states have passed AI regulation, 17 have bills pending
  - California’s SB 53 - Sweeping transparency requirements
  - Colorado’s AI Act - "AI Bill of Rights" model
  - Kentucky _unanimously_ passed regulation on AI companions
  - EU AI Act - Massive step in standardizing "responsible" AI 
- Trump Administration framework
	- Privacy protections for children
	- Energy considerations
	- Intellectual Property protections

::caption::

[IAPP — US State AI Governance Legislation Tracker](https://iapp.org/resources/article/us-state-ai-governance-legislation-tracker) (last updated 3 Mar. 2026).

---
layout: image-right-caption
image: /images/slides/science-obermeyer-racial-bias-health-algorithm.png
backgroundSize: contain
---

# "Bad AI" is bad practice
## Biased medical triage
- Automated system for identifying patients for additional care
- Prioritized white patients over sicker black patients
- Based on medical costs, which have historical biases

::caption::
Ziad Obermeyer et al., [“Dissecting racial bias in an algorithm used to manage the health of populations”](https://www.science.org/doi/10.1126/science.aax2342), *Science*, 25 Oct. 2019.

---
layout: image-right-caption
image: /images/slides/air-canada-chatbot-ars.png
backgroundSize: contain
---

# "Bad AI" is bad practice (2)
## Air Canada's AI chatbot

> Air Canada argued that it could not be held responsible for the chatbot’s misleading information...the chatbot...should be considered a separate entity and, thus, absolve[s Air Canada] of any liability for its inaccuracies.

> [McCarthy Tétrault - Moffatt v. Air Canada: Misrepresentation by AI Chatbot](https://www.mccarthy.ca/en/insights/blogs/techlex/moffatt-v-air-canada-misrepresentation-ai-chatbot)



::caption::
Ashley Belanger, [“Air Canada must honor refund policy invented by airline’s chatbot”](https://arstechnica.com/tech-policy/2024/02/air-canada-must-honor-refund-policy-invented-by-airlines-chatbot/), *Ars Technica*, 16 Feb. 2024.


---

# Three "pillars" of regulation

- Governance - Policies for managing development, deployment and monitoring, including roles and remediation pathways
- Assessment of risks and potential impact - Approach to assessment and mitigation strategies
- Transparency - Clear documentation and disclosures to users, deployers and regulators

---
layout: quote-slide
---

# Best Practice or Regulation?

> **Establish governance documentation and processes**. Create comprehensive documentation of your sensitive data handling practices, including classification schemes, protection mechanisms, access control policies, and incident response procedures.

...

> Privacy violations [are] mitigated through design choices that include privacy protections by default, ensuring that...only strictly necessary data for the context is collected

---
layout: quote-slide
---

# Best Practice or Regulation? (2)

> **Establish governance documentation and processes**. Create comprehensive documentation of your sensitive data handling practices, including classification schemes, protection mechanisms, access control policies, and incident response procedures.

> <span style="color: #FF6B35">(AWS Well-Architected Framework - protect sensitive data privacy)</span>

...

> Privacy violations [are] mitigated through design choices that include privacy protections by default, ensuring that...only strictly necessary data for the context is collected

> <span style="color: #FF6B35">(NY State Assembly Bill A3265)</span>

---

# Governance

- Policies for managing development, deployment and monitoring, including roles and remediation pathways
- Covering the "life cycle" of the system
  - What is the use-case?
  - What data are you using?
  - What model are you using?
  - How do you measure performance?
  - How do you monitor post-deployment?
  - What do you do if something goes wrong?
  - What is the plan for "sunsetting"?

---
layout: image-right-caption
image: /images/slides/iso-42001-aims-pentagon.png
backgroundSize: contain
---

# Governance in regulation
- NY State Assembly Bill A3265
  - New York AI Bill of Rights 
  - Governance focused on risks to privacy and discrimination
- ISO42001 - International Standard for Artificial Intelligence Management Systems (AIMS)
  - Organization-wide policies for AI development

::caption::

Poorva Dange, [“What is ISO 42001? A Comprehensive Guide to AI Management Systems”](https://iso-docs.com/blogs/iso-42001-artificial-intelligence-management-system-aims/what-is-iso-42001), *ISO Templates and Documents*, 4 Mar. 2025.

---
layout: two-cols-header
layoutClass: gap-4
---

# Deployer vs Provider

::right::
## Deployer 
- Uses the services of a provider (e.g. OpenAI for chatbot)
- Has their own governance and monitoring processes

::left::
## Provider
- Governance, technical and operational requirements
- Supplies materials so Deployers can meet their responsibilities

::bottom::

<div class="w-full text-center text-sm font-semibold pt-2">

Let's not even get into distributors, importers, etc...

</div>

---
layout: image-right-caption
image: /images/slides/agent-governance-toolkit-policy-yaml.png
backgroundSize: contain
---

# Tools for implementing governance

- Microsoft Agent Governance Framework (security-focused)
- Vendor-provided tools
  - AWS Well-Architected Framework Tool
  - CredoAI
  - IBM watsonx.governance
- Model cards (more later)

::caption::
Microsoft, [“Agent Governance Toolkit”](https://github.com/microsoft/agent-governance-toolkit), *GitHub* (accessed 28 Apr. 2026).

---
layout: quote-slide
---

# Best Practice or Regulation?

> Training, validation and testing data sets [must] be relevant, sufficiently representative, and to the best extent possible, free of errors and complete in view of the intended purpose 

...

> Training datasets are independent of test sets: Training and test datasets are selected and maintained to be appropriately independent of one another. 


---
layout: quote-slide
---

# Best Practice or Regulation? (2)

> Training, validation and testing data sets [must] be relevant, sufficiently representative, and to the best extent possible, free of errors and complete in view of the intended purpose

> <span style="color: #FF6B35">(EU AI Act Article 10)</span>

...

> Training datasets are independent of test sets: Training and test datasets are selected and maintained to be appropriately independent of one another.

> <span style="color: #FF6B35">(IMDRF Good Machine Learning Principles)</span>

---
layout: image-right-caption
image: /images/slides/eu-ai-act-4-risk-levels-vibrancy.png
backgroundSize: contain
---

# Risk assessment

- What can go wrong and how do you track and manage it
- Similar concepts in MLOps
  - Observability - Monitoring and logging
  - Retraining/Rollbacks - Fallback mechanisms
- Mitigation commensurate with the risk
  - EU AI Act - 4 risk levels
    - Controls are tuned to the level of risk

::caption::

Linda Eriksson, [“What Are the 4 Risk Levels of the EU AI Act?”](https://www.vibrancy.ai/post/what-are-the-4-risk-levels-of-the-eu-ai-act), *Vibrancy*, 12 Feb. 2024.

---
layout: image-right-caption
image: /images/slides/medasr-model-card-limitations.png
backgroundSize: contain
---

# Impact assessment

- What harms may come from the system and who will they affect?
- Assess individual/group-level bias
  - Group - Does the model perform better for certain groups vs others?
  - Individual - Are similar individuals treated similarly?

::caption::

Google, [MedASR model card — Limitations](https://developers.google.com/health-ai-developer-foundations/medasr/model-card#limitations), *Health AI Developer Foundations* (page last updated 26 Jan. 2026).

---
layout: image-right-caption
image: /images/slides/plot4ai-card-layout.png
backgroundSize: contain
---

# Resources

- PLOT4AI - Threat inventory and assessment framework for AI systems
- IBM Fairness 360 - https://research.ibm.com/blog/ai-fairness-360
  - Toolkit for applying some standard bias measures
- Google "What if" - https://pair-code.github.io/what-if-tool/
  - Visual exploration of model results with built-in bias metrics
- NIST - Risk Management Framework
  - Seven steps for "completeness"

::caption::

Isabel Barberá, [“How does it work?”](https://plot4.ai/how-does-it-work), *PLOT4AI*, 2025.

---
layout: quote-slide
---

# Best Practice or Regulation?

> "Desired outcome: You can trace a data element back to its source, verify the transformations it underwent, and verify data integrity throughout the ML lifecycle." 

...

> Documentation on data should include, but is not limited to, the following topics:
>  - the provenance of the data;
>  - the date that the data were last updated or modified (e.g. date tag in metadata);
>  - for machine learning, the categories of data (e.g. training, validation, test and production data)

---
layout: quote-slide
---

# Best Practice or Regulation? (2)

> "Desired outcome: You can trace a data element back to its source, verify the transformations it underwent, and verify data integrity throughout the ML lifecycle."

> <span style="color: #FF6B35">(AWS well-Architected Framework - Enforce Data Lineage)</span>

...

> Documentation on data should include, but is not limited to, the following topics:
>  - the provenance of the data;
>  - the date that the data were last updated or modified (e.g. date tag in metadata);
>  - for machine learning, the categories of data (e.g. training, validation, test and production data)

> <span style="color: #FF6B35">(ISO42001 - B.4.3 Data resources)</span>

---

# Transparency

- Traceable, reviewable and visible
  - Traceable - Data resources, training processes, etc should be documented
  - Reviewable - These materials should be available for auditors and (in some cases) the public
  - Visible - Disclosures about the use of AI and its limitations

---
layout: two-cols-header
layoutClass: gap-4
---

# Transparency in regulation
::left::
- ISO42001 Annex A - Outlines the key elements that need documentation
  - Examples: System documentation, data management
- Many variations on the theme of "disclosure"
  - EU AI Act - must notify that a person is interacting with AI
  - China's Cyberspace Administration - Clear labelling requirements for AI content
  - NY State - Notification of use of AI decision-making systems

::right::
<img src="/images/slides/chatgpt-disclaimer-example.png" alt="ChatGPT disclaimer example" class="max-h-[18vh] w-auto max-w-full object-contain mx-auto mb-2" />
<img src="/images/slides/attraction-ai-disclosure-example.png" alt="Attraction AI disclosure example" class="max-h-[18vh] w-auto max-w-full object-contain mx-auto mb-2" />

Brafton, [“AI disclaimer examples”](https://www.brafton.com/blog/ai/ai-disclaimer-example/)

---
layout: image-right-caption
image: /images/slides/c2pa-elements.png
backgroundSize: contain
---

# Tools for implementing transparency
- Data Version Control (DVC) - open-source version control for data
  - Useful tools for documenting transformations, metrics
- C2PA - Coalition for Content Provenance and Authenticity
  - Content credentials
- Explainable AI (e.g. SHAP, LIME)

::caption::
Coalition for Content Provenance and Authenticity (C2PA), [“C2PA Technical Specification v2.4”](https://spec.c2pa.org/specifications/specifications/2.4/specs/C2PA_Specification.html), *C2PA*, n.d.

---

# Key components of regulation

- Governance - Policies for managing development, deployment and monitoring, including roles and remediation pathways
  - ML translation: Documentation, Observability, Retraining/Rollbacks
- Assessment of risks and potential impact - Approach to assessment and mitigation strategies
  - ML translation: EDA, sensitivity analysis, sampling techniques
- Transparency - Clear documentation and disclosures to users, deployers and regulators
  - ML translation: Documentation (again!)

---
layout: image-right-caption
image: /images/slides/gemini-3-1-pro-model-card.png
backgroundSize: contain
---

# One neat trick: Model Cards

- Model Cards for Model Reporting (Mitchell et al. 2019)
- Core elements
  - Model details (e.g. owner, type, version)
  - Intended use (e.g. intended use/users)
  - Factors (i.e. groups, environments, instrumentation)
  - Metrics
  - Data - Evaluation and training
  - Quantitative Analysis
  - Ethical considerations
  - Caveats and Recommendations

::caption::
Google DeepMind, [“Gemini 3.1 Pro”](https://deepmind.google/models/model-cards/gemini-3-1-pro/), *Model card*, Feb. 2026.

---

# Real world: Using model cards for compliance

- Situation: SaaS product, providing AI-powered solution for orgs
- Motivation: Major org required ISO42001 certification for all providers
- (Some) ISO42001 requirements (Annex A):
  - System identity
  - Intended purpose
  - Performance profile
  ...starting to sound familiar?
  
---

# Model cards to the rescue!

- Model cards: Single source of truth for data, metrics, etc
- Became a "one stop shop" for related documentation (Confluence)
- Template for new projects, vastly accelerated development pipeline

---
layout: center
---

# How many people feel the systems they work on could use better documentation?

---
layout: center
---
# Regulation may be the support you need to build the systems you want.

---
layout: two-cols-header
layoutClass: gap-4
---

# Thank you!

::left::

## Other resources
- [IAPP AI Governance groups + resources](https://iapp.org/)
- [Aequitas project - fair AI frameworks and initiatives](https://www.aequitas-project.eu/)
- [Google Rules of ML guide](https://developers.google.com/machine-learning/guides/rules-of-ml/)
- [IMDRF Good Machine Learning Principles](https://www.imdrf.org/sites/default/files/2025-02/IMDRF_AIML%20WG_GMLP_N88%20Final.pdf)

### Model card examples
- [Hugging Face model cards](https://huggingface.co/docs/hub/model-cards)
- [CHAI model cards](https://github.com/coalition-for-health-ai/mc-schema)

::right::

## Get in touch
- Website: [https://benbatorsky.com/](https://benbatorsky.com/)
- GitHub: [bpben](https://github.com/bpben)
- These slides: [https://bpben.github.io/odsc_ai_reg_26](https://bpben.github.io/odsc_ai_reg_26)

---
layout: image-right-caption
image: /images/distaval-ad-1958.png
backgroundSize: contain
---

# The Rise of a "Safe" Sedative (1950s)

Thalidomide (Distaval) was marketed worldwide as a non-toxic wonder drug.

- **Marketed for:** Anxiety, sleep, and morning sickness
- **The claim:** Harmless even for pregnant women

::caption::

[Advertisement for Distaval (thalidomide), 1958](https://www.researchgate.net/figure/Advertisement-for-Distaval-thalidomide-1958_fig4_223985310)

---
layout: image-right-caption
image: /images/frances-kelsey.png
backgroundSize: contain
---

# The FDA's refusal (1960)

- FDA Reviewer Dr. Frances Kelsey refused to approve (1960)
	- Application relied on testimonials, limited clinical data
	- Reports of nerve damage in adults
- Manufacturer aggressively pushed for approval
> "Most of the things they called me, you wouldn’t print,” Dr. Kelsey later told the Washington Post.<sup>1</sup>

::caption::
Isabel Sans, [“Frances Oldham Kelsey: How an FDA Pharmacologist Prevented Thalidomide from Becoming a National Tragedy”](https://boundarystones.weta.org/2026/04/24/frances-oldham-kelsey-how-fda-pharmacologist-prevented-thalidomide-becoming-national#:~:text=Kelsey%20asked%20Merrell%20to%20send,Every%20delay%20was%20profit%20lost.), *Boundary Stones (WETA)*, 24 Apr. 2026. (image)

<sup>1</sup> Seidman, Lisa A., and Noreen Warren. "Frances Kelsey & Thalidomide in the US: A Case Study Relating to Pharmaceutical Regulations." <em>The American Biology Teacher</em> 64, no. 7 (2002): 495-500.

---
layout: center
---

# Regulation makes the difference

| Region | Regulatory context | Impact / outcome |
| :--- | :--- | :--- |
| **Europe & UK** | Approved | >10,000 children born with deformations. |
| **United States** | Blocked by FDA | ~17 cases |

<br>

The 1962 Kefauver-Harris Amendment followed, mandating that drug makers prove a drug is both safe and effective before approval.