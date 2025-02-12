# Context Development Agent Configurations - Feb 2025

*12-Feb-25*

This repository contains agent configurations designed to facilitate personal context data development workflows. These agents are intended to proactively develop personal contextual data for storage in a vector store, ultimately enhancing personal context RAG pipelines.

## Agent Roles and Workflow

In AI-driven tools, it's becoming increasingly common to employ specialized agents for specific tasks. This project explores the use of such agents to build a personal context data store.

During experimentation, various agents were created, each tailored to slightly different aspects of the context development process. These configurations reflect different approaches to the task.

For instance, the initial "interviewer" agent asked questions randomly. A later version connected to the contextual data vector store, refining its questions based on existing data. This evolution aimed to streamline the interviewing process by targeting questions based on identified needs.

The envisioned workflow (V1) can involve either a single agent handling all tasks or multiple specialized agents. The latter approach is favored for its modularity, allowing each agent to focus on a specific part of the task. This isolation simplifies debugging and testing.

Therefore, in addition to configurations that attempt to take the context development process from initiation to database writing, there's also a standalone agent dedicated to parsing raw interview data.

A planning agent is also included, which doesn't directly participate in interviewing or parsing but assists the user in ideating the overall project of generating personal contextual data.

## Agent Configuration Summary

| Agent Configuration | Description |
|---|---|
| [General Interviewer](interviewers/interviewer-general.md) | This agent conducts interviews with the user to generate contextual data. It asks questions at random and structures the output in a specific format suitable for vector storage. |
| [Gap-Filler Interviewer](interviewers/interviewer-gap-filler.md) | This agent identifies and fills in gaps in existing contextual data about the user. It takes a proactive approach, probing areas that need development and enrichment to create a more complete context profile. |
| [Context Extractor](parsers/extractor.md) | This agent acts as a text formatting tool, extracting contextual data from unstructured text and reformatting it in the third person. This is useful for converting existing documents into context snippets. |
| [Context Planner](planners/helper.md) | This agent assists the user in planning their context data development efforts. It provides recommendations and suggestions for specific context snippets to develop, helping to guide the overall process. |

## Orchestration and Implementation

These experiments are open-sourced to encourage collaboration and exploration in the field of AI agent orchestration and implementation. If you're interested in using agents in a similar manner, feel free to reach out and collaborate.

### Workflow Examples

[![Workflow](https://img.shields.io/badge/Workflow-blue?logo=github)](https://github.com/danielrosehill/AI-Interview-Workflow-V2)

Several workflows have been mapped out for using agents to proactively build a store of personal data.

One approach involves connecting the interviewing agent to a growing personal contacts data store.

Another approach involves using the interviewing agent and then manually feeding in the data.

### Agentic Context Development Interview Demo

[![Agentic Context Development Interview Demo](https://img.shields.io/badge/Agentic%20Context%20Development%20Interview%20Demo-blue?logo=github)](https://github.com/danielrosehill/Agentic-Context-Development-Interview-Demo)

This Streamlit application models a basic AI agent interview process. The interviewing agent asks the user questions at random, and the user can periodically download the gathered contextual data.

### Personal-Context-Store-Ideation

[![Personal-Context-Store-Ideation](https://img.shields.io/badge/Personal--Context--Store--Ideation-blue?logo=github)](https://github.com/danielrosehill/Personal-Context-Store-Ideation)

This repository contains general notes regarding the personal context or ideation idea and why it could be highly beneficial for AI users from a privacy protection standpoint.

### Context Data Generation Bot

[![Context Data Generation Bot](https://img.shields.io/badge/Context%20Data%20Generation%20Bot-blue?logo=github)](https://github.com/danielrosehill/Context-Data-Generation-Bot)

This is an individual configuration for a context data generation bot.

### Personal Context Repo Idea

[![Personal Context Repo Idea](https://img.shields.io/badge/Personal%20Context%20Repo%20Idea-blue?logo=github)](https://github.com/danielrosehill/Personal-Context-Repo-Idea)

This repository outlines the personal context repo idea.

### Demo public context repo

[![Demo public context repo](https://img.shields.io/badge/Demo%20public%20context%20repo-blue?logo=github)](https://github.com/danielrosehill/My-LLM-Context-Repo-Public)

This is a demo public context repository.

12-Feb-25

## Author

Daniel Rosehill
(public at danielrosehill dot com)

## Licensing

This repository is licensed under CC-BY-4.0 (Attribution 4.0 International)
[License](https://creativecommons.org/licenses/by/4.0/)

### Summary of the License

The Creative Commons Attribution 4.0 International (CC BY 4.0) license allows others to:

- **Share**: Copy and redistribute the material in any medium or format.
- **Adapt**: Remix, transform, and build upon the material for any purpose, even commercially.

The licensor cannot revoke these freedoms as long as you follow the license terms.

#### License Terms

- **Attribution**: You must give appropriate credit, provide a link to the license, and indicate if changes were made. You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- **No additional restrictions**: You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.

For the full legal code, please visit the [Creative Commons website](https://creativecommons.org/licenses/by/4.0/legalcode).