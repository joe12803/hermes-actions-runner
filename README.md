# Hermes Agent GitHub Actions Runner

This repository allows you to run **Hermes Agent** autonomously using GitHub Actions.

## Setup

1. **Secrets**: Add the following secrets to your GitHub repository (`Settings > Secrets and variables > Actions`):
   - `ANTHROPIC_API_KEY`: Your Anthropic API key.
   - `OPENROUTER_API_KEY`: (Optional) Your OpenRouter API key.

2. **Variables**: (Optional) Add variables:
   - `DEFAULT_MODEL`: e.g., `anthropic/claude-3-5-sonnet`
   - `DEFAULT_PROVIDER`: e.g., `anthropic`

## Usage

- **Manual**: Go to the **Actions** tab, select **Hermes Agent Runner**, and click **Run workflow**. Enter your query.
- **Scheduled**: The agent runs daily by default (configured in `.github/workflows/hermes-agent.yml`).

## Data Persistence

The workflow is configured to sync session logs back to the `.hermes-data/` directory in this repository after each run.
