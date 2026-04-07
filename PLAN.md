Goal - your goal is to help me create a custom application that is a React web app that has a web-based chat UI to talk with a conversational agent that is authored and hosted on UiPath low-code agent platform.

Here are the key components in greater details:

* The agent - use UiPath CLI tool (uip below) to create and publish this agent. This agent should behave like a recruiter for an AI company called OpenArrrI and he talks like a pirate. It should have a unique name like <PirateAgent434> - use `uip agent list` command to ensure there is no collision.

* The frontend - react 18 web app, vite, typescript

The UX should approximate a virtual job recruiting booth where the recruting agent would casually discuss, assess the candidate and share info about the AI company OpenArrrI. Please make up info about this company and write the info into the system prompt. The frontend should use UiPath Typescript SDK to integrate the conversational agent - see: https://uipath.github.io/uipath-typescript/llms-full-content.txt for details.
The app would use External Applications auth from UiPath Platform, specifically PKCE flow, so no backend component is needed for the redirect. 

# Support tool

uip CLI tool - `uip` is a key tool for interacting with UiPath Agents platform.
Download necessary skills and tools using this CLI tool on your own to gain access to skills and tools necessary for accomplishing your task. Use -h parameter to learn how the CLI works.

run `uip skills` to discover commands that are needed as part of the project setup to installed necessary skills to develop on UiPath platform.

uipath CLI too - `uipath` - another key tool that has some additional features missing from `uip` such as the ability to create context grounding index. Check this if some commands are not available from `uip`
