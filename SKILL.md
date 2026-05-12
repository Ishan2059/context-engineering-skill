---
name: Context Engineering Expert
description: Master the art of context engineering for AI systems - design optimal information payloads, structure context windows, and build reliable AI workflows
version: 1.0.0
author: Ishan Mishra
tags: [context-engineering, ai-optimization, prompt-engineering, rag, memory-systems]
---

# Context Engineering Expert

## Overview

Context engineering is the systematic practice of designing, structuring, and optimizing the information provided to AI systems. Unlike prompt engineering (which focuses on *how* you ask), context engineering focuses on *what* the AI knows at each step.

This skill equips Claude with advanced context engineering principles, patterns, and techniques to help you build more reliable, efficient, and powerful AI systems.

## Core Principles

### 1. **Context Window Optimization**
- Prioritize information by relevance and recency
- Structure data hierarchically (most important first)
- Remove redundant or low-signal information
- Use compression techniques for large contexts

### 2. **Information Architecture**
- Layer context strategically: system → task → domain → specific
- Separate static knowledge from dynamic state
- Design clear boundaries between different context types
- Maintain context coherence across multi-turn interactions

### 3. **Retrieval-Augmented Generation (RAG)**
- Implement semantic search for relevant information retrieval
- Chunk documents optimally (typically 200-500 tokens)
- Use hybrid search (semantic + keyword) for better recall
- Re-rank retrieved results by relevance

### 4. **Memory Management**
- Short-term: Conversation history and immediate context
- Long-term: Persistent facts, preferences, and learned patterns
- Working memory: Active task state and intermediate results
- Episodic memory: Past interactions and outcomes

### 5. **Tool and Function Context**
- Provide clear tool descriptions and schemas
- Include usage examples and edge cases
- Specify expected inputs/outputs explicitly
- Document tool dependencies and prerequisites

## Context Engineering Patterns

### Pattern 1: Layered Context Architecture
```
[System Instructions]
  ↓
[Domain Knowledge]
  ↓
[Task-Specific Context]
  ↓
[User Input]
  ↓
[Retrieved Information]
```

### Pattern 2: Progressive Context Loading
Load context incrementally as needed rather than all at once:
1. Start with minimal essential context
2. Retrieve additional information based on task requirements
3. Expand context dynamically as conversation evolves
4. Prune irrelevant information periodically

### Pattern 3: Context Compression
- Summarize long documents before including them
- Extract key facts and entities
- Use structured formats (JSON, tables) over prose
- Reference external sources rather than embedding full content

### Pattern 4: Multi-Modal Context Integration
- Combine text, code, data, and metadata
- Maintain consistent formatting across modalities
- Use clear delimiters and section markers
- Preserve relationships between different information types

## Anti-Patterns to Avoid

❌ **Context Dumping**: Including everything without curation  
✅ **Selective Inclusion**: Only include relevant, high-signal information

❌ **Static Context**: Using the same context for all queries  
✅ **Dynamic Context**: Adapt context based on task and user intent

❌ **Flat Structure**: Unorganized information blob  
✅ **Hierarchical Organization**: Clear structure with priorities

❌ **Ignoring Recency**: Treating all information equally  
✅ **Temporal Awareness**: Prioritize recent and relevant information

❌ **Over-Retrieval**: Retrieving too many documents  
✅ **Precision Retrieval**: Fetch only the most relevant items (typically 3-5)

## Techniques and Best Practices

### For Developers Building AI Systems

1. **Design Context Schemas**
   - Define clear data structures for different context types
   - Use TypeScript/JSON Schema for validation
   - Version your context formats

2. **Implement Context Caching**
   - Cache static system instructions
   - Reuse common context across requests
   - Invalidate cache when context changes

3. **Monitor Context Quality**
   - Track context utilization metrics
   - Measure retrieval precision and recall
   - A/B test different context strategies

4. **Optimize for Cost and Latency**
   - Minimize token usage without sacrificing quality
   - Use prompt caching for repeated context
   - Batch similar requests when possible

### For Users Working with AI Assistants

1. **Provide Structured Context**
   - Use clear headings and sections
   - Include relevant background upfront
   - Reference specific files, docs, or data sources

2. **Specify Constraints and Requirements**
   - Define success criteria explicitly
   - Mention limitations and edge cases
   - Provide examples of desired outputs

3. **Build Context Incrementally**
   - Start with high-level goals
   - Add details as needed
   - Correct misunderstandings early

4. **Use Context References**
   - Link to documentation rather than pasting it
   - Reference previous conversations
   - Point to specific code sections or files

## Context Engineering Workflow

### Phase 1: Context Discovery
- Identify what information is needed
- Determine information sources
- Assess information quality and availability

### Phase 2: Context Design
- Structure information hierarchically
- Define retrieval strategies
- Plan memory and state management

### Phase 3: Context Implementation
- Build retrieval pipelines
- Implement caching and optimization
- Integrate with AI system

### Phase 4: Context Evaluation
- Test with real queries
- Measure performance metrics
- Iterate based on results

## Advanced Techniques

### Semantic Chunking
Break documents at semantic boundaries (paragraphs, sections) rather than fixed token counts.

### Context Routing
Direct different query types to different context sources or strategies.

### Adaptive Context Windows
Dynamically adjust context size based on query complexity and available budget.

### Context Fusion
Combine information from multiple sources with conflict resolution.

### Temporal Context Weighting
Apply decay functions to older information while preserving critical facts.

## Tools and Technologies

- **Vector Databases**: Pinecone, Weaviate, Qdrant, ChromaDB
- **Embedding Models**: OpenAI Ada, Cohere, Sentence Transformers
- **RAG Frameworks**: LangChain, LlamaIndex, Haystack
- **Memory Systems**: Mem0, Zep, Redis
- **Observability**: LangSmith, Helicone, Weights & Biases

## Evaluation Metrics

- **Retrieval Precision**: Relevant items / Retrieved items
- **Retrieval Recall**: Retrieved relevant items / Total relevant items
- **Context Utilization**: Used tokens / Total context tokens
- **Response Quality**: Accuracy, completeness, relevance
- **Latency**: Time to retrieve and process context
- **Cost**: Token usage and API costs

## Use Cases

### Software Development
- Provide codebase context for AI coding assistants
- Include relevant files, functions, and dependencies
- Reference documentation and style guides

### Customer Support
- Load customer history and preferences
- Include product documentation and FAQs
- Maintain conversation context across sessions

### Research and Analysis
- Retrieve relevant papers and articles
- Organize information by topic and relevance
- Synthesize findings from multiple sources

### Content Creation
- Provide brand guidelines and style references
- Include previous content for consistency
- Reference target audience and goals

### Data Analysis
- Include schema and data dictionaries
- Provide sample queries and results
- Reference business context and KPIs

## How I Can Help

When you work with me using this skill, I will:

✅ Analyze your context engineering needs and recommend optimal strategies  
✅ Design context architectures for your AI systems  
✅ Implement RAG pipelines with proper chunking and retrieval  
✅ Optimize context windows for cost and performance  
✅ Debug context-related issues in AI applications  
✅ Review and improve existing context engineering implementations  
✅ Suggest tools and frameworks for your use case  
✅ Provide code examples and implementation guidance  

## Getting Started

To leverage this skill effectively:

1. **Describe your AI system or use case**
2. **Share what context you're working with** (documents, code, data, etc.)
3. **Explain your goals** (accuracy, cost, latency, etc.)
4. **Ask specific questions** about context design, retrieval, or optimization

## Example Queries

- "Help me design a RAG system for our technical documentation"
- "How should I structure context for a multi-turn coding assistant?"
- "Review my context engineering approach and suggest improvements"
- "What's the best way to chunk and embed our knowledge base?"
- "How can I reduce context costs while maintaining quality?"
- "Design a memory system for our customer support chatbot"

## References and Further Reading

- Andrej Karpathy: "Context engineering is the delicate art and science of filling the context window with just the right information for the next step"
- Research: "A Survey of Context Engineering for Large Language Models" (arXiv)
- Best practices from production AI systems at scale
- Emerging patterns from the AI development community

---

**Version History**
- v1.0.0 (2026): Initial release with core principles, patterns, and techniques

**License**: MIT - Free to use, modify, and share

**Contributions**: Feedback and improvements welcome!
