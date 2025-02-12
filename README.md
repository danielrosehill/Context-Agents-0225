# 🤖 Context Development Agents - Feb 2025 🚀

*Personal RAG Pipeline Creation with AI Interview Bot Workflow*

[![Context Development](https://img.shields.io/badge/Context%20Development-blue?style=flat-square)](https://example.com/context-development)

This repository showcases a workflow for creating personal RAG pipelines using AI interview bots. It includes agent configurations for building and managing contextual information, leveraging vector stores to enhance RAG pipelines. The ultimate goal is to connect this knowledge store to agents for more relevant and targeted guidance.

## Agent Roles and Workflow

In modern AI applications, specialized agents are increasingly used to handle specific tasks. This project is my exploration of using such agents to build a **personal context data store**, improving the performance and relevance of AI interactions. The core idea is that by engaging in "**interviews**" with AI agents, I can cultivate a **robust contextual data knowledge store** that reflects my unique experiences, skills, and goals.

During my experimentation, I created various agents, each tailored to a specific aspect of the context development process. These configurations reflect different approaches and strategies for building a **comprehensive context profile** and a **powerful contextual data knowledge store**.

For example, my initial "**interviewer**" agent asked questions randomly to gather information. A later version was connected to the **contextual data vector store**, allowing it to refine its questions based on existing data. This iterative approach aimed to optimize the interviewing process by targeting questions based on **identified knowledge gaps** and **enriching the contextual data knowledge store**.

The envisioned workflow (V1) can involve either a single agent handling all tasks or multiple specialized agents working together. I favor the latter approach for its **modularity and maintainability**, allowing each agent to focus on a specific part of the task. This isolation simplifies **debugging, testing, and future enhancements** to the agents and the **overall contextual data knowledge store**.

In addition to configurations that attempt to automate the entire context development process, there's also a standalone agent dedicated to parsing raw interview data and converting it into **structured context snippets** for inclusion in the **knowledge store**.

A planning agent is also included, which doesn't directly participate in interviewing or parsing but assists me in ideating and planning my context data development efforts, ensuring the **knowledge store** is **comprehensive and well-organized**.

## Agent Configuration Summary

| Agent Configuration | Description | Raw Config | JSON Config |
|---|---|---|---|
| [General Interviewer](agent-configs/interviewers/interviewer-general.md) | This agent conducts interviews with me to generate contextual data. It asks questions at random and structures the output in a specific format suitable for **vector storage**, contributing to the **overall contextual data knowledge store**. | [![Raw Config](https://img.shields.io/badge/Raw%20Config-blue)](agent-configs/interviewers/interviewer-general.md) | [![JSON Config](https://img.shields.io/badge/JSON%20Config-blue)](agent-configs/interviewers/json/interviewer-general.json) |
| [Gap-Filler Interviewer](agent-configs/interviewers/interviewer-gap-filler.md) | This agent identifies and fills in gaps in existing contextual data about me. It takes a proactive approach, probing areas that need **development and enrichment** to create a **more complete context profile** and a **more comprehensive knowledge store**. | [![Raw Config](https://img.shields.io/badge/Raw%20Config-blue)](agent-configs/interviewers/interviewer-gap-filler.md) | [![JSON Config](https://img.shields.io/badge/JSON%20Config-blue)](agent-configs/interviewers/json/interviewer-gap-filler.json) |
| [Context Extractor](agent-configs/parsers/extractor.md) | This agent acts as a text formatting tool, extracting contextual data from unstructured text and reformatting it in the third person. This is useful for converting existing documents into **context snippets** for inclusion in the **contextual data knowledge store**. | [![Raw Config](https://img.shields.io/badge/Raw%20Config-blue)](agent-configs/parsers/extractor.md) | [![JSON Config](https://img.shields.io/badge/JSON%20Config-blue)](agent-configs/parsers/json/extractor.json) |
| [Context Planner](agent-configs/planners/helper.md) | This agent assists me in planning my context data development efforts. It provides recommendations and suggestions for specific context snippets to develop, helping to guide the overall process of building a **comprehensive and well-organized knowledge store**. | [![Raw Config](https://img.shields.io/badge/Raw%20Config-blue)](agent-configs/planners/helper.md) | [![JSON Config](https://img.shields.io/badge/JSON%20Config-blue)](agent-configs/planners/json/helper.json) |

## Implementation Sketch

To set up an actual workflow for building my **contextual data knowledge store**, I would typically follow these steps:

1.  **Choose a Vector Database:** Select a **vector database** to store my context data. Options include:
    *   **Pinecone:** A fully managed vector database ideal for production environments.
    *   **Milvus:** An open-source vector database that offers high performance and scalability.
    *   **Weaviate:** A graph-based vector database that supports complex data relationships.
    *   **FAISS:** A library for efficient similarity search and clustering of dense vectors, suitable for smaller-scale projects.

2.  **Set up the Agents:** Configure the agents described above, ensuring they can access and interact with the **vector database**. This typically involves setting up API keys and authentication credentials, allowing them to contribute to and access the **contextual data knowledge store**.

3.  **Create a Data Pipeline:** Implement a data pipeline to process the output from the agents and store it in the **vector database**. This might involve using tools like:
    *   **Langchain:** A framework for building applications powered by language models.
    *   ** নিজস্ব scripts:** Custom scripts written in Python or other languages to handle data transformation and loading into the **knowledge store**.

4.  **Develop a RAG Pipeline:** Build a Retrieval-Augmented Generation (RAG) pipeline that retrieves context data from the **vector database** and uses it to enhance the responses of a large language model. This can be implemented using frameworks like Langchain or Haystack, enabling more **relevant and targeted interactions** with AI agents.

## Use Cases

See [use-cases/personal.md](use-cases/personal.md) for personal use cases and [use-cases/business.md](use-cases/business.md) for business use cases.

## Workflow Examples

See [workflows.md](workflows.md) for detailed workflow examples.

## Contributing

I welcome contributions to this repository! If you have any ideas for new agents, improvements to existing agents, or other enhancements, please feel free to submit a pull request.

I invite you to discuss these ideas further! You can find me at [danielrosehill.com](https://danielrosehill.com) or reach out via email at public@danielrosehill.com.

Check out an example of a context-driven interview [here](examples/short-job-interview/1.md).

## Related Repositories

| Repository | Description |
|---|---|
| [![Workflow](https://img.shields.io/badge/Workflow-blue?logo=github)](https://github.com/danielrosehill/Personal-RAG-Agent-Workflow) | Several workflows have been mapped out for using agents to proactively build a store of personal data. One approach involves connecting the interviewing agent to a growing personal contacts data store. Another approach involves using the interviewing agent and then manually feeding in the data. |
| [![Agentic Context Development Interview Demo](https://img.shields.io/badge/Agentic%20Context%20Development%20Interview%20Demo-blue?logo=github)](https://github.com/danielrosehill/Agentic-Context-Development-Interview-Demo) | This Streamlit application models a basic AI agent interview process. The interviewing agent asks the user questions at random, and the user can periodically download the gathered contextual data. |
| [![Personal-Context-Store-Ideation](https://img.shields.io/badge/Personal--Context--Store--Ideation-blue?logo=github)](https://github.com/danielrosehill/Personal-Context-Store-Ideation) | This repository contains general notes regarding the personal context or ideation idea and why it could be highly beneficial for AI users from a privacy protection standpoint. |
| [![Context Data Generation Bot](https://img.shields.io/badge/Context%20Data%20Generation%20Bot-blue?logo=github)](https://github.com/danielrosehill/Context-Data-Generation-Bot) | This is an individual configuration for a context data generation bot. |
| [![Personal Context Repo Idea](https://img.shields.io/badge/Personal%20Context%20Repo%20Idea-blue?logo=github)](https://github.com/danielrosehill/Personal-Context-Repo-Idea) | This repository outlines the personal context repo idea. |
| [![Demo public context repo](https://img.shields.io/badge/Demo%20public%20context%20repo-blue?logo=github)](https://github.com/danielrosehill/My-LLM-Context-Repo-Public) | This is a demo public context repository. |

12-Feb-25

## Repo Map

*   [Evaluation Prompts](resources/eval-prompts.md)
*   [General Interviewer Config](agent-configs/interviewers/interviewer-general.md)
*   [Gap-Filler Interviewer Config](agent-configs/interviewers/interviewer-gap-filler.md)
*   [Context Extractor Config](agent-configs/parsers/extractor.md)
*   [Context Planner Config](agent-configs/planners/helper.md)

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