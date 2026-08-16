# BOS AI Copilot

[![.NET](https://img.shields.io/badge/.NET-9-512BD4)](https://dotnet.microsoft.com/)
[![C#](https://img.shields.io/badge/C%23-13-239120)](https://learn.microsoft.com/dotnet/csharp/)
[![Semantic Kernel](https://img.shields.io/badge/Semantic%20Kernel-AI-blue)](https://github.com/microsoft/semantic-kernel)
[![Status](https://img.shields.io/badge/status-active%20development-orange)](#project-status)

**BOS AI Copilot** is a .NET AI Engineering project that explores how LLMs, Semantic Kernel, native C# tools and structured outputs can support the creation, analysis and evolution of software projects based on the BOS Framework.

The repository is intentionally public while the project evolves, so it also serves as a practical record of the engineering decisions involved in building an LLM-powered application with .NET.

> **Current stage:** active development. The architecture and capabilities are evolving incrementally; this README distinguishes implemented foundations from planned capabilities.

## Why this project exists

Project ideas usually begin with incomplete, ambiguous or unstructured information. The goal of BOS AI Copilot is to help transform that initial input into something an engineer can reason about and review.

The assistant is designed to:

1. understand the user's project intent;
2. identify missing information;
3. select appropriate deterministic tools when needed;
4. produce structured results;
5. keep the human in the review and decision loop.

## Example use case

> **User:** I want to start a project to automate restaurant customer service through WhatsApp.

The copilot can progressively analyze the request, identify information gaps, invoke appropriate functions and generate structured project information for human review.

## Project status

### Implemented foundations

- .NET solution separated into API, Core and Plugins projects
- LLM integration
- Semantic Kernel integration
- Native C# plugins / tools
- Function calling foundations
- Conversation-oriented interaction
- External prompt structure
- Dependency Injection
- Configuration and application structure prepared for incremental evolution

### In progress / evolving

- richer project-analysis workflows
- additional BOS-oriented plugins
- structured project artifacts
- stronger automated test coverage
- retrieval capabilities and knowledge grounding

### Future evolution

- Retrieval-Augmented Generation (RAG)
- embeddings and vector retrieval
- MCP integration
- more advanced agentic workflows
- persistent memory where justified
- deeper BOS document integration
- production-oriented evaluation and observability

## Architecture

```text
BOS-AI-Copilot/
├── docs/                      # Technical and project documentation
├── prompts/                   # Externalized AI prompts
├── src/
│   ├── BosAiCopilot.Api/      # API / application entry point
│   ├── BosAiCopilot.Core/     # Core contracts and application logic
│   └── BosAiCopilot.Plugins/  # Native C# tools exposed to the AI layer
└── tests/                     # Automated tests
```

The project intentionally separates the AI orchestration layer from deterministic application capabilities. Business operations that can be expressed reliably in C# should remain deterministic tools rather than being delegated unnecessarily to the model.

## Engineering principles

This project is not intended to be only a prompt demo. The implementation is guided by software-engineering concerns that become especially important in AI applications:

- explicit separation of responsibilities
- deterministic tools for deterministic operations
- structured outputs instead of free-form text where appropriate
- dependency injection and testability
- externalized prompts and configuration
- secure secret management
- incremental architecture
- human review for generated project artifacts

## Tech stack

- **.NET / C#**
- **ASP.NET Core**
- **Microsoft Semantic Kernel**
- **LLM integration**
- **Native C# plugins / function calling**
- **JSON structured outputs**
- **xUnit** for automated testing

## Planned plugin areas

The project evolves through focused capabilities rather than a single monolithic agent.

### Project analysis

Examples of intended operations:

- create a project draft
- identify missing information
- define objectives
- define success criteria
- classify project stage

### Deterministic calculations

Examples:

- token-cost estimation
- monthly operating-cost estimation
- cost per interaction
- date and deadline calculations

### Artifact assistance

Examples:

- initial project-charter structure
- requirement drafts
- acceptance-criteria drafts

## Running locally

Clone the repository:

```bash
git clone https://github.com/wilfigueredo/BOS-AI-Copilot.git
cd BOS-AI-Copilot
```

Restore and build:

```bash
dotnet restore
dotnet build
```

Run the automated tests:

```bash
dotnet test
```

The application requires the appropriate LLM provider configuration and API credentials. Secrets should be provided through local secret management or environment configuration and must not be committed to the repository.

## Roadmap

The roadmap is intentionally incremental:

```text
LLM integration
      ↓
Semantic Kernel
      ↓
Native tools / function calling
      ↓
Structured workflows
      ↓
Retrieval / RAG
      ↓
Evaluation & observability
      ↓
More advanced agentic capabilities
```

The objective is to introduce complexity only when the previous layer is understood and testable.

## Portfolio context

BOS AI Copilot is part of my transition from **Software Engineering → AI Engineering**. It applies a long-standing .NET and software-architecture background to modern LLM application development, with emphasis on maintainability, deterministic behavior, testing and production-oriented engineering practices.

---

**William Figueiredo**  
Software Engineering → AI Engineering
