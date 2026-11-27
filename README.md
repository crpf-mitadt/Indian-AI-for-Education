# Indian AI for Education 🇮🇳

> A curated map of datasets, models, language technologies, infrastructure, research, standards, and open resources for building AI-powered education systems in India.

[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)
![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)
![India](https://img.shields.io/badge/focus-India-orange.svg)
![Education](https://img.shields.io/badge/domain-Education-blue.svg)

**Indian AI for Education** maps the technology stack needed to build AI-powered education products and public-interest education systems for India — from curriculum and educational datasets to Indic language models, speech recognition, text-to-speech, OCR, machine translation, retrieval, fine-tuning, inference, compute, evaluation, privacy, and deployment.

The focus is deliberately **India-heavy**.

“Indian” does **not** mean that every resource listed here must have been developed in India. Global tools and models are included when they are materially useful for building education systems for Indian learners, teachers, institutions, languages, and deployment environments.

**Last major review:** 24 August 2026

---

## Why this repository exists

Building an AI tutor, teacher copilot, assessment system, multilingual learning application, or education assistant for India requires substantially more than choosing an LLM.

A production system may require:

```text
Curriculum / Learning Outcomes
            ↓
Educational Content
            ↓
Copyright & Licensing
            ↓
OCR / Document Parsing
            ↓
Language Identification
            ↓
Transliteration / Normalization
            ↓
Machine Translation
            ↓
Embeddings / Retrieval / RAG
            ↓
LLM / VLM
            ↓
ASR ← Voice Interface → TTS
            ↓
Evaluation
            ↓
Safety / Privacy / Child Protection
            ↓
LMS / Education Infrastructure
            ↓
Cloud / Edge / Offline Deployment
```

India adds important requirements including:

* 22 scheduled languages
* many writing systems
* Indian English
* code-mixing and code-switching
* Romanized Indic text such as Hinglish
* state-specific curricula
* CBSE, NCERT, NIOS and state boards
* multilingual classrooms
* shared and low-cost devices
* intermittent connectivity
* offline requirements
* child speech
* local accents and dialects
* document-heavy education workflows
* privacy requirements for children and learner data
* differing licenses for government and educational content

This repository tries to map those pieces in one place.

---

## Important: Public does not mean open

A resource appearing on the internet does **not** automatically mean that it can be:

* downloaded
* redistributed
* modified
* translated
* embedded
* placed in a RAG index
* used commercially
* used to train an AI model
* used to create synthetic data

Always check the license and terms of the individual resource.

In particular, educational content such as textbooks may have significantly more restrictive terms than software or government open datasets.

**Inclusion in this repository is not a statement that a resource is legally usable for model training.**

---

## Resource tags

Tags are used where useful.

* `OSS` — Open-source software.
* `Open weights` — Model weights are available; this does not necessarily mean the model is OSI-open-source.
* `Dataset` — Dataset or corpus.
* `Benchmark` — Evaluation dataset or benchmark.
* `API` — Hosted API/service is available.
* `Government` — Government or government-backed resource.
* `Indic-22` — Covers all 22 scheduled Indian languages.
* `Offline` — Particularly useful for offline/local deployment.
* `Edge` — Relevant to constrained-device inference.
* `Gated` — Access requires accepting terms or requesting access.
* `Non-commercial` — Commercial use is restricted.
* `Education` — Specifically designed for education or educational data.
* `Research` — Research project or publication.
* `Check license` — Carefully review the current artifact-specific license before use.

Licenses can change between versions. Always verify the upstream source.

---

# Contents

* [Indian Language Scope](#indian-language-scope)
* [India AI Ecosystem](#india-ai-ecosystem)
* [Foundation Models and Indic LLMs](#foundation-models-and-indic-llms)

  * [Sarvam AI](#sarvam-ai)
  * [BharatGen](#bharatgen)
  * [AI4Bharat](#ai4bharat-language-models)
  * [Community Indic Models](#community-indic-models)
  * [Global Models Worth Evaluating](#global-models-worth-evaluating)
* [Vision and Multimodal Models](#vision-and-multimodal-models)
* [Machine Translation](#machine-translation)
* [Transliteration and Romanized Indic](#transliteration-and-romanized-indic)
* [Code-Mixing and Code-Switching](#code-mixing-and-code-switching)
* [Language Identification](#language-identification)
* [Speech Recognition and ASR](#speech-recognition-and-asr)
* [Text-to-Speech](#text-to-speech)
* [OCR](#ocr)
* [Document Intelligence](#document-intelligence)
* [Indic Text and Language Datasets](#indic-text-and-language-datasets)
* [Speech Datasets](#speech-datasets)
* [Translation Datasets](#translation-datasets)
* [Embeddings and Rerankers](#embeddings-and-rerankers)
* [Retrieval and RAG](#retrieval-and-rag)
* [Vector Databases](#vector-databases)
* [Annotation and Data Curation](#annotation-and-data-curation)
* [Training and Fine-Tuning](#training-and-fine-tuning)
* [Inference and Model Serving](#inference-and-model-serving)
* [Offline and Edge AI](#offline-and-edge-ai)
* [Evaluation and Benchmarks](#evaluation-and-benchmarks)
* [Education-Specific Evaluation](#education-specific-evaluation)
* [Compute in India](#compute-in-india)
* [India Education Digital Infrastructure](#india-education-digital-infrastructure)
* [Curriculum and Educational Content](#curriculum-and-educational-content)
* [Indian Education Data](#indian-education-data)
* [State-Level Education Resources](#state-level-education-resources)
* [Open-Source Learning Platforms](#open-source-learning-platforms)
* [AI Tutors and Teacher Tools](#ai-tutors-and-teacher-tools)
* [Assessment and Question Generation](#assessment-and-question-generation)
* [Education Interoperability Standards](#education-interoperability-standards)
* [Accessibility](#accessibility)
* [Privacy, Safety and Governance](#privacy-safety-and-governance)
* [Copyright and Data Licensing](#copyright-and-data-licensing)
* [Research and Evidence](#research-and-evidence)
* [Organizations](#organizations)
* [Other Useful Catalogs](#other-useful-catalogs)
* [Reference Build Paths](#reference-build-paths)
* [Contributing](#contributing)
* [License](#license)

---

# Indian Language Scope

India's 22 scheduled languages are:

* Assamese
* Bengali
* Bodo
* Dogri
* Gujarati
* Hindi
* Kannada
* Kashmiri
* Konkani
* Maithili
* Malayalam
* Manipuri / Meitei
* Marathi
* Nepali
* Odia
* Punjabi
* Sanskrit
* Santali
* Sindhi
* Tamil
* Telugu
* Urdu

Education systems may additionally need to support:

* Indian English
* Hinglish
* Tanglish
* Manglish and other Romanized Indic writing
* regional dialects
* tribal and low-resource languages
* mixed-language classrooms
* Indian Sign Language

Relevant writing systems include Devanagari, Bengali-Assamese, Gurmukhi, Gujarati, Odia, Tamil, Telugu, Kannada, Malayalam, Meitei Mayek, Ol Chiki, Perso-Arabic and Latin.

Language support should therefore **not** be treated as a simple yes/no field.

---

# India AI Ecosystem

These are some of the most important starting points for Indian language and AI infrastructure.

* [AI4Bharat](https://ai4bharat.iitm.ac.in/) - IIT Madras-based research initiative building open datasets, models and tools for Indian languages. `Research`
* [AI4Bharat GitHub](https://github.com/AI4Bharat) - Source repositories for Indic translation, speech, transliteration, datasets and language models. `OSS`
* [AI4Bharat on Hugging Face](https://huggingface.co/ai4bharat) - AI4Bharat model and dataset releases.
* [AI4Bharat Models](https://huggingface.co/ai4bharat/models) - Browse AI4Bharat model checkpoints.
* [AI4Bharat Datasets](https://huggingface.co/ai4bharat/datasets) - Browse AI4Bharat datasets and benchmarks.
* [BHASHINI](https://bhashini.gov.in/) - Government-backed national language technology platform. `Government`
* [Digital India BHASHINI GitHub](https://github.com/bhashini-dibd) - Open-source repositories from the Digital India BHASHINI Division.
* [ULCA](https://github.com/bhashini-dibd/ulca) - Universal Language Contribution API architecture for datasets, models, benchmarking and language services. `OSS`
* [ULCA Portal](https://bhashini.gov.in/ulca) - BHASHINI's language model and dataset ecosystem.
* [BHASHINI Model Explorer](https://bhashini.gov.in/ulca/model/explore-models) - Explore language models registered through ULCA.
* [BHASHINI API Documentation](https://dibd-bhashini.gitbook.io/bhashini-apis/) - Documentation for BHASHINI language APIs. `API`
* [BharatGen](https://bharatgen.com/) - Indian multilingual and multimodal foundation-model initiative.
* [BharatGen on Hugging Face](https://huggingface.co/bharatgenai) - BharatGen models and datasets.
* [BharatGen Models](https://huggingface.co/bharatgenai/models) - Browse BharatGen model releases.
* [BharatGen Datasets](https://bharatgen.com/datasets/) - Indian-language and domain-specific datasets and benchmarks.
* [Sarvam AI](https://www.sarvam.ai/) - Indian AI company developing foundation, speech and translation models.
* [Sarvam AI on Hugging Face](https://huggingface.co/sarvamai) - Sarvam open-weight and research model releases.
* [Sarvam AI API Documentation](https://docs.sarvam.ai/) - Official documentation for Indian-language speech, text, translation, document and agent APIs. `API`
* [Bodhan.AI](https://bodhan.ai/) - IIT Madras-incubated Centre of Excellence in AI for Education, supported by the Ministry of Education, building the Bharat EduAI Stack for India's public education ecosystem. `Education` `Research`
* [IndiaAI](https://indiaai.gov.in/) - Government of India's national AI ecosystem portal. `Government`
* [AIKosh](https://aikosh.indiaai.gov.in/) - IndiaAI platform for discovering datasets, models and related resources. `Government`
* [IndiaAI Compute](https://compute.indiaai.gov.in/) - National AI compute access infrastructure. `Government`
* [ARTPARK](https://artpark.in/) - AI and robotics innovation ecosystem based at IISc Bengaluru.
* [ARTPARK-IISc on Hugging Face](https://huggingface.co/ARTPARK-IISc) - Speech and language models associated with the Vaani ecosystem.
* [Vaani](https://vaani.iisc.ac.in/) - Large Indian language speech-data initiative involving IISc/ARTPARK.
* [Karya](https://www.karya.in/) - India-focused ethical data company collecting language and speech datasets.
* [Karya Data Catalogue](https://www.karya.in/data-catalogue/) - Catalogue of Indian language speech datasets.
* [EkStep Foundation](https://ekstep.org/) - Nonprofit working on digital public infrastructure for learning.
* [Sunbird](https://www.sunbird.org/) - Open-source digital infrastructure used in large-scale education platforms such as DIKSHA.

---

# Foundation Models and Indic LLMs

## Sarvam AI

* [Sarvam-105B](https://huggingface.co/sarvamai/sarvam-105b) - Large mixture-of-experts model focused on Indian-language performance. `Open weights` `Apache-2.0`
* [Sarvam-30B](https://huggingface.co/sarvamai/sarvam-30b) - Smaller MoE model designed for Indian languages and more practical deployment. `Open weights` `Apache-2.0`
* [Sarvam-M](https://huggingface.co/sarvamai/sarvam-m) - Multilingual 24B-class model built on Mistral Small with Indian-language adaptation. `Open weights`
* [Sarvam-1](https://huggingface.co/sarvamai/sarvam-1) - Compact Indian-language model useful for experimentation with smaller systems. `Open weights` `Non-commercial`
* [OpenHathi-7B-Hi-v0.1-Base](https://huggingface.co/sarvamai/OpenHathi-7B-Hi-v0.1-Base) - Early bilingual Hindi-English/Hinglish Llama-based model from Sarvam. `Open weights` `Check license`
* [Sarvam Translate](https://huggingface.co/sarvamai/sarvam-translate) - Translation model targeting the 22 official Indian languages. `Open weights` `MT`

## BharatGen

* [Param-1](https://huggingface.co/bharatgenai/Param-1) - Hindi-English foundation model from BharatGen.
* [Param-1-2.9B-Instruct](https://huggingface.co/bharatgenai/Param-1-2.9B-Instruct) - Instruction-tuned Param model.
* [Param-1-5B](https://huggingface.co/bharatgenai/Param-1-5B) - Medium-sized Param model.
* [Param-1-7B](https://huggingface.co/bharatgenai/Param-1-7B) - Multilingual Param model supporting Hindi, English and additional Indian languages.
* [Param2-17B-A2.4B-Thinking](https://huggingface.co/bharatgenai/Param2-17B-A2.4B-Thinking) - Mixture-of-experts reasoning model with Indian-language support.
* [AgriParam](https://huggingface.co/bharatgenai/AgriParam) - Domain model for Indian agriculture.
* [FinanceParam](https://huggingface.co/bharatgenai/FinanceParam) - Domain model focused on Indian finance.
* [LegalParam](https://huggingface.co/bharatgenai/LegalParam) - Indian legal-domain model.
* [AyurParam](https://huggingface.co/bharatgenai/AyurParam) - Ayurveda-domain model.

Domain models can be relevant to vocational, professional and higher-education systems, but their individual licenses and evaluation limitations should be reviewed before deployment.

## AI4Bharat Language Models

* [IndicLLMSuite](https://github.com/AI4Bharat/IndicLLMSuite) - Data, pipelines and resources for building language models for Indian languages. `OSS`
* [IndicInstruct](https://github.com/AI4Bharat/IndicInstruct) - Training and evaluation code associated with Airavata and Indic instruction tuning. `OSS`
* [Airavata](https://huggingface.co/ai4bharat/airavata) - Hindi instruction-tuned model derived from OpenHathi. `Open weights` `Check upstream license`
* [IndicBERT-v3-270M](https://huggingface.co/ai4bharat/IndicBERT-v3-270M) - Modern multilingual Indic encoder model.
* [IndicBART](https://huggingface.co/ai4bharat/IndicBART) - Sequence-to-sequence model for Indic NLP tasks.

## Community Indic Models

Community models can be useful for research and language-specific experimentation, but quality, maintenance and licenses vary significantly.

* [Indic-LLM](https://github.com/adithya-s-k/Indic-llm) - Framework and experiments for adapting LLMs to Indian languages including Kannada. `OSS`
* [Indic LLM Resource Catalog](https://github.com/OdiaGenAI/Indic_LLM_Resource_Catalog) - Community catalogue of Indic instruction datasets, models and benchmarks.
* [Indic LLM Leaderboard](https://huggingface.co/spaces/Cognitive-Lab/indic_llm_leaderboard) - Community leaderboard for Indic language models.
* [OdiaGenAI](https://huggingface.co/OdiaGenAI) - Community models and datasets focused particularly on Odia and other Indic languages.
* [Bharat-Tiny-LLM-v2](https://huggingface.co/eulogik/Bharat-Tiny-LLM-v2) - Compact Hindi/Hinglish-focused model with tokenizer optimizations. `Open weights`

## Global Models Worth Evaluating

These are not India-specific, but can be useful baselines or production models. Always benchmark them separately on the exact Indian languages, scripts, grade levels and domains required.

* [Qwen](https://huggingface.co/Qwen) - Open-weight multilingual model family.
* [Gemma](https://huggingface.co/google) - Google's open-weight model family.
* [Mistral](https://huggingface.co/mistralai) - Open-weight model family with efficient deployment options.
* [Llama](https://huggingface.co/meta-llama) - Meta's open-weight Llama model family. `Check license`
* [DeepSeek](https://huggingface.co/deepseek-ai) - Reasoning and general-purpose model family.
* [OLMo](https://huggingface.co/allenai) - Open language-model family from Ai2.
* [Phi](https://huggingface.co/microsoft) - Compact model family from Microsoft.
* [Aya](https://huggingface.co/CohereLabs) - Multilingual models and datasets from Cohere For AI.

---

# Vision and Multimodal Models

Education content contains diagrams, scanned pages, charts, handwriting, equations, maps and photographs. Text-only LLMs are therefore insufficient for many use cases.

## India-focused

* [Patram-7B-Instruct](https://huggingface.co/bharatgenai/patram-7b-instruct) - BharatGen vision-language model focused on document understanding. `Open weights`
* [IndicVisionBench](https://huggingface.co/datasets/krutrim-ai-labs/IndicVisionBench) - Indic/India-oriented VLM evaluation resource. `Benchmark`
* [NCERT Bench Vision Lite](https://huggingface.co/datasets/ai4bharat/ncert-bench-vision-lite) - Multimodal educational benchmark based around NCERT-style content. `Dataset` `Benchmark` `Education`

## General open multimodal ecosystems

* [Qwen-VL Models](https://huggingface.co/Qwen) - Vision-language models useful for document and diagram understanding.
* [Gemma Models](https://huggingface.co/google) - Includes multimodal/open-weight Google model releases.
* [LLaVA](https://github.com/haotian-liu/LLaVA) - Open multimodal research stack.
* [Transformers Multimodal Models](https://huggingface.co/docs/transformers/index) - Hugging Face model ecosystem for vision-language tasks.

---

# Machine Translation

Machine translation is foundational for multilingual education: content localization, teacher tools, cross-lingual retrieval and multilingual tutoring.

## Indic translation models

* [IndicTrans2](https://github.com/AI4Bharat/IndicTrans2) - Machine translation system supporting all 22 scheduled Indian languages. `OSS` `Indic-22`
* [IndicTrans2 English → Indic 1B](https://huggingface.co/ai4bharat/indictrans2-en-indic-1B) - English-to-Indic translation checkpoint.
* [IndicTrans2 Indic → English 1B](https://huggingface.co/ai4bharat/indictrans2-indic-en-1B) - Indic-to-English translation checkpoint.
* [IndicTrans2 Indic → Indic 1B](https://huggingface.co/ai4bharat/indictrans2-indic-indic-1B) - Translation between Indian languages.
* [IndicTrans3 Beta](https://huggingface.co/ai4bharat/IndicTrans3-beta) - Newer LLM-based AI4Bharat translation work including document-oriented translation.
* [Sarvam Translate](https://huggingface.co/sarvamai/sarvam-translate) - Sarvam translation model targeting Indian languages.
* [BHASHINI Model Explorer](https://bhashini.gov.in/ulca/model/explore-models) - Registry of MT and other language models available through the BHASHINI ecosystem. `Government`
* [LekhaAnuvaad](https://github.com/bhashini-dibd/lekhaanuvaad) - Document translation pipeline combining OCR, layout analysis and neural machine translation. `OSS`
* [ULCA](https://github.com/bhashini-dibd/ulca) - Standardized infrastructure for contributing and benchmarking MT datasets and models. `OSS`

## Low-resource and tribal languages

* [Bhili → Marathi Translation](https://huggingface.co/ai4bharat/bhili-translate-bhb-mar) - AI4Bharat translation model for Bhili to Marathi.
* [Marathi → Bhili Translation](https://huggingface.co/ai4bharat/bhili-translate-mar-bhb) - AI4Bharat translation model for Marathi to Bhili.
* [Hindi-Mundari Translation Dataset](https://github.com/karya-inc/dataset-hindi-mundari-translation) - Hindi-to-Mundari parallel corpus created by Karya, Microsoft Research India and IIT Kharagpur. `Dataset` `Non-commercial`

---

# Transliteration and Romanized Indic

A large number of Indian users type languages in Latin script rather than the native script.

Examples:

```text
mera homework samjhao
kal ka chapter explain karo
photosynthesis na enna?
```

Treat transliteration as a first-class product capability.

* [IndicXlit](https://github.com/AI4Bharat/IndicXlit) - Transliteration models and tooling for 21 Indic languages. `OSS`
* [Aksharantar](https://huggingface.co/datasets/ai4bharat/Aksharantar) - Large-scale transliteration corpus containing millions of Indic-script/Roman pairs. `Dataset` `Check license`
* [AI4Bharat Transliteration Python Package](https://pypi.org/project/ai4bharat-transliteration/) - Python package for Indic transliteration.
* [AI4Bharat Indic Transliterate for JavaScript](https://www.npmjs.com/package/@ai4bharat/indic-transliterate) - Browser/JavaScript transliteration tooling.
* [Indic NLP Library](https://github.com/anoopkunchukuttan/indic_nlp_library) - Core utilities for Indic tokenization, normalization and transliteration. `OSS`
* [Indic NLP Resources](https://github.com/anoopkunchukuttan/indic_nlp_resources) - Data resources used by the Indic NLP Library.

---

# Code-Mixing and Code-Switching

Indian conversational systems routinely encounter English mixed with Hindi, Tamil, Telugu, Kannada, Marathi and other languages.

* [IndicCMix](https://huggingface.co/datasets/ai4bharat/IndicCMix) - AI4Bharat code-mixed language resource. `Dataset`
* [OpenHathi](https://huggingface.co/sarvamai/OpenHathi-7B-Hi-v0.1-Base) - Hindi-English/Hinglish-focused model useful as an early code-mixing reference.
* [Aksharantar](https://huggingface.co/datasets/ai4bharat/Aksharantar) - Useful for Romanized Indic normalization and transliteration.
* [IndicXlit](https://github.com/AI4Bharat/IndicXlit) - Transliteration tooling for Roman/native-script conversion.

When evaluating an education assistant, test at least:

```text
native script → native response
Romanized Indic → native response
Romanized Indic → Romanized response
English + Indic code-mixing
cross-script spelling variation
English technical term inside Indic sentence
Indic technical term inside English sentence
```

---

# Language Identification

Language identification should generally happen before or alongside ASR/translation in multilingual voice systems.

* [Vaani-LID v0](https://huggingface.co/ARTPARK-IISc/Vaani-LID_v0) - Language-identification model from the IISc/ARTPARK Vaani ecosystem.
* [ULCA](https://github.com/bhashini-dibd/ulca) - Includes specifications for text language-detection models and related language services.
* [fastText Language Identification](https://fasttext.cc/docs/en/language-identification.html) - Lightweight general-purpose language identification baseline.
* [lingua-py](https://github.com/pemistahl/lingua-py) - Local language-identification library worth testing for text applications.

Language ID should be evaluated on code-mixed inputs rather than only monolingual sentences.

---

# Speech Recognition and ASR

Voice interfaces can be especially important for younger learners, learners with low literacy, accessibility use cases and mobile-first deployments.

## India-specific models and frameworks

* [IndicConformerASR](https://github.com/AI4Bharat/IndicConformerASR) - AI4Bharat ASR framework/models covering all 22 scheduled Indian languages. `OSS` `Indic-22`
* [Indic Conformer 600M Multilingual](https://huggingface.co/ai4bharat/indic-conformer-600m-multilingual) - Multilingual Indic ASR checkpoint.
* [Vistaar](https://github.com/AI4Bharat/vistaar) - Large Indic speech benchmark and training ecosystem spanning numerous datasets and languages. `OSS`
* [IndicSUPERB](https://github.com/AI4Bharat/indicSUPERB) - Benchmark suite for Indian-language speech processing. `Benchmark`
* [SraVaani 1.0](https://huggingface.co/ARTPARK-IISc/SraVaani-1.0) - Multilingual Indic ASR model from IISc/ARTPARK.
* [Shrutam-2](https://huggingface.co/bharatgenai/Shrutam-2) - BharatGen multilingual speech-recognition model.
* [Bhili ASR](https://huggingface.co/ai4bharat/bhili-asr) - AI4Bharat low-resource Bhili ASR model.
* [Bhili ASR Canary 1.2B](https://huggingface.co/ai4bharat/bhili-asr-canary-1.2b) - Newer Bhili ASR experiment based on a larger speech architecture.
* [Sruti](https://github.com/AI4Bharat/Sruti) - AI4Bharat work on inclusive speech recognition with attention to underrepresented speakers. `Research`

## Indian English

* [NPTEL2020 Indian English Speech Dataset](https://github.com/AI4Bharat/NPTEL2020-Indian-English-Speech-Dataset) - Indian English speech drawn from NPTEL educational lectures. `Dataset` `Education`
* [Svarah](https://huggingface.co/datasets/ai4bharat/Svarah) - Indian-accented English speech benchmark/data. `Dataset`
* [Vaani](https://huggingface.co/datasets/ARTPARK-IISc/Vaani) - Includes geographically diverse speech useful for studying Indian speech variation.

## General ASR tools

* [Whisper](https://github.com/openai/whisper) - General multilingual speech-recognition baseline. `OSS`
* [faster-whisper](https://github.com/SYSTRAN/faster-whisper) - Faster Whisper inference using CTranslate2. `OSS`
* [whisper.cpp](https://github.com/ggerganov/whisper.cpp) - Local/edge Whisper inference implementation. `OSS` `Offline`
* [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) - Speech and foundation-model training toolkit.
* [ESPnet](https://github.com/espnet/espnet) - Open speech-processing toolkit.
* [SpeechBrain](https://github.com/speechbrain/speechbrain) - Open-source speech toolkit supporting ASR and related tasks.

For education, evaluate ASR separately on:

* child speech
* classroom noise
* teacher speech
* regional accents
* Indian English
* mixed-language speech
* spontaneous speech
* reading aloud
* mathematical terminology
* scientific terminology
* proper nouns
* short answers

---

# Text-to-Speech

## AI4Bharat

* [IndicF5](https://github.com/AI4Bharat/IndicF5) - High-quality multilingual Indian-language TTS model. `OSS`
* [IndicF5 Model](https://huggingface.co/ai4bharat/IndicF5) - Model weights for IndicF5.
* [Indic Parler-TTS](https://huggingface.co/ai4bharat/indic-parler-tts) - Multilingual expressive TTS covering 20 Indian languages plus English. `Open weights` `Gated`
* [Indic Parler-TTS Pretrained](https://huggingface.co/ai4bharat/indic-parler-tts-pretrained) - Pretrained release for Indic Parler-TTS. `Open weights` `Gated`
* [IndicVoices-R](https://github.com/AI4Bharat/IndicVoices-R) - Large multi-speaker corpus covering 22 Indian languages and designed for TTS research. `Dataset` `Indic-22`
* [Bhili TTS](https://huggingface.co/ai4bharat/bhili-tts) - TTS model for low-resource Bhili.

## BharatGen

* [Sooktam-2](https://huggingface.co/bharatgenai/sooktam2) - BharatGen multilingual Indian TTS model. `Check license`

## IISc / ARTPARK

* [DhVaani 0.5](https://huggingface.co/ARTPARK-IISc/DhVaani-0.5) - Indian-language TTS model from the Vaani ecosystem.
* [SYSPIN TTS Dataset](https://vaani.iisc.ac.in/dataset/syspindataset) - Multi-language Indian TTS dataset. `Dataset`

## Community

* [IndicVoice](https://github.com/Bindkushal/indic-voice) - Compact TTS system with an Indic phonemization frontend. `OSS`
* [Indic G2P](https://github.com/Bindkushal/indic-g2p) - Grapheme-to-phoneme tooling designed for Indic-language speech synthesis.

## General TTS infrastructure

* [Coqui TTS](https://github.com/coqui-ai/TTS) - Open-source deep-learning TTS toolkit.
* [ESPnet](https://github.com/espnet/espnet) - Includes speech-synthesis pipelines.
* [SpeechBrain](https://github.com/speechbrain/speechbrain) - General speech toolkit.
* [eSpeak NG](https://github.com/espeak-ng/espeak-ng) - Lightweight speech synthesizer and phonemizer useful in edge/offline pipelines. `Offline`

For education applications, TTS evaluation should consider:

* pronunciation accuracy
* child comprehensibility
* code-mixed pronunciation
* mathematical notation
* science terminology
* expressive speech
* reading speed
* streaming latency
* speaker consistency
* local deployment
* licensing for generated audio and voice cloning

---

# OCR

OCR is a fundamental education-AI capability because Indian educational material often exists as PDFs, scans, worksheets, question papers and photographed pages.

## India-specific OCR

* [IndicPhotoOCR](https://github.com/Bhashini-IITJ/IndicPhotoOCR) - OCR/scene-text recognition for Indian scripts and languages. `OSS`
* [Bharat Scene Text Dataset](https://github.com/Bhashini-IITJ/BharatSceneTextDataset) - Indian-language scene-text dataset. `Dataset`
* [Indic OCR](https://github.com/indic-ocr) - Community organization maintaining Indic OCR resources.
* [Indic OCR Tessdata](https://github.com/indic-ocr/tessdata) - Tesseract language data aimed at Indian scripts.
* [ULCA](https://github.com/bhashini-dibd/ulca) - Includes OCR model and dataset specifications in the BHASHINI ecosystem.
* [LekhaAnuvaad](https://github.com/bhashini-dibd/lekhaanuvaad) - OCR + layout + translation system for documents. `OSS`

## General OCR

* [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) - Mature open-source OCR engine with many language packs. `OSS` `Offline`
* [Tesseract Traineddata](https://github.com/tesseract-ocr/tessdata) - Official Tesseract language models.
* [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR) - Modern OCR toolkit supporting multilingual and document workflows. `OSS`
* [OCRmyPDF](https://github.com/ocrmypdf/OCRmyPDF) - Adds searchable OCR text layers to PDFs. `OSS`

Important Indian education OCR tests include:

* Devanagari
* Bengali-Assamese
* Gujarati
* Gurmukhi
* Odia
* Tamil
* Telugu
* Kannada
* Malayalam
* Urdu
* Meitei Mayek
* mixed English/Indic pages
* equations
* tables
* diagrams
* page headers/footers
* multiple columns
* photographed textbook pages
* low-quality photocopies

---

# Document Intelligence

OCR only extracts characters. Education systems often need structure: chapters, headings, questions, answers, tables, equations, diagrams and reading order.

* [Docling](https://github.com/docling-project/docling) - Document conversion and structured extraction from PDF and other document formats. `OSS`
* [Marker](https://github.com/datalab-to/marker) - Converts PDFs and documents to structured Markdown. `OSS`
* [Unstructured](https://github.com/Unstructured-IO/unstructured) - Open-source document ingestion and partitioning toolkit.
* [IndicDLP](https://huggingface.co/datasets/ai4bharat/indicdlp) - AI4Bharat Indic document-layout resource. `Dataset`
* [Pralekha](https://huggingface.co/datasets/ai4bharat/Pralekha) - Indic document understanding/alignment dataset. `Dataset`
* [Clean Doc Bench](https://huggingface.co/datasets/ai4bharat/clean-doc-bench) - Document-understanding benchmark from AI4Bharat. `Benchmark`
* [Patram-7B-Instruct](https://huggingface.co/bharatgenai/patram-7b-instruct) - BharatGen document-focused vision-language model.
* [LekhaAnuvaad](https://github.com/bhashini-dibd/lekhaanuvaad) - Indian document translation pipeline integrating layout and OCR.
* [OCRmyPDF](https://github.com/ocrmypdf/OCRmyPDF) - Useful first stage for scanned PDF workflows.

---

# Indic Text and Language Datasets

## Large text corpora

* [Sangraha](https://huggingface.co/datasets/ai4bharat/sangraha) - Large multilingual Indic pretraining corpus from AI4Bharat. `Dataset`
* [IndicCorpV2](https://huggingface.co/datasets/ai4bharat/IndicCorpV2) - Large monolingual corpus covering Indian languages. `Dataset`
* [IndicLLMSuite](https://github.com/AI4Bharat/IndicLLMSuite) - Repository connecting Indic datasets with LLM training pipelines.
* [BPCC](https://huggingface.co/datasets/ai4bharat/BPCC) - Bharat Parallel Corpus Collection for machine translation. `Dataset`
* [IndicCMix](https://huggingface.co/datasets/ai4bharat/IndicCMix) - Code-mixed Indic text resource. `Dataset`
* [Aksharantar](https://huggingface.co/datasets/ai4bharat/Aksharantar) - Romanized/native-script transliteration corpus. `Dataset`
* [IndicQA](https://huggingface.co/datasets/ai4bharat/IndicQA) - Indic-language question-answering resource. `Dataset`

## Instruction and model-alignment resources

* [IndicInstruct](https://github.com/AI4Bharat/IndicInstruct) - Indic instruction-tuning datasets and training/evaluation tooling.
* [IndicLLMSuite](https://github.com/AI4Bharat/IndicLLMSuite) - Includes data and recipes related to Indic LLM pretraining and alignment.
* [OdiaGenAI Indic LLM Resource Catalog](https://github.com/OdiaGenAI/Indic_LLM_Resource_Catalog) - Index of language-specific Indic instruction datasets and models.

---

# Speech Datasets

* [IndicVoices](https://github.com/AI4Bharat/IndicVoices) - Large natural and spontaneous speech corpus across all 22 scheduled Indian languages. `Dataset` `Indic-22`
* [IndicVoices on Hugging Face](https://huggingface.co/datasets/ai4bharat/IndicVoices) - Dataset access page.
* [IndicVoices-R](https://github.com/AI4Bharat/IndicVoices-R) - Multi-speaker TTS-focused dataset across 22 Indian languages. `Dataset` `Indic-22`
* [Vaani](https://vaani.iisc.ac.in/) - Large geographically diverse Indian speech-data project.
* [Vaani Dataset](https://huggingface.co/datasets/ARTPARK-IISc/Vaani) - Hugging Face distribution for Vaani speech data. `Dataset`
* [Kathbath](https://huggingface.co/datasets/ai4bharat/Kathbath) - Indic speech dataset. `Dataset`
* [Shrutilipi](https://huggingface.co/datasets/ai4bharat/Shrutilipi) - Large speech/text alignment corpus for Indian languages. `Dataset`
* [Svarah](https://huggingface.co/datasets/ai4bharat/Svarah) - Indian-accented English speech dataset. `Dataset`
* [Lahaja](https://huggingface.co/datasets/ai4bharat/Lahaja) - Speech resource oriented toward accent/dialect variation. `Dataset`
* [Rural Women Bhojpuri](https://huggingface.co/datasets/ai4bharat/Rural_Women_Bhojpuri) - Speech resource focused on underrepresented rural women Bhojpuri speakers. `Dataset`
* [Rural Women ASR v2](https://huggingface.co/datasets/ai4bharat/Rural_Women_ASR_v2) - Inclusive speech-recognition dataset. `Dataset`
* [NPTEL2020 Indian English Speech Dataset](https://github.com/AI4Bharat/NPTEL2020-Indian-English-Speech-Dataset) - Indian English educational lecture speech. `Dataset`
* [Karya Indic Speech Dataset 2022](https://github.com/karya-inc/dataset-indicspeech-2022) - Sample speech data for 11 Indic languages; full corpus access separately available. `Dataset` `Non-commercial`
* [Karya Data Catalogue](https://www.karya.in/data-catalogue/) - Commercial/research catalogue with conversational and read speech across Indian languages.
* [Mundari TTS Dataset](https://github.com/karya-inc/dataset-mundari-tts) - Mundari TTS corpus. `Dataset` `Non-commercial`
* [SYSPIN TTS Dataset](https://vaani.iisc.ac.in/dataset/syspindataset) - Indian multilingual TTS resource. `Dataset`

---

# Translation Datasets

* [BPCC](https://huggingface.co/datasets/ai4bharat/BPCC) - Large parallel-corpus collection used with IndicTrans2. `Dataset`
* [IN22-Gen](https://huggingface.co/datasets/ai4bharat/IN22-Gen) - General-purpose evaluation set for translation across Indian languages. `Dataset` `Benchmark`
* [IN22-Conv](https://huggingface.co/datasets/ai4bharat/IN22-Conv) - Conversational translation evaluation data. `Dataset` `Benchmark`
* [Aksharantar](https://huggingface.co/datasets/ai4bharat/Aksharantar) - Transliteration rather than semantic translation, but important for multilingual pipelines.
* [Hindi-Mundari Translation Dataset](https://github.com/karya-inc/dataset-hindi-mundari-translation) - Hindi/Mundari parallel text. `Dataset` `Non-commercial`
* [IndicTrans2](https://github.com/AI4Bharat/IndicTrans2) - Repository links the models, corpora and evaluation resources used in the project.

---

# Embeddings and Rerankers

Retrieval models should be evaluated on Indian-language queries independently from the generation model.

## Indic retrieval resources

* [Indic-RAG-Suite](https://huggingface.co/datasets/ai4bharat/Indic-Rag-Suite) - Large retrieval/RAG evaluation suite spanning numerous Indian languages. `Dataset` `Benchmark`
* [MSMARCO-XI](https://huggingface.co/datasets/ai4bharat/MSMARCO-XI) - Multilingual retrieval dataset extending MS MARCO into 14 Indian languages. `Dataset`
* [IndicMSMARCO](https://huggingface.co/datasets/ai4bharat/IndicMSMARCO) - Indic-language retrieval benchmark. `Dataset`

## Multilingual embedding models

* [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large) - Strong multilingual embedding baseline.
* [BGE-M3](https://huggingface.co/BAAI/bge-m3) - Multilingual dense/sparse/multi-vector embedding model.
* [Jina Embeddings v3](https://huggingface.co/jinaai/jina-embeddings-v3) - Multilingual embedding model with long-context support.
* [Sentence Transformers](https://github.com/UKPLab/sentence-transformers) - Widely used embedding and sentence-similarity framework. `OSS`

## Rerankers

* [BGE Reranker v2 M3](https://huggingface.co/BAAI/bge-reranker-v2-m3) - Multilingual cross-encoder reranker.
* [Jina Reranker v2 Base Multilingual](https://huggingface.co/jinaai/jina-reranker-v2-base-multilingual) - Multilingual reranking model.

For textbook RAG, test retrieval by:

```text
board
grade
subject
chapter
learning outcome
language
medium of instruction
question type
native vs Romanized query
cross-language query
```

---

# Retrieval and RAG

## Frameworks

* [LlamaIndex](https://github.com/run-llama/llama_index) - Data/RAG framework for LLM applications. `OSS`
* [Haystack](https://github.com/deepset-ai/haystack) - Open-source retrieval and LLM application framework. `OSS`
* [LangChain](https://github.com/langchain-ai/langchain) - General LLM application/orchestration framework. `OSS`
* [DSPy](https://github.com/stanfordnlp/dspy) - Framework for programming and optimizing language-model pipelines.
* [LiteLLM](https://github.com/BerriAI/litellm) - Unified interface/proxy for many model APIs and self-hosted providers.
* [Instructor](https://github.com/567-labs/instructor) - Structured outputs from language models.
* [Outlines](https://github.com/dottxt-ai/outlines) - Structured/constrained generation tools.

## India-specific retrieval data

* [Indic-RAG-Suite](https://huggingface.co/datasets/ai4bharat/Indic-Rag-Suite)
* [MSMARCO-XI](https://huggingface.co/datasets/ai4bharat/MSMARCO-XI)
* [IndicMSMARCO](https://huggingface.co/datasets/ai4bharat/IndicMSMARCO)

---

# Vector Databases

* [pgvector](https://github.com/pgvector/pgvector) - Vector similarity search inside PostgreSQL. `OSS`
* [Qdrant](https://github.com/qdrant/qdrant) - Dedicated open-source vector database supporting dense and sparse retrieval. `OSS`
* [Milvus](https://github.com/milvus-io/milvus) - Distributed vector database. `OSS`
* [Weaviate](https://github.com/weaviate/weaviate) - Open-source vector database and retrieval engine. `OSS`
* [Chroma](https://github.com/chroma-core/chroma) - Embedding/vector store aimed at AI applications. `OSS`
* [FAISS](https://github.com/facebookresearch/faiss) - High-performance local vector similarity-search library. `OSS` `Offline`

For simple education systems, **PostgreSQL + pgvector** is often enough. A dedicated vector database is not automatically required.

---

# Annotation and Data Curation

## India-specific

* [Shoonya](https://github.com/AI4Bharat/Shoonya) - AI4Bharat annotation platform designed for language-data collection and annotation. `OSS`
* [ULCA](https://github.com/bhashini-dibd/ulca) - Contribution schemas, dataset repositories and benchmarking infrastructure for Indian language technologies.
* [Karya](https://www.karya.in/) - Human data collection platform with an India-focused worker ecosystem.
* [Karya Data Catalogue](https://www.karya.in/data-catalogue/) - Existing Indian speech datasets.

## General tools

* [Label Studio](https://github.com/HumanSignal/label-studio) - General-purpose open-source annotation platform.
* [Argilla](https://github.com/argilla-io/argilla) - Human/AI feedback, dataset curation and annotation platform.
* [Doccano](https://github.com/doccano/doccano) - Text annotation platform for NLP.
* [CVAT](https://github.com/cvat-ai/cvat) - Image/video annotation platform.
* [Cleanlab](https://github.com/cleanlab/cleanlab) - Detects potential label and data-quality problems.
* [DataTrove](https://github.com/huggingface/datatrove) - Large-scale text-data processing pipeline.
* [NeMo Curator](https://github.com/NVIDIA/NeMo-Curator) - Dataset curation and filtering toolkit for foundation models.
* [text-dedup](https://github.com/ChenghaoMou/text-dedup) - Text deduplication toolkit.
* [Dolma](https://github.com/allenai/dolma) - Data-processing toolkit used for large language-model corpora.

---

# Training and Fine-Tuning

## Core frameworks

* [Transformers](https://github.com/huggingface/transformers) - Widely used library for language, vision and multimodal foundation models.
* [Hugging Face Datasets](https://github.com/huggingface/datasets) - Dataset loading and processing library.
* [PEFT](https://github.com/huggingface/peft) - Parameter-efficient fine-tuning including LoRA.
* [TRL](https://github.com/huggingface/trl) - Post-training, preference optimization and reinforcement-learning tooling.
* [Accelerate](https://github.com/huggingface/accelerate) - Distributed/multi-device training utility.
* [Tokenizers](https://github.com/huggingface/tokenizers) - Fast tokenizer library.
* [Axolotl](https://github.com/axolotl-ai-cloud/axolotl) - Configuration-driven fine-tuning framework.
* [Unsloth](https://github.com/unslothai/unsloth) - Memory-efficient fine-tuning workflows.
* [LLaMA-Factory](https://github.com/hiyouga/LLaMA-Factory) - Training and fine-tuning interface for many model families.
* [torchtune](https://github.com/pytorch/torchtune) - PyTorch-native LLM fine-tuning toolkit.
* [DeepSpeed](https://github.com/deepspeedai/DeepSpeed) - Distributed training and optimization.
* [NVIDIA NeMo](https://github.com/NVIDIA/NeMo) - Large-scale training framework for language and speech models.
* [LitGPT](https://github.com/Lightning-AI/litgpt) - Lightweight LLM training/fine-tuning framework.

## Indic-specific training references

* [IndicLLMSuite](https://github.com/AI4Bharat/IndicLLMSuite) - Indic pretraining and alignment resources.
* [IndicInstruct](https://github.com/AI4Bharat/IndicInstruct) - Instruction tuning and Indic evaluation.
* [IndicTrans2](https://github.com/AI4Bharat/IndicTrans2) - Training and inference resources for multilingual Indic translation.
* [IndicConformerASR](https://github.com/AI4Bharat/IndicConformerASR) - Indian-language ASR models and resources.
* [IndicF5](https://github.com/AI4Bharat/IndicF5) - Indic TTS training/inference code.

---

# Inference and Model Serving

## GPU serving

* [vLLM](https://github.com/vllm-project/vllm) - High-throughput LLM inference and OpenAI-compatible serving. `OSS`
* [SGLang](https://github.com/sgl-project/sglang) - High-performance runtime for LLM and multimodal applications. `OSS`
* [TensorRT-LLM](https://github.com/NVIDIA/TensorRT-LLM) - NVIDIA-optimized LLM inference.
* [Text Generation Inference](https://github.com/huggingface/text-generation-inference) - Hugging Face inference server.

## Local inference

* [llama.cpp](https://github.com/ggml-org/llama.cpp) - Efficient local inference across CPUs, GPUs and many device types. `OSS` `Offline` `Edge`
* [Ollama](https://github.com/ollama/ollama) - Simple local model runtime. `Offline`
* [LocalAI](https://github.com/mudler/LocalAI) - Local OpenAI-compatible inference stack.
* [MLX](https://github.com/ml-explore/mlx) - Machine-learning framework optimized for Apple Silicon.
* [MLX LM](https://github.com/ml-explore/mlx-lm) - LLM inference and fine-tuning on Apple Silicon.
* [MLC LLM](https://github.com/mlc-ai/mlc-llm) - Compilation/deployment stack for running LLMs on many devices.
* [ONNX Runtime](https://github.com/microsoft/onnxruntime) - Cross-platform inference runtime.
* [ExecuTorch](https://github.com/pytorch/executorch) - PyTorch inference for mobile and edge devices.

---

# Offline and Edge AI

Offline support should be a **first-class requirement** for Indian education systems rather than an afterthought.

Useful building blocks include:

* [llama.cpp](https://github.com/ggml-org/llama.cpp) - Quantized local LLM inference.
* [whisper.cpp](https://github.com/ggerganov/whisper.cpp) - Offline/local speech recognition.
* [ONNX Runtime](https://github.com/microsoft/onnxruntime) - Device and edge inference.
* [ExecuTorch](https://github.com/pytorch/executorch) - Mobile/embedded model execution.
* [MLC LLM](https://github.com/mlc-ai/mlc-llm) - Deployment across mobile and other hardware.
* [FAISS](https://github.com/facebookresearch/faiss) - Local vector retrieval.
* [SQLite](https://www.sqlite.org/) - Lightweight local structured storage.
* [Kolibri](https://github.com/learningequality/kolibri) - Offline-first educational content platform.
* [Sunbird ED](https://github.com/Sunbird-Ed) - Open education infrastructure relevant to Indian public systems.

Useful deployment patterns:

```text
Internet
   ↓ periodic synchronization
School server / teacher laptop
   ├── local educational content
   ├── OCR/indexed curriculum
   ├── local embeddings
   ├── vector index
   ├── quantized language model
   ├── ASR
   ├── TTS
   └── queued analytics
           ↓
      Local Wi-Fi / LAN
           ↓
     Student devices
```

---

# Evaluation and Benchmarks

General-purpose model benchmarks are insufficient for Indian education systems.

Evaluation should cover:

```text
model capability
+ Indian language capability
+ education quality
+ curriculum alignment
+ safety
+ learning impact
```

## Indic language benchmarks

* [MILU](https://huggingface.co/datasets/ai4bharat/MILU) - Multilingual Indic language-understanding benchmark. `Benchmark`
* [IndicIFEval](https://huggingface.co/datasets/ai4bharat/IndicIFEval) - Verifiable instruction-following benchmark for Indic languages. `Benchmark`
* [IndicIFEval GitHub](https://github.com/AI4Bharat/IndicIFEval) - Evaluation tooling and benchmark repository.
* [Hindi probability minimal pairs](https://huggingface.co/datasets/lmo0317/hindi-probability-minimal-pairs) - Classroom diagnostic with 32 Hindi–English questions distinguishing conditional from joint probability, checked against enumerated outcomes. `Dataset` `Public access` `Check license`
* [IndicContextEval](https://huggingface.co/datasets/ai4bharat/IndicContextEval) - Context/long-context evaluation for Indian languages. `Benchmark`
* [IN22-Gen](https://huggingface.co/datasets/ai4bharat/IN22-Gen) - Indic MT benchmark.
* [IN22-Conv](https://huggingface.co/datasets/ai4bharat/IN22-Conv) - Conversational Indic MT benchmark.
* [IndicSUPERB](https://github.com/AI4Bharat/indicSUPERB) - Indian-language speech evaluation suite.
* [SpeechArenaBench](https://huggingface.co/datasets/ai4bharat/SpeechArenaBench) - Speech-model evaluation data.
* [Indic-RAG-Suite](https://huggingface.co/datasets/ai4bharat/Indic-Rag-Suite) - Retrieval/RAG benchmark for Indian languages.
* [MSMARCO-XI](https://huggingface.co/datasets/ai4bharat/MSMARCO-XI) - Multilingual retrieval evaluation.
* [IndicMSMARCO](https://huggingface.co/datasets/ai4bharat/IndicMSMARCO) - Indic retrieval evaluation.
* [Indic-Bias](https://huggingface.co/datasets/ai4bharat/Indic-Bias) - Dataset for studying bias in Indian-language AI systems.
* [MANGO](https://huggingface.co/datasets/ai4bharat/MANGO) - AI4Bharat evaluation/data resource.
* [FERMAT](https://huggingface.co/datasets/ai4bharat/FERMAT) - AI4Bharat reasoning/evaluation resource.
* [RiddleBench](https://huggingface.co/datasets/ai4bharat/RiddleBench) - Reasoning benchmark.
* [Focus](https://huggingface.co/datasets/ai4bharat/Focus) - AI4Bharat evaluation dataset.
* [Rasa](https://huggingface.co/datasets/ai4bharat/Rasa) - AI4Bharat language dataset/evaluation resource.
* [BhashaBench-Multi](https://huggingface.co/datasets/bharatgenai/BhashaBench-Multi) - BharatGen benchmark covering Indian languages and knowledge domains.
* [BhashaBench-Legal](https://huggingface.co/datasets/bharatgenai/BhashaBench-Legal) - Indian legal-domain benchmark.
* [BhashaBench-Finance](https://huggingface.co/datasets/bharatgenai/BhashaBench-Finance) - Indian finance benchmark.
* [BhashaBench-Krishi](https://huggingface.co/datasets/bharatgenai/BhashaBench-Krishi) - Indian agriculture benchmark.
* [BhashaBench-Ayur](https://huggingface.co/datasets/bharatgenai/BhashaBench-Ayur) - Ayurveda-domain benchmark.
* [IndicParam](https://huggingface.co/datasets/bharatgenai/IndicParam) - Benchmark for low and extremely low-resource Indic languages.
* [ParamBench](https://huggingface.co/datasets/bharatgenai/ParamBench) - Hindi benchmark based on Indian competitive/academic domains.
* [TORQUE](https://huggingface.co/datasets/bharatgenai/TORQUE) - BharatGen evaluation resource.
* [IndicVisionBench](https://huggingface.co/datasets/krutrim-ai-labs/IndicVisionBench) - India-oriented multimodal evaluation.

## General evaluation tooling

* [lm-evaluation-harness](https://github.com/EleutherAI/lm-evaluation-harness) - Widely used LLM evaluation framework.
* [LightEval](https://github.com/huggingface/lighteval) - Hugging Face evaluation toolkit.
* [HELM](https://github.com/stanford-crfm/helm) - Holistic language-model evaluation framework.
* [Ragas](https://github.com/explodinggradients/ragas) - RAG evaluation framework.
* [DeepEval](https://github.com/confident-ai/deepeval) - LLM evaluation framework.
* [promptfoo](https://github.com/promptfoo/promptfoo) - Prompt/model evaluation and red-team tooling.
* [Langfuse](https://github.com/langfuse/langfuse) - LLM tracing, prompt management, datasets and evaluation.
* [Arize Phoenix](https://github.com/Arize-ai/phoenix) - Open-source AI observability and evaluation.
* [MLflow](https://github.com/mlflow/mlflow) - Experiment tracking and model/application evaluation platform.

---

# Education-Specific Evaluation

## India-specific resources

* [NCERT Bench Lite](https://huggingface.co/datasets/ai4bharat/ncert-bench-lite) - AI4Bharat education-oriented benchmark based around NCERT-style material. `Benchmark` `Education`
* [NCERT Bench Vision Lite](https://huggingface.co/datasets/ai4bharat/ncert-bench-vision-lite) - Multimodal educational benchmark. `Benchmark` `Education`
* [PARAKH](https://parakh.ncert.gov.in/) - NCERT's national assessment body and competency-based assessment ecosystem. `Government` `Education`
* [PARAKH Learning Assessment](https://parakh.ncert.gov.in/learning-assessment) - Assessment frameworks and resources.
* [PARAKH Rashtriya Sarvekshan 2024](https://parakh.ncert.gov.in/prs-reports-2024) - National competency-assessment reports and evidence.
* [ASER Centre](https://asercentre.org/) - Large-scale foundational learning assessment work in India.
* [ASER 2024](https://asercentre.org/aser-2024/) - Latest major ASER cycle and associated learning data.

## What education evaluation should measure

### Correctness

* factual accuracy
* mathematical correctness
* scientific correctness
* citation correctness
* hallucination rate

### Curriculum

* board alignment
* grade alignment
* chapter alignment
* competency alignment
* terminology alignment

### Pedagogy

* age appropriateness
* explanation quality
* quality of hints
* misconception diagnosis
* scaffolding
* Socratic behavior
* cognitive load
* quality of examples
* refusal to simply give answers when learning requires reasoning

### Language

* native-script accuracy
* Romanized input
* code-mixed input
* dialect robustness
* terminology preservation
* Indian English
* translation quality

### Safety

* harmful content
* stereotypes
* caste/religion/gender bias
* age-inappropriate material
* privacy leakage
* jailbreak resistance
* academic-integrity risks

### Actual learning impact

The highest-level question is not:

> Did the model answer correctly?

It is:

> Did the learner understand more after interacting with the system?

---

# Compute in India

## IndiaAI Compute

* [IndiaAI Compute Portal](https://compute.indiaai.gov.in/) - Government-backed AI compute marketplace/infrastructure. `Government`
* [IndiaAI Compute Login](https://compute.indiaai.gov.in/login) - Access portal.
* [IndiaAI Compute Pricing](https://compute.indiaai.gov.in/pricelist) - Current GPU/provider price list.
* [IndiaAI Price Calculator](https://compute.indiaai.gov.in/indiaaipricecalculator) - Compute-cost calculator.
* [IndiaAI Compute Ready Reckoner](https://compute.indiaai.gov.in/files/Ready-Reckoner.pdf) - Guidance for using the platform.
* [IndiaAI Compute End User Policy](https://compute.indiaai.gov.in/files/end-user-policy.pdf) - Eligibility and usage policy.

Prices and available accelerators change. Link to the live price list rather than hardcoding prices in downstream projects.

## National research compute

* [PARAM Siddhi-AI](https://www.cdac.gov.in/index.aspx?id=hpc_nsf_siddhi-AI) - C-DAC AI supercomputing infrastructure.
* [AIRAWAT / National AI Research Analytics and Knowledge Dissemination Platform](https://www.cdac.gov.in/index.aspx?id=hpc_nsf_npsfidx) - National AI compute/research infrastructure.
* [C-DAC AIRAWAT Service](https://cdac.gov.in/index.aspx?id=service_details&serviceId=AIResearchAnalyticsandKnowledgeDisseminationPlatform%28AIRAWAT%29) - AIRAWAT service details.

## Indian cloud providers

* [Yotta Shakti Cloud](https://yotta.com/shakticloud/) - Indian AI cloud/GPU infrastructure.
* [E2E Networks](https://www.e2enetworks.com/) - India-based cloud provider offering GPU infrastructure.

Also evaluate global clouds with Indian regions when data residency, latency or institutional procurement require them.

---

# India Education Digital Infrastructure

## NDEAR

* [NDEAR](https://www.ndear.gov.in/) - National Digital Education Architecture. `Government` `Education`
* [NDEAR Policies and Standards](https://www.ndear.gov.in/policies-and-standards.html) - Policies and interoperability standards.
* [NDEAR Standards](https://standards.ndear.gov.in/) - Standards directory associated with the architecture.

NDEAR is particularly relevant because it treats education infrastructure as interoperable building blocks rather than one giant application.

## DIKSHA and Sunbird

* [DIKSHA](https://diksha.gov.in/) - India's national digital infrastructure/platform for school education. `Government` `Education`
* [About DIKSHA](https://diksha.gov.in/about-us/) - Overview, supported languages and licensing information.
* [DIKSHA Open Source](https://diksha.gov.in/help/diksha-oss/index.html) - DIKSHA open-source documentation.
* [Sunbird](https://www.sunbird.org/) - Open-source digital public infrastructure ecosystem underlying DIKSHA.
* [Sunbird ED GitHub](https://github.com/Sunbird-Ed) - Main education repositories.
* [Sunbird ED Community](https://github.com/Sunbird-Ed/Community) - Documentation and community resources.
* [Sunbird ED Portal](https://github.com/Sunbird-Ed/SunbirdEd-portal) - Web portal code.
* [Sunbird ED Mobile App](https://github.com/Sunbird-Ed/SunbirdEd-mobile-app) - Mobile learning application.
* [Sunbird Client Services](https://github.com/Sunbird-Ed/sunbird-client-services) - Client-side services.
* [Sunbird MCP](https://github.com/Sunbird-Ed/Sunbird-MCP) - MCP server for searching and retrieving Sunbird educational content. `OSS`

---

# Curriculum and Educational Content

## National curriculum and policy

* [National Education Policy 2020](https://www.education.gov.in/nep-2020) - National education policy. `Government`
* [Ministry of Education NEP Initiatives](https://www.education.gov.in/nep-initiatives) - Implementation initiatives.
* [National Curriculum Framework for School Education 2023](https://www.education.gov.in/national-curriculum-framework-school-education-2023) - Current national school curriculum framework. `Government`
* [NCF 2023 PDF](https://www.education.gov.in/sites/upload_files/mhrd/files/ncf_2023.pdf) - Full framework document.

## NCERT

* [NCERT](https://ncert.nic.in/) - National Council of Educational Research and Training.
* [NCERT Textbooks](https://ncert.nic.in/textbook.php) - Official textbook access.
* [NCERT Books Portal](https://ncertbooks.ncert.gov.in/) - Official NCERT textbook portal.
* [CIET](https://ciet.ncert.gov.in/) - Central Institute of Educational Technology.
* [ePathshala](https://ciet.ncert.gov.in/initiative/epathshala) - Digital NCERT textbooks and educational resources.
* [ePathshala License](https://epathshala.nic.in/pages.php?id=license) - Important usage and copyright conditions for NCERT e-content.
* [NROER](https://nroer.gov.in/) - National Repository of Open Educational Resources.

**Important:** NCERT/ePathshala resources should not be assumed to be freely trainable just because they are downloadable. Review the current license and obtain permission where required.

## National course platforms

* [SWAYAM](https://swayam.gov.in/) - Government-supported online course platform spanning school to postgraduate education.
* [About SWAYAM](https://swayam.gov.in/about) - Platform scope and coordinating institutions.
* [NPTEL](https://nptel.ac.in/) - IIT/IISc-led higher-education course platform.
* [National Digital Library of India](https://ndl.iitkgp.ac.in/) - Large digital discovery platform for educational resources.
* [PM eVIDYA](https://pmevidya.education.gov.in/) - Multimodal education initiative involving digital, television and other channels.
* [NIOS](https://nios.ac.in/) - National Institute of Open Schooling.
* [CBSE Academic](https://cbseacademic.nic.in/) - CBSE curricula, sample papers, academic circulars and resources.

---

# Indian Education Data

## School education

* [UDISE+](https://udiseplus.gov.in/) - Unified District Information System for Education Plus. `Government`
* [UDISE+ on Open Government Data](https://www.data.gov.in/catalog/unified-district-information-system-education-plus-udise-plus) - Downloadable/API-accessible school-system datasets. `Dataset` `Government`
* [Open Government Data Platform India](https://data.gov.in/) - Searchable government open-data portal.
* [Government Open Data License - India](https://www.data.gov.in/policies) - Licensing framework for data.gov.in resources.

UDISE+ can be useful for understanding:

* school infrastructure
* enrollment
* teachers
* management type
* geography
* electricity
* computers
* internet availability
* toilets and water
* school categories

It is primarily **system/infrastructure data**, not a direct measure of individual student learning.

## Higher education

* [AISHE](https://aishe.gov.in/) - All India Survey on Higher Education. `Government`
* [AISHE Final Reports and Data](https://aishe.gov.in/aishe-final-report/) - National higher-education reports and downloadable data.

AISHE includes information on:

* universities
* colleges
* enrollment
* gender
* teachers
* programmes
* disciplines
* institutional categories

## Learning outcomes

* [ASER Centre](https://asercentre.org/) - Independent learning assessment and education research organization.
* [ASER 2024](https://asercentre.org/aser-2024/) - Rural household-based foundational learning survey.
* [About ASER 2024](https://asercentre.org/about-aser-2024/) - Methodology and scope.
* [PARAKH](https://parakh.ncert.gov.in/) - National Assessment Centre under NCERT.
* [PARAKH Learning Assessment](https://parakh.ncert.gov.in/learning-assessment) - Competency-based assessment resources.
* [PARAKH Rashtriya Sarvekshan 2024 Reports](https://parakh.ncert.gov.in/prs-reports-2024) - State/national assessment results.

---

# State-Level Education Resources

India's curriculum ecosystem is state-specific. AI systems intended for schools should map content by:

```text
state
→ board
→ medium
→ grade
→ subject
→ textbook
→ chapter
→ competency / learning outcome
```

Useful starting points:

* [Maharashtra Balbharati](https://ebalbharati.in/) - Maharashtra State Bureau of Textbook Production and Curriculum Research.
* [Kerala SCERT](https://scert.kerala.gov.in/) - Kerala State Council of Educational Research and Training.
* [Kerala Revised Curriculum/Textbooks](https://scert.kerala.gov.in/curriculum-2024/) - Current revised textbook resources.
* [Telangana SCERT](https://www.scert.telangana.gov.in/) - Telangana curriculum, textbooks and academic resources.
* [Karnataka DSERT](https://dsert.karnataka.gov.in/) - Department of State Educational Research and Training, Karnataka.
* [Tamil Nadu SCERT](https://scert.tnschools.gov.in/) - Tamil Nadu State Council of Educational Research and Training.
* [Andhra Pradesh SCERT](https://scert.ap.gov.in/) - Andhra Pradesh curriculum and academic resources.
* [Gujarat GCERT](https://gcert.gujarat.gov.in/) - Gujarat Council of Educational Research and Training.
* [Bihar SCERT](https://scert.bihar.gov.in/) - Bihar State Council of Educational Research and Training.
* [Uttar Pradesh SCERT](https://scert-up.in/) - Uttar Pradesh State Council of Educational Research and Training.
* [Haryana SCERT](https://scertharyana.gov.in/) - Haryana State Council of Educational Research and Training.
* [Assam SCERT](https://scert.assam.gov.in/) - Assam State Council of Educational Research and Training.
* [Odisha SCERT](https://scert.odisha.gov.in/) - Odisha State Council of Educational Research and Training.
* [Punjab SCERT](https://scert.punjab.gov.in/) - Punjab State Council of Educational Research and Training.
* [West Bengal SCERT](https://www.scertwb.org/) - West Bengal State Council of Educational Research and Training.

Before ingesting state textbooks or exam material, independently verify copyright and reuse permissions.

---

# Open-Source Learning Platforms

* [Sunbird ED](https://github.com/Sunbird-Ed) - Large-scale open-source digital education infrastructure used in India.
* [Kolibri](https://github.com/learningequality/kolibri) - Offline-first learning platform designed for low-connectivity environments. `OSS` `Offline`
* [Learning Equality - Kolibri](https://learningequality.org/kolibri/) - Project website and implementation resources.
* [Moodle](https://github.com/moodle/moodle) - Widely used open-source LMS. `OSS`
* [Open edX](https://github.com/openedx/edx-platform) - Open-source online-learning platform used at large scale. `OSS`
* [Oppia](https://github.com/oppia/oppia) - Open-source interactive learning platform.
* [H5P](https://h5p.org/) - Framework for interactive HTML5 educational content.
* [H5P Core](https://github.com/h5p/h5p-php-library) - Open-source H5P library.

---

# AI Tutors and Teacher Tools

## India-focused research/deployments

* [Shiksha Copilot](https://www.microsoft.com/en-us/research/blog/teachers-in-india-help-microsoft-research-design-ai-tool-for-creating-great-classroom-content/) - Microsoft Research India/Sikshana Foundation project for curriculum-grounded teacher lesson planning in Karnataka. `Research` `Education`
* [Teacher-AI Collaboration for Lesson Planning in Low-Resource Schools](https://deeshib.github.io/shiksha-copilot/) - Research site studying Shiksha Copilot deployment with Indian government-school teachers. `Research`
* [Microsoft Research publication on Shiksha Copilot](https://www.microsoft.com/en-us/research/publication/teacher-ai-collaboration-for-curating-and-customizing-lesson-plans-in-low-resource-schools/) - Large-scale study of teacher-AI collaboration in Karnataka. `Research`
* [Sarvam Voice Agents](https://docs.sarvam.ai/conversations/newly-launched) - Hosted end-to-end voice-agent platform for Indian conversational workflows, supporting 10 Indian languages plus English; relevant to multilingual tutoring, parent support and education-service interfaces. `API`

## General open research

* [Tutor CoPilot](https://github.com/rosewang2008/tutor-copilot) - Research/demo code for real-time AI assistance to human tutors. `Research`
* [Oppia](https://github.com/oppia/oppia) - Interactive/adaptive educational platform that can serve as a reference for tutoring flows.
* [Kolibri](https://github.com/learningequality/kolibri) - Offline learning infrastructure useful for delivering AI-assisted experiences in constrained environments.

This section should grow to include open-source projects for:

* Socratic tutoring
* teacher copilots
* lesson planning
* worksheet generation
* personalized practice
* reading tutors
* mathematics tutors
* science tutors
* language-learning tutors
* voice tutors
* doubt solving
* teacher professional development

---

# Assessment and Question Generation

Useful components include:

* question generation
* distractor generation
* rubric generation
* short-answer grading
* essay feedback
* mathematical grading
* competency mapping
* item difficulty estimation
* misconception detection
* adaptive testing

Relevant resources:

* [PARAKH](https://parakh.ncert.gov.in/) - India's national assessment body.
* [PARAKH Learning Assessment](https://parakh.ncert.gov.in/learning-assessment) - Competency-based assessment guidance.
* [NCERT Bench Lite](https://huggingface.co/datasets/ai4bharat/ncert-bench-lite) - Educational model evaluation.
* [NCERT Bench Vision Lite](https://huggingface.co/datasets/ai4bharat/ncert-bench-vision-lite) - Multimodal education evaluation.
* [QTI](https://www.1edtech.org/standards/qti) - Interoperability standard for questions and tests.
* [Moodle](https://github.com/moodle/moodle) - Mature open-source question-bank and assessment infrastructure.
* [Open edX](https://github.com/openedx/edx-platform) - Open assessment and course-delivery stack.

Generated assessment items should be teacher-reviewable and traceable to learning outcomes.

---

# Education Interoperability Standards

AI education systems should integrate into existing institutional infrastructure rather than forcing every institution onto a new platform.

## India

* [NDEAR](https://www.ndear.gov.in/) - India's national architecture for interoperable digital education.
* [NDEAR Policies and Standards](https://www.ndear.gov.in/policies-and-standards.html)
* [NDEAR Standards](https://standards.ndear.gov.in/)

## International

* [LTI](https://www.1edtech.org/standards/lti) - Learning Tools Interoperability; connects external tools such as AI tutors to LMS platforms.
* [QTI](https://www.1edtech.org/standards/qti) - Question and Test Interoperability for assessments/question banks.
* [OneRoster](https://www.1edtech.org/standards/oneroster) - Exchange of roster, course and grade information.
* [CASE](https://www.1edtech.org/standards/case) - Competencies and Academic Standards Exchange.
* [Common Cartridge](https://www.1edtech.org/standards/common-cartridge) - Portable course/content packaging.
* [Caliper Analytics](https://www.1edtech.org/standards/caliper) - Standardized learning-event analytics.
* [Open Badges](https://www.1edtech.org/standards/open-badges) - Portable digital credentials.
* [xAPI](https://xapi.com/overview/) - Learning-experience event standard.
* [SCORM](https://scorm.com/scorm-explained/) - Older but widely deployed e-learning content interoperability standard.
* [Schema.org LearningResource](https://schema.org/LearningResource) - Structured metadata for educational content.
* [Dublin Core](https://www.dublincore.org/specifications/dublin-core/) - General metadata standards useful for content repositories.

---

# Accessibility

AI education should support learners with disabilities from the architecture stage.

## India

* [Indian Sign Language Research and Training Centre](https://islrtc.nic.in/) - Government institution focused on Indian Sign Language.
* [ISLRTC Indian Sign Language Dictionary](https://islrtc.nic.in/isl-dictionary/) - Indian Sign Language dictionary resources.
* [CIET](https://ciet.ncert.gov.in/) - NCERT educational technology resources including accessible educational media.
* [ePathshala](https://ciet.ncert.gov.in/initiative/epathshala) - Digital content in multiple formats.

## Global standards/tools

* [WCAG](https://www.w3.org/WAI/standards-guidelines/wcag/) - Web Content Accessibility Guidelines.
* [WAI-ARIA](https://www.w3.org/WAI/standards-guidelines/aria/) - Accessibility semantics for web interfaces.
* [DAISY Consortium](https://daisy.org/) - Accessible publishing standards and tools.
* [NVDA](https://github.com/nvaccess/nvda) - Open-source screen reader.
* [eSpeak NG](https://github.com/espeak-ng/espeak-ng) - Lightweight speech synthesis/phonemization.

Accessibility-related AI opportunities include:

* automatic alt text
* text simplification
* TTS
* ASR
* sign-language tools
* accessible mathematics
* captioning
* dyslexia-friendly presentation
* image/diagram descriptions
* multilingual assistive interfaces

---

# Privacy, Safety and Governance

Education systems frequently process data about children. Treat this as high-sensitivity infrastructure.

## India

* [MeitY Acts and Policies](https://www.meity.gov.in/documents/act-and-policies) - Official source for India's digital laws and rules.
* [Digital Personal Data Protection Rules 2025](https://www.meity.gov.in/documents/act-and-policies/digital-personal-data-protection-rules-2025-gDOxUjMtQWa) - Final DPDP Rules, enforcement timeline and related notifications. `Government`
* [NDEAR Policies and Standards](https://www.ndear.gov.in/policies-and-standards.html) - Education-DPI policy and standards resources.

## International guidance

* [UNESCO Guidance for Generative AI in Education and Research](https://unesdoc.unesco.org/ark:/48223/pf0000386693) - Policy and governance guidance for GenAI in education.
* [UNICEF Policy Guidance on AI for Children](https://www.unicef.org/innocenti/reports/policy-guidance-ai-children) - Child-centered AI policy guidance.
* [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework) - General AI risk-management framework.
* [OWASP Top 10 for LLM Applications](https://owasp.org/www-project-top-10-for-large-language-model-applications/) - Application security issues relevant to educational AI.

Before deploying an AI education application, ask:

```text
Does it collect a learner's name?
Does it know the learner's age?
Does it record voice?
Does it store chats?
Does it store homework?
Does it store assessment results?
Does it infer ability or mastery?
Does it build a persistent learner profile?
Does it send data to an external model provider?
Does the provider retain inputs?
Can teachers inspect the model's reasoning/evidence?
Can students delete their data where applicable?
Can sensitive data leak through RAG?
Can one student retrieve another student's data?
Are minors using the system directly?
```

---

# Copyright and Data Licensing

Copyright and dataset licensing are core infrastructure concerns for AI education.

## India

* [ePathshala License](https://epathshala.nic.in/pages.php?id=license) - Terms covering NCERT digital educational content.
* [DIKSHA About and Licensing](https://diksha.gov.in/about-us/) - Includes information about licenses applied to DIKSHA/NCERT resources.
* [Open Government Data Platform India](https://data.gov.in/) - Government datasets.
* [Government Open Data License - India](https://www.data.gov.in/policies) - Open-data licensing framework.
* [Government Open Data License PDF](https://data.gov.in/sites/default/files/NDSAP_OpenDataLicense.pdf) - License text.

## General licensing resources

* [Creative Commons Licenses](https://creativecommons.org/share-your-work/cclicenses/) - Overview of Creative Commons licenses.
* [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) - Public-domain dedication used by this curated repository.
* [Choose a License](https://choosealicense.com/) - Practical guide to common software licenses.
* [SPDX License List](https://spdx.org/licenses/) - Standard identifiers for software/data licenses.
* [Open Source Initiative](https://opensource.org/licenses) - OSI-approved software licenses.

Keep these distinctions explicit:

```text
Publicly accessible ≠ Open source
Open source ≠ Open weights
Open weights ≠ Open data
Open data ≠ Permission to train
Non-commercial ≠ Open source
API access ≠ Redistribution rights
Downloadable ≠ Derivative works allowed
```

For each resource added to this repository, contributors should link to the canonical license where practical.

---

# Research and Evidence

## India and multilingual education

* [Shiksha Copilot Research](https://www.microsoft.com/en-us/research/blog/teachers-in-india-help-microsoft-research-design-ai-tool-for-creating-great-classroom-content/) - Curriculum-grounded teacher copilot developed with Indian educators.
* [Teacher-AI Collaboration for Curating and Customizing Lesson Plans in Low-Resource Schools](https://www.microsoft.com/en-us/research/publication/teacher-ai-collaboration-for-curating-and-customizing-lesson-plans-in-low-resource-schools/) - Large mixed-methods study with Indian government-school teachers.
* [IndicTrans2](https://arxiv.org/abs/2305.16307) - Research paper accompanying the 22-language translation system.
* [IndicIFEval](https://arxiv.org/abs/2602.22125) - Indic instruction-following benchmark research.
* [Airavata](https://arxiv.org/abs/2401.15006) - Hindi instruction-tuned LLM research.
* [AI4Bharat Publications](https://ai4bharat.iitm.ac.in/) - Entry point for Indian language AI research.
* [ASER Centre](https://asercentre.org/) - Research and measurement of foundational learning.
* [PARAKH](https://parakh.ncert.gov.in/) - National competency-based assessment research and frameworks.
* [Bodhan Open Research Problems in AI for Education](https://research.bodhan.ai/) - Open research agenda covering 200+ India-focused problems across speech, language, vision, safety and agentic systems for education. `Research` `Education`
* [SraVaani 1.0 Paper](https://arxiv.org/abs/2608.08235) - Research paper for the IISc/ARTPARK multilingual ASR model covering 65 Indian languages and dialects, including low-resource and tribal languages. `Research`

## Global AI-and-education guidance

* [UNESCO Generative AI in Education and Research](https://unesdoc.unesco.org/ark:/48223/pf0000386693)
* [UNICEF AI for Children](https://www.unicef.org/innocenti/reports/policy-guidance-ai-children)
* [Tutor CoPilot](https://github.com/rosewang2008/tutor-copilot) - Research on AI support for human tutors.
* [U.S. Department of Education - Responsible Use of Education Technology in the Classroom](https://www.ed.gov/about/news/press-release/us-department-of-education-releases-guidance-responsible-use-of-education-technology-classroom) - 2026 guidance emphasizing instructional value, evidence, educator judgement, transparency and student outcomes. `Government` `Education`

Research added here should ideally answer questions such as:

* Does AI improve learning?
* For which learners?
* Under what conditions?
* Does it help teachers?
* What failure modes occur?
* What happens in multilingual classrooms?
* What happens with low connectivity?
* What happens when students have low foundational literacy?
* Does performance differ by language or dialect?
* Does AI reduce or amplify educational inequality?

---

# Organizations

## India

* [AI4Bharat](https://ai4bharat.iitm.ac.in/) - Indian-language AI research.
* [BHASHINI](https://bhashini.gov.in/) - National language technology mission/platform.
* [BharatGen](https://bharatgen.com/) - Indian foundation-model initiative.
* [Sarvam AI](https://www.sarvam.ai/) - Indian foundation and language-model company.
* [Bodhan.AI](https://bodhan.ai/) - IIT Madras-incubated Centre of Excellence in AI for Education building the Bharat EduAI Stack.
* [IndiaAI](https://indiaai.gov.in/) - National AI ecosystem.
* [ARTPARK](https://artpark.in/) - AI and robotics ecosystem at IISc.
* [Vaani](https://vaani.iisc.ac.in/) - Indian speech-data initiative.
* [Karya](https://www.karya.in/) - Human-centered Indian AI data ecosystem.
* [EkStep Foundation](https://ekstep.org/) - Education digital public infrastructure.
* [Sunbird](https://www.sunbird.org/) - Open digital public infrastructure.
* [NCERT](https://ncert.nic.in/) - National educational research and curriculum body.
* [CIET](https://ciet.ncert.gov.in/) - National educational technology institution.
* [PARAKH](https://parakh.ncert.gov.in/) - National assessment centre.
* [Pratham](https://www.pratham.org/) - Large Indian education nonprofit.
* [ASER Centre](https://asercentre.org/) - Education assessment and research centre.
* [Sikshana Foundation](https://sikshana.org/) - Education nonprofit working with government schools.
* [C-DAC](https://www.cdac.in/) - National advanced computing institution.

## Global

* [Learning Equality](https://learningequality.org/) - Offline-first learning infrastructure.
* [1EdTech](https://www.1edtech.org/) - Education interoperability standards.
* [UNESCO](https://www.unesco.org/) - International education policy and research.
* [UNICEF](https://www.unicef.org/) - Child-centered education and AI policy.
* [Hugging Face](https://huggingface.co/) - Model/dataset ecosystem.
* [Ai2](https://allenai.org/) - Open AI research and models.

---

# Other Useful Catalogs

Avoid duplicating useful community work unnecessarily; cross-link it.

* [Indic LLM Resource Catalog](https://github.com/OdiaGenAI/Indic_LLM_Resource_Catalog) - Community catalogue of Indic LLMs and instruction datasets.
* [AI4Bharat Models](https://huggingface.co/ai4bharat/models) - Complete model catalogue.
* [AI4Bharat Datasets](https://huggingface.co/ai4bharat/datasets) - Complete dataset catalogue.
* [BharatGen Models](https://huggingface.co/bharatgenai/models) - BharatGen releases.
* [BharatGen Datasets](https://bharatgen.com/datasets/) - BharatGen benchmark and dataset catalogue.
* [Sarvam AI Models](https://huggingface.co/sarvamai) - Sarvam releases.
* [ARTPARK-IISc Models](https://huggingface.co/ARTPARK-IISc) - Vaani/ARTPARK language models.
* [BHASHINI Model Explorer](https://bhashini.gov.in/ulca/model/explore-models) - BHASHINI/ULCA model registry.
* [AIKosh](https://aikosh.indiaai.gov.in/) - IndiaAI dataset/model discovery platform.
* [Karya Data Catalogue](https://www.karya.in/data-catalogue/) - Indian-language speech datasets.
* [Open Government Data Platform India](https://data.gov.in/) - Government open datasets.

---

# Reference Build Paths

The following are not prescriptions. They illustrate how resources in this list fit together.

## Multilingual textbook RAG tutor

```text
Authorized curriculum / textbook content
              ↓
      Docling / Marker
              ↓
IndicPhotoOCR / PaddleOCR / Tesseract
              ↓
     document structure
              ↓
multilingual-e5 / BGE-M3
              ↓
     pgvector / Qdrant
              ↓
 curriculum-aware retrieval
              ↓
 Sarvam / BharatGen / Qwen / Gemma
              ↓
   citation-backed answer
              ↓
 education + Indic evaluation
```

Relevant links:

* [Docling](https://github.com/docling-project/docling)
* [IndicPhotoOCR](https://github.com/Bhashini-IITJ/IndicPhotoOCR)
* [PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)
* [multilingual-e5-large](https://huggingface.co/intfloat/multilingual-e5-large)
* [BGE-M3](https://huggingface.co/BAAI/bge-m3)
* [pgvector](https://github.com/pgvector/pgvector)
* [Qdrant](https://github.com/qdrant/qdrant)
* [Sarvam-30B](https://huggingface.co/sarvamai/sarvam-30b)
* [Param2](https://huggingface.co/bharatgenai/Param2-17B-A2.4B-Thinking)
* [NCERT Bench Lite](https://huggingface.co/datasets/ai4bharat/ncert-bench-lite)

## Voice-first tutor

```text
Microphone
    ↓
Language identification
    ↓
Indic ASR
    ↓
Transliteration / normalization
    ↓
Tutor / RAG model
    ↓
Pedagogical policy
    ↓
Indic TTS
    ↓
Audio response
```

Relevant links:

* [Vaani-LID](https://huggingface.co/ARTPARK-IISc/Vaani-LID_v0)
* [IndicConformerASR](https://github.com/AI4Bharat/IndicConformerASR)
* [IndicXlit](https://github.com/AI4Bharat/IndicXlit)
* [IndicF5](https://github.com/AI4Bharat/IndicF5)
* [Indic Parler-TTS](https://huggingface.co/ai4bharat/indic-parler-tts)

## Teacher copilot

```text
Board + grade + subject + chapter
              ↓
Curriculum / learning outcomes
              ↓
Authorized educational resources
              ↓
RAG / resource retrieval
              ↓
LLM
              ↓
lesson plan + examples + activity
              ↓
teacher review
              ↓
worksheet / assessment
              ↓
QTI / LMS export
```

Relevant references:

* [Shiksha Copilot](https://www.microsoft.com/en-us/research/blog/teachers-in-india-help-microsoft-research-design-ai-tool-for-creating-great-classroom-content/)
* [DIKSHA](https://diksha.gov.in/)
* [NDEAR](https://www.ndear.gov.in/)
* [QTI](https://www.1edtech.org/standards/qti)

## Offline school deployment

```text
Periodic Internet
      ↓
School server / teacher laptop
      ├── Kolibri / Sunbird content
      ├── local vector DB
      ├── quantized model
      ├── local ASR
      ├── local TTS
      └── queued telemetry
               ↓
         local Wi-Fi
               ↓
       student devices
```

Relevant links:

* [Kolibri](https://github.com/learningequality/kolibri)
* [Sunbird ED](https://github.com/Sunbird-Ed)
* [llama.cpp](https://github.com/ggml-org/llama.cpp)
* [whisper.cpp](https://github.com/ggerganov/whisper.cpp)
* [FAISS](https://github.com/facebookresearch/faiss)
* [ONNX Runtime](https://github.com/microsoft/onnxruntime)

## Multilingual content localization

```text
Source content
     ↓
OCR / parsing
     ↓
structure extraction
     ↓
IndicTrans / Sarvam Translate
     ↓
terminology validation
     ↓
human educator review
     ↓
localized content
```

Relevant links:

* [LekhaAnuvaad](https://github.com/bhashini-dibd/lekhaanuvaad)
* [IndicTrans2](https://github.com/AI4Bharat/IndicTrans2)
* [IndicTrans3](https://huggingface.co/ai4bharat/IndicTrans3-beta)
* [Sarvam Translate](https://huggingface.co/sarvamai/sarvam-translate)

---

# What Is Still Missing?

This repository should continuously expand coverage of areas that remain underrepresented.

Priority gaps include:

* child-speech datasets for Indian languages
* classroom-noise ASR benchmarks
* code-switched educational speech
* handwriting recognition for Indian scripts
* Indian mathematical OCR
* multilingual STEM terminology
* state-board-specific benchmarks
* competency-aligned question datasets
* Indian Sign Language AI
* tribal and low-resource languages
* multimodal textbook understanding
* school-level RAG benchmarks
* AI tutoring learning-gain studies in India
* accessibility benchmarks
* offline model benchmarks on low-cost Indian devices
* teacher-AI collaboration datasets
* student misconception datasets
* curriculum knowledge graphs
* open question banks with clear training licenses
* transparent copyright metadata for education datasets

Contributions in these areas are especially welcome.

---

# Contributing

Contributions are welcome.

The goal is **quality over quantity**.

## What belongs here?

A resource should be directly useful for building, deploying, evaluating, governing or researching AI-powered education systems in India.

Examples include:

* Indic LLMs
* multilingual models
* datasets
* educational datasets
* ASR
* speech datasets
* TTS
* machine translation
* transliteration
* code-mixing
* OCR
* document AI
* multimodal models
* embeddings
* rerankers
* retrieval/RAG
* annotation tools
* fine-tuning
* inference
* compute
* edge deployment
* education platforms
* curriculum resources
* assessments
* interoperability standards
* privacy
* safety
* accessibility
* research

## Preferred entry format

```md
- [Project Name](https://canonical-url.example/) - One concise sentence explaining why it matters. `Relevant tag`
```

## Prefer primary sources

Please prefer:

1. official GitHub repository
2. official Hugging Face model/dataset
3. official project website
4. official government portal
5. original research paper

Avoid linking to third-party articles when a primary source exists.

## Do not submit

* SEO listicles
* affiliate links
* generic AI directories
* thin wrappers around another product
* duplicate projects
* abandoned demo repositories with no reusable value
* resources with misleading descriptions
* pirated educational material
* datasets with unclear provenance presented as unquestionably open

## Licensing

Never describe something as open source simply because it is downloadable.

When known, distinguish:

```text
OSS
Open weights
Open data
Public access
API-only
Gated
Non-commercial
Commercial use allowed
Derivative works allowed
Training allowed
Unknown / unclear
```

For educational content, copyright and training rights deserve particular scrutiny.

## Descriptions

Descriptions should be factual rather than promotional.

Prefer:

> Multilingual ASR model covering 22 scheduled Indian languages.

Avoid:

> Revolutionary world-class model that transforms education forever.

## One resource may appear in multiple sections

A resource may legitimately belong in multiple places when it serves different discovery paths, but avoid unnecessary duplication.

## Link maintenance

If you find a dead link:

* open an issue
* submit a pull request
* replace it with the canonical successor where appropriate
* mark discontinued resources clearly rather than silently misrepresenting them

---

# Suggested Repository Topics

Useful GitHub topics for this repository:

```text
artificial-intelligence
education
india
edtech
indic
indic-languages
llm
machine-learning
nlp
datasets
speech-recognition
text-to-speech
ocr
machine-translation
rag
multilingual
education-technology
open-source
ai-for-education
digital-public-infrastructure
```

---

# Acknowledgements

This repository builds on work from researchers, educators, governments, nonprofits, open-source communities and language communities across India and the world.

Particular recognition is due to the communities behind:

* AI4Bharat
* BHASHINI
* BharatGen
* Sarvam AI
* Vaani / ARTPARK / IISc
* IndiaAI
* NDEAR
* DIKSHA
* Sunbird
* NCERT
* PARAKH
* Pratham / ASER Centre
* Karya
* EkStep Foundation
* Learning Equality
* open-source ML and education communities

No inclusion in this repository implies endorsement by, affiliation with, or endorsement of any listed organization.

---

# License

This curated repository is dedicated to the public domain under the [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) public-domain dedication.

You may copy, modify, distribute and reuse **this curated list** without asking permission, subject to the terms of CC0.

**Important:** CC0 applies only to original material in this repository.

Every external dataset, model, paper, textbook, API, software project and other linked resource remains subject to **its own copyright, license and terms of use**.

Always check the upstream license before using a linked resource for:

* model training
* fine-tuning
* redistribution
* commercial deployment
* derivative works
* translation
* RAG indexing
* synthetic-data generation

---

## Star the repository

If this map helps you build, research or teach with AI in India, consider starring the repository and contributing resources that others should know about.

**Built for an open, multilingual and accessible AI-for-education ecosystem in India. 🇮🇳**
