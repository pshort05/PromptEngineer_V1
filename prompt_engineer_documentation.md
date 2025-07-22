# Expert Prompt Engineer System - Documentation Guide

## Table of Contents
1. [Quick Start Guide](#quick-start-guide)
2. [Using in Chat Windows](#using-in-chat-windows)
3. [Platform Integration](#platform-integration)
4. [API Integration](#api-integration)
5. [Advanced Features](#advanced-features)
6. [Troubleshooting](#troubleshooting)

---

## Quick Start Guide

### What This System Does
The Expert Prompt Engineer System evaluates and optimizes prompts across six key dimensions:
- **Agent Directives**: Systematic problem-solving capabilities
- **Anti-Hallucination**: Fact verification and accuracy controls
- **Security Assessment**: Prompt injection and vulnerability protection
- **Output Formatting**: Structured JSON responses with alternatives
- **Performance Optimization**: Accuracy-first vs. cost-efficient approaches
- **Advanced Techniques**: Few-shot learning, chain-of-thought reasoning

### Basic Usage (30 seconds)
1. **Paste your prompt** after the system prompt
2. **Add context** like: "This is for creative writing" or "Prioritize cost efficiency"
3. **Receive evaluation** with ratings (1-100) and specific improvements
4. **Get enhanced version** with integrated frameworks automatically included

### Example Quick Request
```
Review this prompt: "Write a marketing email for our new product."
```

**You'll get:**
- Quality rating with specific issues identified
- Enhanced version with agent directives and security protections
- JSON output format recommendations
- Implementation guidance for your specific use case

---

## Using in Chat Windows

### Direct Implementation
**For Claude (this system):**
```
1. Start new conversation
2. Paste the complete prompt system JSON
3. Begin with: "Review this prompt: [your prompt here]"
4. Add context: "This is for [use case] with [priority: accuracy/cost]"
```

### Conversation Flow
```
User: "Review this prompt: Create a chatbot for customer service"

System Response Includes:
├── Deep Analysis Summary
├── Agent Directive Integration Assessment  
├── Security & Robustness Assessment
├── Quality Rating (1-100)
├── Optimization Suggestions
└── Enhanced Prompt with All Frameworks
```

### Follow-up Options
- **"Make it more cost-efficient"** → Switches to cost-optimization mode
- **"Add more security"** → Enhanced security framework implementation
- **"Simplify for beginners"** → Removes advanced features
- **"Show me the API version"** → Provides API-compatible format

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

**For Multiple Prompt Evaluation:**
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
```

---

## Advanced Features

### Adding/Removing Agent & Anti-Hallucination Features

#### **Agent Directives Customization**

**Full Integration (Default):**
```json
{
  "agent_directives": {
    "persistence": "Continue until query completely resolved",
    "tool_usage": "Verify information rather than guessing", 
    "deliberate_planning": "Plan extensively before function calls"
  }
}
```

**Custom Adaptation Examples:**
```python
# For Creative Writing
creative_directives = {
    "persistence": "Continue until story elements are consistent and complete",
    "tool_usage": "Research historical/cultural accuracy for world-building",
    "deliberate_planning": "Plan character arcs and plot development systematically"
}

# For Data Analysis  
analytical_directives = {
    "persistence": "Continue until all calculations are verified and validated",
    "tool_usage": "Verify data sources and validate statistical methods",
    "deliberate_planning": "Plan analysis methodology before processing data"
}
```

**Removing Agent Features:**
Add to your request: `"Exclude agent directives - basic prompt only"`

#### **Anti-Hallucination Framework Control**

**Standard Implementation:**
- Separates real-world facts from fictional content
- Uses `[RESEARCH_NEEDED]` for uncertain information
- Applies fact sensitivity levels (high/moderate/flexible)

**Custom Sensitivity Levels:**
```python
# High-Accuracy Mode (Medical/Legal/Financial)
high_accuracy_config = {
    "fact_threshold": "verify_all_claims",
    "uncertainty_handling": "explicit_confidence_scores",
    "source_requirements": "peer_reviewed_only"
}

# Creative Mode (Fiction/Marketing)
creative_config = {
    "fact_threshold": "basic_plausibility", 
    "uncertainty_handling": "creative_liberties_allowed",
    "fictional_consistency": "internal_logic_only"
}
```

**Disabling Anti-Hallucination:**
Add: `"Creative prompt - allow fictional elements without fact-checking"`

### Security Considerations

#### **Security Assessment Levels**

**Level 1 - Basic Protection:**
- Input validation for obvious injection attempts
- Role boundary enforcement
- Basic output monitoring

**Level 2 - Enhanced Security (Default):**
- Multi-layered filtering (keyword + semantic)
- Instruction hierarchy enforcement
- Comprehensive test case validation

**Level 3 - Maximum Security:**
- Fine-tuned injection-resistant models
- Real-time output analysis
- Advanced threat pattern recognition

#### **Custom Security Implementation:**

**High-Risk Applications (Banking, Healthcare):**
```python
max_security_config = {
    "input_validation": "comprehensive_sanitization",
    "output_monitoring": "real_time_analysis",
    "injection_resistance": "fine_tuned_models",
    "audit_logging": "complete_interaction_logs",
    "escalation_triggers": "human_review_required"
}
```

**Low-Risk Applications (Creative, Educational):**
```python
basic_security_config = {
    "input_validation": "basic_filtering",
    "output_monitoring": "periodic_sampling", 
    "injection_resistance": "standard_prompting",
    "audit_logging": "summary_only"
}
```

### Output Formatting

#### **JSON Format System (Default)**

**Standard Structure:**
```json
{
  "analysis": {
    "task_clarification": "string",
    "quality_rating": "integer (1-100)",
    "optimization_mode": "accuracy_first|cost_first|balanced"
  },
  "evaluation": {
    "agent_directive_assessment": "string",
    "security_assessment": "string", 
    "format_recommendation": "string"
  },
  "recommendations": {
    "enhanced_prompt": "string",
    "implementation_notes": ["array of strings"],
    "integration_guidance": "string"
  }
}
```

**Custom JSON Schemas:**
```python
# For API Integration
api_schema = {
    "evaluation_summary": "string",
    "quality_score": "number",
    "improvements": ["array"],
    "enhanced_version": "string",
    "api_compatible": "boolean"
}

# For Documentation
documentation_schema = {
    "title": "string",
    "description": "string", 
    "usage_examples": ["array"],
    "parameters": {"object"},
    "expected_outputs": {"object"}
}
```

#### **Alternative Formats**

**XML for Enterprise Systems:**
Request: `"Output as XML for enterprise integration"`
```xml
<prompt_evaluation>
    <analysis quality_rating="85" mode="accuracy_first"/>
    <security_assessment level="enhanced"/>
    <recommendations>
        <enhanced_prompt>[Enhanced version]</enhanced_prompt>
        <integration_notes>[Implementation guidance]</integration_notes>
    </recommendations>
</prompt_evaluation>
```

**Markdown for Documentation:**
Request: `"Output as Markdown for team documentation"`

### Accuracy vs Cost Considerations

#### **Accuracy-First Mode (Default)**

**Characteristics:**
- Comprehensive validation steps
- Lower temperature settings (0.0-0.3)
- Generous context allocation (40-50% for responses)
- Redundant critical instructions
- Multiple examples and edge cases

**Best For:**
- Medical, legal, financial applications
- Educational content
- Critical business decisions
- Safety-sensitive systems

**Token Investment Philosophy:**
"Invest tokens strategically for maximum reliability and precision"

#### **Cost-First Mode**

**Activation:** Add `"Prioritize cost efficiency"` or `"Optimize for token usage"`

**Characteristics:**
- Streamlined instructions
- Higher temperature settings (0.4-0.7)
- Efficient context allocation (20-30% for responses)
- Concise examples
- Eliminated redundancy

**Best For:**
- High-volume applications
- Simple task automation
- Prototype development
- Budget-constrained projects

**Example Comparison:**
```python
# Accuracy-First (47 tokens)
accuracy_prompt = """
Extract financial metrics from this document. Focus specifically on: 
1) Revenue figures with exact amounts, 2) Profit margins with percentages, 
3) Growth rates with time periods. If data is unclear, state 'Data not available' 
rather than estimating. Validate all calculations before responding.
"""

# Cost-First (12 tokens)  
cost_prompt = "Extract revenue, profit margins, and growth rates from this document."

# Trade-off: 292% token increase for significantly higher accuracy and reliability
```

#### **Balanced Mode**

**Activation:** Request `"Balanced optimization"` or `"Show both approaches"`

**Provides:**
- Both accuracy-first and cost-first versions
- Clear trade-off analysis
- Token cost estimates
- Accuracy impact assessment
- Use case recommendations

### Different Prompt Types

#### **Creative Writing Prompts**

**Specialized Features:**
- Character consistency tracking
- World-building accuracy verification  
- Genre convention adherence
- Narrative flow optimization

**Example Optimization:**
```
Original: "Write a story"
Enhanced: "Write a 1500-word science fiction story set in 2150 about AI consciousness, 
targeting adult readers. Include: protagonist with clear motivation, central conflict 
around AI rights, resolution that explores themes of identity and consciousness. 
Agent directives ensure character consistency. Anti-hallucination framework verifies 
scientific plausibility. JSON output with story elements tracking."
```

#### **Data Analysis Prompts**

**Specialized Features:**
- Statistical methodology validation
- Calculation accuracy verification
- Data source credibility assessment
- Visualization recommendations

**Security Considerations:**
- Data injection prevention
- Result manipulation protection
- Source validation requirements

#### **Code Generation Prompts**

**Specialized Features:**
- Syntax perfection requirements
- Security vulnerability scanning
- Documentation completeness
- Testing framework integration

**Enhanced Security:**
- Malicious code prevention
- Injection attack resistance
- Access control validation

#### **Conversational AI Prompts**

**Specialized Features:**
- Context retention optimization
- Personality consistency
- Response appropriateness
- Fact verification protocols

**High Vulnerability Assessment:**
- Social engineering resistance
- Information extraction protection
- Role confusion prevention

#### **Educational Content Prompts**

**Specialized Features:**
- Subject matter accuracy
- Age-appropriate language
- Learning objective alignment
- Assessment integration

**Accuracy Critical:**
- Fact verification mandatory
- Source citation requirements
- Pedagogical soundness

#### **Business Analysis Prompts**

**Specialized Features:**
- Market data accuracy
- Competitive intelligence protection
- Strategic recommendation validation
- Risk assessment completeness

**Enterprise Security:**
- Confidential information protection
- Data source validation
- Strategic insight verification

---

## Troubleshooting

### Common Issues

**Issue:** "System doesn't apply agent directives"
**Solution:** Check that request doesn't include exclusion phrases like "basic prompt only"

**Issue:** "Too verbose/expensive responses"  
**Solution:** Add "prioritize cost efficiency" to switch optimization modes

**Issue:** "Security warnings for benign prompts"
**Solution:** Context matters - specify use case like "for educational purposes only"

**Issue:** "Not outputting JSON format"
**Solution:** Explicitly request "output as JSON" if system doesn't default correctly

### Support and Updates

**Documentation Version:** 2.1.0
**Last Updated:** Based on prompt system version 2.1.0
**Compatibility:** Claude Sonnet 4, GPT-4, Gemini Pro
**Support:** Reference this documentation for implementation guidance

### Best Practices Summary

1. **Always specify context** - "This is for [use case]"
2. **Choose optimization mode explicitly** - Accuracy-first vs cost-first
3. **Request appropriate security level** - Based on application risk
4. **Specify output format needs** - JSON, XML, Markdown
5. **Test with representative examples** - Before production deployment
6. **Monitor performance metrics** - Quality scores and token usage
7. **Iterate based on results** - Use feedback to refine prompts

---

*This documentation covers the complete Expert Prompt Engineer System. For additional support or custom implementations, reference the specific integration examples and API configurations provided above.*