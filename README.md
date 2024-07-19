## Introduction

After a few months spent on acquiring the basics of data science and machine learning, with this project I aim to use that knowledge hands-on with LLM via prompting. I will be playing with the dataset I have previously worked on for the Apziva project "Potential talents". The goal of the project was to streamline the first selection round of potential candidates by ranking their fit based on the semantic similarity between their job title and a (series of) specific keywords such as “full-stack software engineer”, “engineering manager”, or “aspiring human resources”. Here, I will basically bypass under-the-hood coding, and ask LLMs to do the same by providing a viable prompt.

The core of the notebook will basically focus on prompt viability, (often referred to as _prompt engineering_), i.e. design of prompts ensuring the optimal output.

## Prerequisites

- `pandas`
- `huggingface_hub`
- `transformers`
- `torch`

## LLMs used

I extensively played with three well-known, and highly performative models: Mistral, Llama, and Phi from the huggingface models repository.

## Conclusions

Out of the three LLMs tested, `Mistral-7B-Instruct-v0.3` handled the complex task effectively, despite requiring a detailed and lengthy prompt. The real challenge was not with LLMs or prompt engineering, but with the computational setup both locally and remotely. In particular, in the cloud, memory issues persisted even after purchasing compute units. This highlights a significant accessibility issue in AI research. Standard machines' computing limitations make online computing the only viable option for many, yet services like Google Colab and AWS don’t offer enough memory, even with subscriptions. This creates a barrier for amateurs, beginners, and independent researchers, underscoring the need for more accessible and affordable computing solutions to democratize access to AI tools.

A solution to this was found in letting the `langchain` library to handle the computational part of the workflow, thus bypassing the computational issues aforementioned. I explore this in the companion notebook `llm-prompting_langchain_potential-talents.ipynb`, which hold promise to create a ecologically and ethically valid workflow for all researchers.
