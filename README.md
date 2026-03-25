# Market Research Crew

A multi-agent AI system for conducting comprehensive market research using [crewAI](https://crewai.com). This project orchestrates specialized AI agents to research markets, analyze trends, and generate detailed market research reports.

## Overview

MarketResearchCrew leverages a team of AI agents working collaboratively to:
- **Research** market trends and competitive landscapes
- **Analyze** industry data and market opportunities
- **Generate** comprehensive market research reports in markdown format

Each agent has a specialized role and set of tools to perform their tasks efficiently.

## Prerequisites

- Python >=3.10 <3.14
- OpenAI API key (set in `.env`)
- [UV](https://docs.astral.sh/uv/) for dependency management

## Installation

1. Install UV (if not already installed):
```bash
pip install uv
```

2. Install project dependencies:
```bash
crewai install
```

3. Configure your environment:
   - Create a `.env` file in the project root
   - Add your OpenAI API key:
     ```
     OPENAI_API_KEY=your_key_here
     ```

## Project Structure

```
market_research_crew/
├── src/market_research_crew/
│   ├── config/
│   │   ├── agents.yaml          # Agent definitions and configurations
│   │   └── tasks.yaml           # Task definitions and workflows
│   ├── tools/
│   │   └── custom_tool.py       # Custom tools for agents
│   ├── crew.py                  # Crew orchestration logic
│   ├── main.py                  # Entry point
│   └── __init__.py
├── knowledge/
│   └── user_preference.txt      # Knowledge base for domain context
├── reports/
│   └── report.md                # Generated research reports
├── tests/                       # Test suite
├── pyproject.toml               # Project dependencies
├── AGENTS.md                    # CrewAI reference documentation
└── README.md                    # This file
```

## Usage

### Running the Crew

Execute the market research crew from the project root:

```bash
crewai run
```

This will:
1. Initialize all configured agents
2. Execute research and analysis tasks
3. Generate a comprehensive report in `reports/report.md`

### Customizing

#### Agents Configuration
Edit `src/market_research_crew/config/agents.yaml` to:
- Define agent roles and goals
- Configure backstories and expertise
- Assign tools to specific agents

#### Tasks Configuration
Edit `src/market_research_crew/config/tasks.yaml` to:
- Define research objectives
- Set expected outputs
- Configure task dependencies

#### Custom Logic
Modify `src/market_research_crew/crew.py` to:
- Add custom agent initialization
- Configure processing strategies
- Implement specialized workflows

#### Input Parameters
Edit `src/market_research_crew/main.py` to:
- Set research topics
- Configure input parameters
- Customize report generation

## Configuration

### Setting Up OpenAI API Key

Create a `.env` file in the project root:
```
OPENAI_API_KEY=sk-your-api-key-here
```

### Knowledge Base

Add domain knowledge and preferences in `knowledge/user_preference.txt` to help agents stay aligned with your research goals and constraints.

## Output

The crew generates research outputs to `reports/report.md` containing:
- Market analysis and trends
- Competitive landscape insights
- Key findings and recommendations
- Sources and data references

## Development

### Running Tests

```bash
crewai test
```

Run crew performance tests to ensure quality across iterations.

### Debugging

Enable verbose output in crew execution to see detailed agent interactions:

Enable `verbose: true` in agent configurations within `config/agents.yaml`.

## Troubleshooting

**Import errors or missing packages:**
```bash
crewai install
```

**API Key issues:**
- Verify `OPENAI_API_KEY` is set in `.env`
- Check your OpenAI account has available credits

**Execution timeouts:**
- Increase task timeouts in `config/tasks.yaml`
- Split large research tasks into smaller subtasks

## Resources

- [CrewAI Documentation](https://docs.crewai.com)
- [CrewAI GitHub Repository](https://github.com/joaomdmoura/crewai)
- [OpenAI API Documentation](https://platform.openai.com/docs)

## Support

For issues or questions:
1. Check the [CrewAI docs](https://docs.crewai.com)
2. Review the `AGENTS.md` file for CrewAI patterns and best practices
3. Submit issues to the [CrewAI repository](https://github.com/joaomdmoura/crewai)
- [Join our Discord](https://discord.com/invite/X4JWnZnxPb)
- [Chat with our docs](https://chatg.pt/DWjSBZn)

Let's create wonders together with the power and simplicity of crewAI.
