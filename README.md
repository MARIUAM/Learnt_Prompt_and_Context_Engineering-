

# Title
story.append(Paragraph("Prompt and Context Engineering — Full Syllabus & Study Guide", styles['Title']))
story.append(Spacer(1, 8))

# Intro & Links
intro = """
The foundation course for Agentic AI program covering Prompt and Context Engineering is complete.
Below are class recordings, learning material links, exam details, full syllabus (expanded) and study tips.
"""
story.append(Paragraph(intro, styles['Normal']))
story.append(Spacer(1, 6))

links = """
Class Recording Playlist:
https://www.youtube.com/playlist?list=PL0vKVrkG4hWpeKmZyCRTpfRiLQ13b5uRX

Detailed Learning Material:
https://github.com/panaversity/learn-low-code-agentic-ai/tree/main/00_prompt_engineering

Recommended study materials (exam references):
- https://github.com/panaversity/learn-n8n-agentic-ai/blob/main/00_prompt_engineering/readme.md
- https://github.com/panaversity/learn-low-code-agentic-ai/blob/main/00_prompt_engineering/six_part_prompting_framework.md
- https://github.com/panaversity/learn-n8n-agentic-ai/blob/main/00_prompt_engineering/context_engineering_tutorial.md
- https://github.com/panaversity/learn-low-code-agentic-ai/blob/main/00_prompt_engineering/image_generation/readme.md
"""
story.append(Paragraph(links, styles['Normal']))
story.append(Spacer(1, 10))

# Exam details
exam = """
Exam Details:
- Prompt and Context Engineering: Effective AI Communication
- Level 1 Certification Exam (L1:P0-PTE)
- Total Questions: 150
- Duration: 2 hours 45 minutes (165 minutes)
- Difficulty: Beginner level
"""
story.append(Paragraph(exam, styles['Heading2']))
story.append(Spacer(1, 8))

# Key Topics headings and details
sections = [
    ("1. Fundamentals", 
     "Primary goals and differences between prompt engineering (crafting instructions for desired outputs) and context engineering (providing relevant facts/documents for grounding). "
     "How LLMs work (prediction engines guessing next tokens, not human-like understanding). Common failure modes (e.g., hallucinations from missing info, messy outputs from vague instructions). "
     "Recommended workflows (prompt first, then ground with context; feeding tool outputs back in agentic flows). Viewing LLMs as sophisticated autocomplete systems."),
    
    ("2. Configuration", 
     "Settings: temperature (controls randomness/creativity), top-K (limits to top likely tokens), top-P (nucleus sampling threshold), output/token limits (length & cost). "
     "Starting config strategies (conservative, balanced, creative). Appropriate uses (temp 0 for math/consistency, higher for creative writing)."),
    
    ("3. Prompting Techniques",
     "Basic techniques: zero-shot, one-shot, few-shot (3–5 examples). Advanced techniques: role prompting (assign persona), system prompting (behavior rules), Chain-of-Thought (CoT), Self-Consistency (multiple reasoning paths), Step-Back, ReAct (reasoning + tool actions), Tree-of-Thoughts (ToT). "
     "Practical tips like combining 'Let's think step by step' with low temperature for reliable CoT outputs."),
    
    ("4. Best Practices & Pitfalls", 
     "Best practices: use specific/action verbs, positive instructions, structured formats (JSON), variables for reusability, break complex tasks into chains, feed prior context, optimize token use. "
     "Pitfalls: vague/ambiguous instructions, constraint overload, negative-only constraints, over-reliance on tools without reasoning, excessive details that confuse models. Examples of strong vs weak prompts for various tasks."),
    
    ("5. Testing and Evaluation", 
     "Record prompt versions, goals, settings, and quality notes. Use A/B testing to compare prompt variants. Metrics: accuracy, relevance, completeness, style, format, and consistency across runs."),
    
    ("6. Advanced Techniques and Tips", 
     "Context management in long conversations (summarize past, chunk tasks). Prompt chaining (sequential steps), structured outputs (JSON) for downstream parsing, and multi-modal prompting (explicit image/text details)."),
    
    ("7. Mixture-of-Experts (MoE) & Prompting", 
     "MoE basics: gating/router chooses experts (sparse activation). Impact on prompting: front-load domain signals, split mixed tasks, lower temperature for consistent expert outputs. Tradeoffs: efficiency & specialization vs routing instability and memory overhead."),
    
    ("8. Practical Application", 
     "Effective prompt elements for content creation (topic, audience, tone, format), code generation (language, requirements, examples), and customer feedback analysis (sentiment, themes, recommendations)."),
    
    ("9. Context Engineering Integration", 
     "RAG (Retrieval-Augmented Generation): prioritize relevance and recency, chunking, ranking, deduping, and token budget optimization. Combine prompts for behavior with context for knowledge; design ranking and retrieval pipelines."),
    
    ("10. Comprehensive/Applied Scenarios", 
     "Consolidated examples: optimized prompts for reports, Q&A bots, story generation, and addressing MoE-related pitfalls (front-loading, low temperature). Realistic applied scenarios to test prompt + context + tools."),
    
    ("11. Context Engineering (Deep)", 
     "LLM as CPU, context window as RAM. Differences from prompt engineering: context engineering is broader and more code-like for building agents. Agent components: model, tools, memory, knowledge base, orchestration, guardrails, audio/speech. "
     "Multi-agent systems, context selection/compression/ isolation strategies, hierarchical summarization, optimization for accuracy/latency/cost, security/isolation, memory hierarchies, temporal reasoning, and enterprise trade-offs."),
    
    ("12. 6-Step Framework", 
     "Strong command verbs (analyze, summarize), rule of three for context (who/what/when), logic for reasoning + output format, roleplay to specify expertise, iterative questioning for refinement, and voice memos for natural follow-ups. When to use minimal vs extensive context."),
    
    ("13. AI Image Generation Prompting (Nano Banana)", 
     "Principles: specificity > generality, visual hierarchy (subject → environment → lighting → technical), professional photography language (lens, aperture, lighting), and the 7-component image prompt structure: Subject, Pose, Environment, Lighting, Style, Technical specs, Mood. "
     "Best practices: anchor to 'uploaded photo', control scene with environment cues, use photography terms for realism, add branding. Common mistakes & quality-control checklist included."),
    
    ("Study Tips & Practice", 
     "Hands-on testing with free tools (Grok, ChatGPT, Google Gemini), master key distinctions (prompt vs context, top-K vs top-P, MoE routing), analyze examples of success/failure, practice frameworks (image 7-component & 6-step text framework), build templates, integrate RAG and agents, and do systematic quality checks. "
     "Advanced prep: combine CoT with image/multi-expert setups, read transformer basics, RAG & MoE papers, and practice on prompt engineering platforms." )
]

for title, body in sections:
    story.append(Paragraph(title, styles['Heading2']))
    story.append(Spacer(1, 4))
    story.append(Paragraph(body, styles['Normal']))
    story.append(Spacer(1, 8))

# Final pagebreak and footer note
story.append(PageBreak())
footer = "Generated study guide — customize it, create practice prompts, and convert sections into flashcards and timed mocks.\nGood luck!"
story.append(Paragraph(footer, styles['Normal']))

doc.build(story)
pdf_path
___________________________________________________________________________________________________________________________________________________________


