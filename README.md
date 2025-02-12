# Context Development Agent Configs - Feb 2025

*12-Feb-25*

This repository is a collection of agents for personal context data development workflows that I have been working with to date.

## How These Agents Fit And Work Together

In AI tools that leverage agents, it's increasingly common to have specific agents tasked with aspects of the overall job. 

A project I have been working on Is leveraging AI agents to proactively develop personal contextual data for storage in a vector store and ultimately for use in personal context RAG pipelines. 

During my experiments, I found it necessary to create different agents, all for slightly different aspects of this job. Some of the configurations reflect slight differences in the approaches I've been experimenting with to date. 

For example, the first interviewing agent was my original configuration and simply asks the user questions more or less at random. A later iteration of the interviewing agent is connected to the contextual data vector store and therefore refines its question a little bit based upon what it knows is already in the database. My thinking was this evolution was that the interviewing process could be rendered more streamlined by targeting the questions according to need. 

In the chained workflow envisioned (I've just created V1), there can either be one agent who tries to do it all, or multiple agents specializing on parts of the workflow. My opinion is that the second approach is likely much more appropriate. Each agent can focus on one part of the task and for debugging and troubleshooting. It also makes life a bit easier, although of course it means configuring workflows

That's why, for example, in addition to having agent configurations that try to take the context development process from initiation through to writing to a database (envisioned as using a tool for vector storage writing), there is also a stand alone agent whose purpose is just to parse the raw interview data gathered. 

Finally, I believe it's important to have a planning agent which doesn't get involved directly in the actual interviewing or parsing of the context data, but which rather helps the user to ideate the overall project of generating personal contextual data. That is the planner configuration in the repository.

## Orchrestration / Implementation 

I open source my experiments with the hope that anyone else interested in AI might wish to attempt to model these experiments themselves. AI, agent, orchestration and implementation is a new field. And I encourage anyone else looking at using agents in a similar manner to reach out and see how we could collaborate. 

### Workflow

[![Workflow](https://img.shields.io/badge/Workflow-blue?logo=github)](https://github.com/danielrosehill/AI-Interview-Workflow-V2)

I've mapped out a couple of workflows to date for using agents to proactively build up a store of personal data. 

One approach is, as described in the above repository, connecting the interviewing agent to your growing personal contacts data store. 

Another approach is simply using the interviewing agent and then feeding in the data. 

### Agentic Context Development Interview Demo

[![Agentic Context Development Interview Demo](https://img.shields.io/badge/Agentic%20Context%20Development%20Interview%20Demo-blue?logo=github)](https://github.com/danielrosehill/Agentic-Context-Development-Interview-Demo)

This is a Streamlit application which models a basic AI agent interview process. The interviewing agent asked the user questions at random. The user answers and periodically can download the contextual data gathered. 

### Personal-Context-Store-Ideation

[![Personal-Context-Store-Ideation](https://img.shields.io/badge/Personal--Context--Store--Ideation-blue?logo=github)](https://github.com/danielrosehill/Personal-Context-Store-Ideation)

General notes regarding the personal context or ideation idea and why I think from a privacy protection standpoint it could be highly beneficial for AI users.

### Context Data Generation Bot

[![Context Data Generation Bot](https://img.shields.io/badge/Context%20Data%20Generation%20Bot-blue?logo=github)](https://github.com/danielrosehill/Context-Data-Generation-Bot)

 This is an individual configuration for a context data generation bot. 

### Personal Context Repo Idea

[![Personal Context Repo Idea](https://img.shields.io/badge/Personal%20Context%20Repo%20Idea-blue?logo=github)](https://github.com/danielrosehill/Personal-Context-Repo-Idea)

Personal-Context-Repo-Idea

### Demo public context repo

[![Demo public context repo](https://img.shields.io/badge/Demo%20public%20context%20repo-blue?logo=github)](https://github.com/danielrosehill/My-LLM-Context-Repo-Public)

My-LLM-Context-Repo-Public

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