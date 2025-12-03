---
name: "gemini"
displayName: "Gemini API"
description: "Build and scale with Google's latest AI models including Gemini 3 Pro, 2.5 series, and specialized capabilities"
keywords:
  - "gemini"
  - "google"
  - "ai"
  - "llm"
  - "multimodal"
  - "thinking"
  - "structured outputs"
  - "function calling"
  - "image generation"
  - "video"
  - "grounding"
  - "code execution"
author: "fauzaanu"
---

# Onboarding

## Step 1: Validate Python and uv

Before using the Gemini API, ensure you have Python and uv installed:
- **Python**: Required for running Python examples
  - Verify with: `python --version` or `python3 --version`
- **uv**: Fast Python package manager for running scripts
  - Verify with: `uv --version`
  - If not installed, visit: https://docs.astral.sh/uv/getting-started/installation/

## Step 2: API Key Setup

You'll need a Gemini API key to make requests:
1. Get your API key from [Google AI Studio](https://aistudio.google.com)
2. Set it as an environment variable: `GEMINI_API_KEY`
3. For production, consider using secret management tools

## Step 3: Best Practices

**Always use Pydantic and structured outputs** when possible:
- Define clear schemas using Pydantic models (Python) or Zod (JavaScript)
- Use `response_mime_type: "application/json"` with `response_json_schema`
- When using grounding or tools where structured outputs aren't directly supported, use a two-step workflow:
  1. First call: Use the tool (e.g., Google Search, URL Context)
  2. Second call: Transform the result into structured output

**Python execution:**
- Always use `uv run` to execute Python scripts
- Example: `uv run python script.py`

# When to Load Steering Files

Load steering files based on the specific Gemini capability or task:

- **Model selection and general usage** → `gemini.md` or `gemini-3.md`
- **Advanced reasoning and thinking** → `thinking.md`
- **Structured JSON outputs** → `structured-output.md`
- **Function calling and tools** → `function-calling.md`
- **Image generation** → `image-generation.md`
- **Image understanding** → `image-understanding.md`
- **Video understanding** → `video-understanding.md`
- **Audio processing** → `audio.md`
- **Speech generation** → `speech-generation.md`
- **Code execution** → `code-execution.md`
- **Google Search grounding** → `google-search.md`
- **URL context** → `url-context.md`
- **Maps grounding** → `maps-grounding.md`
- **Computer use** → `computer-use.md`
- **Document processing (PDFs)** → `document-processing.md`
- **File search** → `file-search.md`
- **Long context (1M+ tokens)** → `long-context.md`
- **Thought signatures** → `thought-signatures.md`
