# UiPath Agentic Coding Demo

This demo shows that UiPath Agentic Platform is Coding Agent ready. Clone this repo and launch Claude Code from the repo root.
Ask Claude Code to `execute PLAN.md` and follow any prompt for info, and the coding agent would help produce a simple but meaningful agentic application.

## Do these before you clone the repo
- install `uipath` CLI, run `pip install uipath`
- clone https://github.com/UiPath/cli and build `uip` CLI locally
- create an External Applications entry in your Automation Cloud org. Create as "Non-Confidential application", with scope:
  - UiPath.Orchestrator: OR.Execution OR.Folders OR.Jobs OR.Users
  - Traces.Api: Traces.Api
  - ConversationalAgents: ConversationalAgents
- redirect URL: http://localhost:5173 for dev server (the coding agent should use `window.location.href.split('?')[0].split('#')[0].replace(/\/$/, '')` to derive the redirect URL. If you later deploy to Coded App, you would need to add the corresponding Coded APP URL to the redirect URL. Coding agent should be able to tell you what is the redirect URL to add to your config. (you can have many valid redirect URLs for each external application entry).

## PLAN.md
Take a look to understand the scenario that we will be building. We will show building a simple but meaningful agent-powered application.

## CLAUDE.md
Contains instructions helpful for first time success for building agent powered UiPath apps using coding agent. 

