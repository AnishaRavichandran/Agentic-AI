# Agentic AI Blog Generator

## Project Overview
This project uses a multi-agent AI system to generate blog posts based on a user-provided topic. It identifies the appropriate blog genre, generates a draft, refines the content through iterative feedback, and evaluates the final output.

## Features
- **Genre Identification:** Classifies the topic into categories such as Health, News, Fashion, Business, Tech, and BibleApp.
- **Blog Generation:** Generates an initial blog draft using a Gemini language model and Google Search.
- **Automated Critique:** Reviews the draft for factual accuracy, readability, structure, tone, and genre-specific requirements.
- **Iterative Refinement:** Improves the draft based on feedback, with a maximum of two refinement-loop iterations.
- **LLM-Based Evaluation:** Scores the final blog on factuality, instruction adherence, and style/format using a structured evaluation schema.

## Tech Stack
- Python
- Google Agent Development Kit (ADK)
- Gemini 2.5 Flash-Lite
- Google Search
- Pydantic

## Workflow
1. The user provides a blog topic.
2. The Genre Identifier Agent determines the appropriate genre.
3. The Initial Writer Agent generates a blog draft.
4. The Critic Agent reviews the draft and provides feedback.
5. The Refiner Agent revises the draft based on the feedback.
6. The Judge Agent evaluates the final output and provides scores and an overall verdict.

## Key Insights
This project demonstrates :
- Multi-agent orchestration
- A2A (Agent-to-agent) interaction by state sharing
- Tool usage (google_search)
- Structured evaluation using LLM as a judge

## Future Enhancements
- Independent Judge Model: Use a different LLM for evaluation to reduce potential self-evaluation bias.
- Observability and Tracing: Implement logging, execution traces, and observability to monitor agent interactions, identify errors, and improve evaluation.
