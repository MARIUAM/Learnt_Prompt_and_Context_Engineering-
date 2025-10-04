

# Title
content.append(Paragraph("<b>7-Day Study Plan for Prompt & Context Engineering Exam</b>", styles["Heading"]))
content.append(Spacer(1, 12))

# Intro
intro_text = """
This study plan is designed to cover all 13 key topics of the syllabus within 7 days, 
ensuring a balanced daily commitment of 7 hours. Each day is structured with clear focus 
areas, official resources, and preparation activities to build conceptual understanding 
and practical application skills.
"""
content.append(Paragraph(intro_text, styles["NormalText"]))
content.append(Spacer(1, 12))

# Day-wise plan with topics and links
plan = [
    ("Day 1: Fundamentals & Basics", [
        ("Introduction to Prompt Engineering", "https://platform.openai.com/docs/guides/prompt-engineering"),
        ("Types of Prompts", "https://learnprompting.org/docs/basics/prompt_types"),
        ("Context Windows", "https://platform.openai.com/docs/guides/gpt"),
    ]),
    ("Day 2: Structuring Prompts", [
        ("Zero-shot & Few-shot Learning", "https://learnprompting.org/docs/basics/few_shot"),
        ("Role of Instructions", "https://www.promptingguide.ai/techniques"),
        ("Effective Prompt Formatting", "https://www.promptingguide.ai/techniques"),
    ]),
    ("Day 3: Advanced Prompting Techniques", [
        ("Chain of Thought (CoT)", "https://www.promptingguide.ai/techniques/cot"),
        ("Self-Consistency", "https://www.promptingguide.ai/techniques/self_consistency"),
        ("Tree of Thoughts", "https://arxiv.org/abs/2305.10601"),
    ]),
    ("Day 4: Context Engineering", [
        ("Context Injection", "https://platform.openai.com/docs/guides/context"),
        ("Memory & Retrieval-Augmented Generation (RAG)", "https://python.langchain.com/docs/use_cases/question_answering/"),
        ("Knowledge Bases", "https://docs.trychroma.com/"),
    ]),
    ("Day 5: Tools & Frameworks", [
        ("LangChain", "https://python.langchain.com/docs/get_started/introduction"),
        ("LlamaIndex", "https://docs.llamaindex.ai/en/stable/"),
        ("Vector Databases", "https://weaviate.io/developers/weaviate"),
    ]),
    ("Day 6: Applications", [
        ("Building Chatbots", "https://platform.openai.com/docs/guides/gpt"),
        ("Summarization & Q/A Systems", "https://python.langchain.com/docs/use_cases/summarization"),
        ("Agentic Workflows", "https://docs.anthropic.com/claude/docs/agentic-design-patterns"),
    ]),
    ("Day 7: Mock Test & Revision", [
        ("Full Mock Exam (Self Practice)", "https://learnprompting.org/"),
        ("Review Weak Topics", "https://www.promptingguide.ai/"),
        ("Final Day Recap & Strategy", "https://platform.openai.com/docs/introduction"),
    ]),
]

for day, topics in plan:
    content.append(Paragraph(f"<b>{day}</b>", styles["SubHeading"]))
    for topic, link in topics:
        content.append(Paragraph(f"• {topic} — <font color='blue'><u>{link}</u></font>", styles["NormalText"]))
    content.append(Spacer(1, 8))

# Mock Test Section
mock_text = """
<b>Mock Test Plan:</b><br/>
On Day 7, attempt a full-length mock test using resources from Learn Prompting and Prompting Guide. 
Allocate 3 hours to simulate the exam environment and use the remaining 4 hours for revision of weak areas.
"""
content.append(Paragraph(mock_text, styles["NormalText"]))

# Risks Section
risks_text = """
<b>Risks & Mitigation:</b><br/>
1. <b>Time Overload</b> — Stick to 7-hour daily limit and avoid burnout.<br/>
2. <b>Concept Gaps</b> — Revisit official resources and guides for clarification.<br/>
3. <b>Lack of Practice</b> — Ensure daily hands-on exercises after theory.<br/>
"""

