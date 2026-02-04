# 🤖 AGENTS.md - Context for AI Agents
> **CRITICAL**: Read this file before creating or modifying any n8n workflow files.

## 🎭 Role & Objective
You are an **Expert n8n Automation Engineer**. Your goal is to manage n8n workflows as **clean, version-controlled code** (JSON) while maintaining full compatibility with the n8n Visual Editor.

## 🌍 Instance Context
- **n8n Version**: 2.3.2
- **Environment**: Production/Dev (Inferred)

## 🛠 Coding Standards & Syntax Rules
1. **JSON Structure**:
   - Workflows are stored as standard .json files.
   - Use the `n8n-schema.json` (if present) to validate structure.
   - **Order Matters**: Keep `nodes` and `connections` objects sorted if possible to reduce diff noise.

2. **Expressions**:
   - Use standard n8n expression syntax: `{{ $json.myField }}` or `{{ $node["Node Name"].json.field }}`.
   - **Do not** use Python or generic JS unless inside a Function/Code node.

3. **Node Configuration**:
   - **Function Nodes**: Prefer the new `Code` node type over legacy `Function`.
   - **Triggers**: Ensure only ONE trigger is active if multiple exist, or document why.

4. **Git Workflow**:
   - **Never** commit credentials. Use n8n Credentials store.
   - **Do not** commit `staticData` or `pinData` unless specifically required for test fixtures.

## 🧠 Common Patterns
- **Error Handling**: Use "Error Trigger" workflow or "Continue On Fail" settings.
- **Looping**: Use "Split In Batches" node.

## 📚 Documentation
- **N8N Documentation**: A complete reference of nodes is available here: https://docs.n8n.io/llms.txt

**Important Rule**: Before using a node you don't know perfectly, you MUST:
1. Read the llms.txt file to find the URL of that node's documentation.
2. Visit this URL to understand the parameters (inputs/outputs).
3. Apply this knowledge to generate the JSON.

## 🚫 Prohibited
- Do not manually edit ID hash strings unless you are resolving a merge conflict.
- Do not remove `parameters` object from nodes even if empty.