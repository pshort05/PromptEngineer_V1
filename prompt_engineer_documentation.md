# Expert Prompt Engineer System

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/Version-2.1.0-blue.svg)](https://github.com/your-username/expert-prompt-engineer)
[![Documentation](https://img.shields.io/badge/Documentation-Complete-green.svg)](./framework_documentation.md)

> **World-class prompt engineering system for crafting precise, complete, and effective LLM prompts**

## Overview

The Expert Prompt Engineer System is a comprehensive framework for evaluating and optimizing prompts across six key dimensions: Agent Directives, Anti-Hallucination protocols, Security Assessment, Output Formatting, Performance Optimization, and Advanced Techniques. Built by AI engineering experts, this system transforms basic prompts into production-ready, systematic problem-solving agents.

### Key Features

- 🎯 **Systematic Evaluation**: Multi-dimensional prompt analysis with 1-100 quality scoring
- 🛡️ **Security-First Design**: OWASP-aligned protection against prompt injection and jailbreaking
- 🤖 **Agent Directives**: Transform prompts into persistent, fact-checking, systematically-planning agents  
- 📊 **Flexible Output**: JSON default with XML, Markdown, and custom format support
- ⚡ **Performance Optimization**: Accuracy-first and cost-efficient modes with clear trade-offs
- 🔧 **Universal Integration**: Works with Claude, GPT-4, Gemini, and custom API implementations

## Table of Contents
1. [Quick Start Guide](#quick-start-guide)
2. [Installation & Usage](#installation--usage)
3. [Platform Integration](#platform-integration)
4. [API Integration](#api-integration)
5. [Advanced Configuration](#advanced-configuration)
6. [Framework Documentation](#framework-documentation)
7. [Contributing](#contributing)
8. [License](#license)

## Quick Start Guide

### What This System Does
The Expert Prompt Engineer System evaluates and optimizes prompts across six key dimensions:
- **Agent Directives**: Systematic problem-solving capabilities
- **Anti-Hallucination**: Fact verification and accuracy controls  
- **Security Assessment**: Prompt injection and vulnerability protection
- **Output Formatting**: Structured JSON responses with alternatives
- **Performance Optimization**: Accuracy-first vs. cost-efficient approaches
- **Advanced Techniques**: Few-shot learning, chain-of-thought reasoning

### 30-Second Setup
1. **Copy the system prompt** from [`optimized_prompt_engineer.json`](./optimized_prompt_engineer.json)
2. **Start a new conversation** in your preferred AI platform
3. **Paste the system prompt** and begin with:
   ```
   Review this prompt: "Write a marketing email for our new product."
   Context: This is for [use case] with priority: [accuracy/cost]
   ```

### What You Get
- ✅ Quality rating (1-100) with specific improvement areas identified
- ✅ Enhanced version with integrated security and agent frameworks  
- ✅ JSON-formatted recommendations for easy integration
- ✅ Implementation guidance tailored to your specific use case

---

## Installation & Usage

### Prerequisites
- Access to Claude, GPT-4, Gemini, or compatible LLM API
- Basic understanding of prompt engineering concepts
- JSON parsing capabilities for structured output (optional)

### Direct Chat Implementation
**For Claude (Recommended):**
```bash
# 1. Copy the complete system prompt from the JSON file
# 2. Start new conversation 
# 3. Paste system prompt
# 4. Begin evaluation:
```

```
Review this prompt: "Create a chatbot for customer service"
Context: High-security application for financial services
Priority: Accuracy-first approach
```

### Response Structure
```json
{
  "analysis": {
    "task_clarification": "Customer service chatbot with financial security requirements",
    "quality_rating": 75,
    "optimization_mode": "accuracy_first"
  },
  "evaluation": {
    "agent_directive_assessment": "Requires persistence and fact verification",
    "security_assessment": "High vulnerability - needs comprehensive protection",
    "format_recommendation": "JSON with response validation"
  },
  "recommendations": {
    "enhanced_prompt": "[Complete enhanced version with all frameworks]",
    "implementation_notes": ["Security boundaries required", "Add input validation"],
    "integration_guidance": "Implement Level 2 security with real-time monitoring"
  }
}
```

### Command Options
- **"Make it more cost-efficient"** → Switches to cost-optimization mode
- **"Add maximum security"** → Implements Level 3 security framework
- **"Output as XML"** → Changes to XML format
- **"Exclude agent directives"** → Provides basic prompt only

---

## Platform Integration

### Claude Projects Integration

**Setup Steps:**
1. **Create New Project** in Claude interface
2. **Add System Prompt**: Paste the complete JSON system in project knowledge
3. **Configure Instructions**:
```
You are Alex, the expert prompt engineer. Use the comprehensive prompt engineering system to evaluate and optimize user prompts. Always apply the universal frameworks unless explicitly told otherwise.
```

**Project Benefits:**
- ✅ Persistent evaluation standards across conversations
- ✅ Consistent framework application
- ✅ Context retention for iterative improvements
- ✅ Team collaboration on prompt optimization

**Usage in Projects:**
```
Simply type: "Evaluate this prompt for [use case]"
The system automatically applies all frameworks and provides comprehensive analysis.
```

### Custom GPTs Integration

**Adaptation Requirements:**
OpenAI's Custom GPT format requires conversion from JSON to natural language instructions.

**Setup Process:**
1. **Create New Custom GPT** in OpenAI interface
2. **Convert JSON to Instructions**:

```
You are Alex, an expert prompt engineer with 20+ years experience and PhD from MIT.

CORE EVALUATION FRAMEWORK:
- Analyze prompts using 3 diagnostic questions: input completeness, output type, intended effect
- Rate quality 1-100 based on clarity, completeness, effectiveness
- Apply universal agent directives: persistence, tool usage, deliberate planning
- Implement anti-hallucination protocols: separate facts from fiction, flag uncertainties
- Assess security vulnerabilities: prompt injection, jailbreaking, defense mechanisms
- Default to JSON output format unless user specifies otherwise
- Prioritize accuracy over cost unless user requests cost optimization

PROMPT TYPE TAXONOMY:
- Creative Writing: Character consistency, narrative coherence
- Data Analysis: Methodological rigor, calculation accuracy  
- Code Generation: Syntax perfection, security practices
- Conversational AI: Factual accuracy, context retention
- Educational Content: Subject matter accuracy, pedagogical soundness
- Business Analysis: Market data accuracy, analytical rigor

Always provide: Task clarification, quality rating, optimization suggestions with enhanced version including all frameworks.
```

**Custom GPT Limitations:**
- ⚠️ Cannot access full JSON structure complexity
- ⚠️ Limited context window for complete calibration examples
- ⚠️ No direct JSON manipulation capabilities
- ✅ Can still provide comprehensive evaluation and recommendations

### Gemini Gems Integration

**Setup in Google AI Studio:**
1. **Create New Gem** in AI Studio interface
2. **System Instructions**:

```json
{
  "role": "Expert Prompt Engineer",
  "identity": "Alex - PhD in ML/AI from MIT, founding OpenAI engineer",
  "capabilities": [
    "Comprehensive prompt evaluation across 6 dimensions",
    "Universal framework integration (agent directives, anti-hallucination, security)",
    "Multi-type prompt optimization (creative, analytical, technical, conversational)",
    "Accuracy-first optimization with cost-efficient alternatives"
  ],
  "evaluation_process": [
    "Deep analysis of prompt structure and objectives",
    "Security vulnerability assessment", 
    "Agent directive integration recommendations",
    "Anti-hallucination framework application",
    "JSON output format optimization",
    "Quality rating (1-100) with specific improvements"
  ],
  "output_format": "Structured analysis with enhanced prompt versions including all frameworks"
}
```

**Gemini-Specific Features:**
- ✅ Native JSON handling for complex structures
- ✅ Advanced reasoning capabilities for deep analysis
- ✅ Multi-modal input support for visual prompt elements
- ✅ Integration with Google Workspace tools

---

## API Integration

### REST API Implementation

**Endpoint Configuration:**
```python
import requests
import json

# Example using Claude API
def evaluate_prompt_with_expert_system(user_prompt, context="general", priority="accuracy"):
    
    system_prompt = """[Full JSON system from artifact]"""
    
    user_message = f"""
    Review this prompt: {user_prompt}
    Context: {context}
    Priority: {priority}
    """
    
    payload = {
        "model": "claude-3-sonnet-20240229",
        "max_tokens": 4000,
        "temperature": 0.1,  # Low for consistent analysis
        "system": system_prompt,
        "messages": [
            {"role": "user", "content": user_message}
        ]
    }
    
    response = requests.post(
        "https://api.anthropic.com/v1/messages",
        headers={
            "x-api-key": "your-api-key",
            "content-type": "application/json"
        },
        json=payload
    )
    
    return response.json()
```

**OpenAI API Adaptation:**
```python
import openai

def evaluate_with_openai(user_prompt):
    # Convert JSON system to text format for OpenAI
    system_content = """
    You are Alex, expert prompt engineer with MIT PhD and OpenAI founding experience.
    
    Evaluate prompts using:
    1. Diagnostic framework (input/output/effect analysis)
    2. Universal agent directives integration
    3. Anti-hallucination protocols
    4. Security vulnerability assessment
    5. JSON output format recommendations
    6. Quality rating (1-100) with improvements
    
    Always provide enhanced versions with integrated frameworks.
    """
    
    response = openai.ChatCompletion.create(
        model="gpt-4-turbo-preview",
        temperature=0.1,
        messages=[
            {"role": "system", "content": system_content},
            {"role": "user", "content": f"Evaluate this prompt: {user_prompt}"}
        ]
    )
    
    return response.choices[0].message.content
```

**Google AI API Implementation:**
```python
import google.generativeai as genai

def evaluate_with_gemini(user_prompt):
    genai.configure(api_key="your-api-key")
    model = genai.GenerativeModel('gemini-pro')
    
    system_instruction = """[Adapted system prompt for Gemini format]"""
    
    response = model.generate_content(
        f"{system_instruction}\n\nEvaluate this prompt: {user_prompt}",
        generation_config=genai.types.GenerationConfig(
            temperature=0.1,
            max_output_tokens=4000
        )
    )
    
    return response.text
```

### Batch Processing Setup

**Multiple Prompt Evaluation:**
```python
def batch_evaluate_prompts(prompt_list, context_list=None):
    results = []
    for i, prompt in enumerate(prompt_list):
        context = context_list[i] if context_list else "general"
        result = evaluate_prompt_with_expert_system(prompt, context)
        results.append({
            "original_prompt": prompt,
            "evaluation": result,
            "context": context
        })
    return results

# Usage example
prompts = [
    "Write a story about dragons",
    "Create a customer service chatbot", 
    "Analyze this financial data"
]
contexts = ["creative_writing", "conversational_ai", "data_analysis"]
results = batch_evaluate_prompts(prompts, contexts)
```

### Error Handling

```python
import time
import logging

def robust_prompt_evaluation(prompt, max_retries=3, backoff_factor=2):
    """Robust evaluation with retry logic and error handling"""
    for attempt in range(max_retries):
        try:
            result = evaluate_prompt_with_expert_system(prompt)
            return result
        except Exception as e:
            if attempt == max_retries - 1:
                logging.error(f"Failed to evaluate prompt after {max_retries} attempts: {e}")
                return {"error": str(e), "prompt": prompt}
            wait_time = backoff_factor ** attempt
            time.sleep(wait_time)
            logging.warning(f"Attempt {attempt + 1} failed, retrying in {wait_time}s: {e}")
```

## Advanced Configuration

### Agent Directives Customization

**Default Implementation:**
```json
{
  "persistence": "Continue until query completely resolved",
  "tool_usage": "Verify information rather than guessing", 
  "deliberate_planning": "Plan extensively before function calls"
}
```

**Domain-Specific Adaptations:**
```python
# Creative Writing
creative_directives = {
    "persistence": "Continue until story elements are consistent and complete",
    "tool_usage": "Research historical/cultural accuracy for world-building",
    "deliberate_planning": "Plan character arcs and plot development systematically"
}

# Data Analysis  
analytical_directives = {
    "persistence": "Continue until all calculations are verified and validated",
    "tool_usage": "Verify data sources and validate statistical methods",
    "deliberate_planning": "Plan analysis methodology before processing data"
}
```

**Excluding Agent Features:**
```
"Exclude agent directives - basic prompt only"
```

### Security Configuration

**Security Levels:**
- **Level 1**: Basic input validation and role boundaries
- **Level 2**: Multi-layered filtering with comprehensive test cases (Default)
- **Level 3**: Fine-tuned models with real-time analysis

**High-Risk Implementation:**
```python
max_security_config = {
    "input_validation": "comprehensive_sanitization",
    "output_monitoring": "real_time_analysis", 
    "injection_resistance": "fine_tuned_models",
    "audit_logging": "complete_interaction_logs"
}
```

### Output Format Options

**JSON (Default):**
```json
{
  "evaluation_summary": "string",
  "quality_score": "number",
  "improvements": ["array"],
  "enhanced_version": "string"
}
```

**XML for Enterprise:**
```xml
<prompt_evaluation>
    <analysis quality_rating="85" mode="accuracy_first"/>
    <recommendations>
        <enhanced_prompt>[Enhanced version]</enhanced_prompt>
    </recommendations>
</prompt_evaluation>
```

**Markdown for Documentation:**
```markdown
# Prompt Evaluation Results
**Quality Rating:** 85/100
## Enhanced Version
[Complete enhanced prompt with frameworks]
```

### Performance Modes

**Accuracy-First (Default):**
- Lower temperature settings (0.0-0.3)
- Comprehensive validation steps
- Generous context allocation (40-50%)
- Multiple examples and edge cases

**Cost-First Mode:**
```
"Prioritize cost efficiency" or "Optimize for token usage"
```
- Streamlined instructions  
- Higher temperature settings (0.4-0.7)
- Efficient context allocation (20-30%)
- Minimal but effective examples

## Framework Documentation

For detailed technical information about the core frameworks, see:

📖 **[Core Framework Documentation](./framework_documentation.md)**

This comprehensive guide covers:
- **[Agent Directives](./framework_documentation.md#agent-directives)**: Systematic problem-solving implementation
- **[Anti-Hallucination Guidelines](./framework_documentation.md#anti-hallucination-guidelines)**: Fact verification protocols
- **[Security Considerations](./framework_documentation.md#security-considerations)**: OWASP-aligned protection strategies
- **[Output Formats](./framework_documentation.md#output-formats-and-considerations)**: Format selection and optimization
- **[Accuracy vs Cost](./framework_documentation.md#accuracy-vs-cost-considerations)**: Performance trade-off strategies

Each section includes:
- Quick summaries for rapid understanding
- Detailed technical implementation guidance  
- External references to authoritative sources
- Real-world examples and code samples