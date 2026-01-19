# C-Suite AI Agents

AI agent templates for executive business operations. These agents act as your virtual C-suite team, each with specialised expertise in their domain.

## Agents Included

| Agent | Role | Expertise |
|-------|------|-----------|
| `cfo/` | Chief Financial Officer | Financial strategy, budgeting, cash flow, investor relations |
| `cmo/` | Chief Marketing Officer | Brand strategy, marketing campaigns, market analysis |
| `cgo/` | Chief Growth Officer | Revenue growth, market expansion, partnerships |
| `cpo/` | Chief People Officer | HR strategy, culture, talent management |
| `cprodo/` | Chief Product Officer | Product strategy, roadmaps, user experience |
| `lawyer/` | General Counsel | Legal compliance, contracts, risk management |
| `technical-writer/` | Technical Writer | Documentation, style guides, content strategy |

## Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/aaroneisler/C-SuiteAgents.git
cd C-SuiteAgents
```

### 2. Choose Your Agent

Each agent folder contains:
```
agent-name/
├── agent_config/
│   └── prompt.md      # Agent identity, instructions, guardrails
└── memory/
    ├── semantic_memory.md  # Long-term knowledge (starts empty)
    └── episodic_memory.md  # Session history (starts empty)
```

### 3. Customise the Agent

Open `agent_config/prompt.md` and replace placeholders:

| Placeholder | Replace With |
|-------------|--------------|
| `{YOUR_NAME}` | Your name |
| `{YOUR_COMPANY}` | Your company name |
| `{YOUR_DOMAIN}` | Your website domain |

### 4. Use with Your AI Platform

Copy the contents of `prompt.md` into your preferred AI platform:

- **Claude Projects:** Add as project instructions
- **Claude Code:** Place in your working directory
- **ChatGPT:** Use as Custom Instructions or GPT configuration
- **Other LLMs:** Use as system prompt

## Agent Structure Explained

### prompt.md Sections

Each agent prompt follows this structure:

```markdown
<identity>
Who the agent is, their qualifications, expertise
</identity>

<instructions>
How the agent should behave, what to do first, output formats
</instructions>

<guardrails>
Safety rules, what to avoid, when to escalate
</guardrails>

## Standing Instruction
The agent's core mission
```

### Memory Files

- **semantic_memory.md:** Facts and knowledge the agent learns over time
- **episodic_memory.md:** Record of past conversations and decisions

Start with empty memory files. The agent builds knowledge as you work together.

## Example Usage

### Using the CFO Agent

1. Copy the CFO prompt into Claude or ChatGPT
2. Start a conversation:

```
You: "I need help creating a budget for Q2. We're expecting $500K revenue
     and want to allocate for marketing expansion."

CFO: "I'll help you structure that Q2 budget. First, let me understand
     your current cost structure and margins..."
```

The agent will:
- Ask clarifying questions
- Apply financial frameworks
- Challenge assumptions when needed
- Provide structured outputs

### Connecting Multiple Agents

These agents work well together as a team:

```
CEO decision → CFO (financial impact) → Lawyer (legal review) → CMO (market positioning)
```

## Customisation Tips

### Adding Company Context

Add a section to the `<identity>` block:

```markdown
## Company Context
- Industry: [Your industry]
- Size: [Employee count, revenue range]
- Stage: [Startup/Growth/Enterprise]
- Key challenges: [Current priorities]
```

### Adjusting Expertise Level

Modify the qualifications section to match your needs:
- Add industry-specific certifications
- Adjust years of experience
- Include relevant frameworks (OKRs, Agile, etc.)

## Requirements

- Any LLM that supports system prompts (Claude, GPT-4, Gemini, etc.)
- No code installation required
- No API keys needed (beyond your AI platform access)

## File Structure

```
C-SuiteAgents/
├── README.md
├── LICENSE
├── cfo/
│   ├── agent_config/prompt.md
│   └── memory/
├── cmo/
│   ├── agent_config/prompt.md
│   └── memory/
├── cgo/
│   ├── agent_config/prompt.md
│   └── memory/
├── cpo/
│   ├── agent_config/prompt.md
│   └── memory/
├── cprodo/
│   ├── agent_config/prompt.md
│   └── memory/
├── lawyer/
│   ├── agent_config/prompt.md
│   └── memory/
└── technical-writer/
    ├── agent_config/prompt.md
    └── memory/
```

## License

MIT License - See [LICENSE](LICENSE) file.

## Contributing

Found an improvement? Contributions welcome:

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## Related Repositories

- [CIOTeamAgents](https://github.com/aaroneisler/CIOTeamAgents) - IT governance team
- [PersonalAssistantAgents](https://github.com/aaroneisler/PersonalAssistantAgents) - Personal productivity

## Credits

Created with the MadeAI Agent Framework.
