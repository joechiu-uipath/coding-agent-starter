# Agent-powered web app demo

## Goal
Your goal is to help me create a custom application that is a React web app that has a web-based chat UI to talk with a conversational agent that is authored and hosted on UiPath low-code agent platform.

Here are the key components in greater details:

## The conversational agent
Use UiPath CLI tool (uip below) to create and publish this agent. This agent should behave like a recruiter for an AI company called OpenArrrI and he talks like a pirate. It should have a unique name like <PirateAgent434> - use `uip agent list` command to ensure there is no collision. 

This convrsational agent should reference a context grounding index containing current job openings.
In the project folder, there is a job-opening.pdf. You need to follow this process to create an Context Grounding index.
1. Create a Storage Bucket matching agent name in Shared root folder.
2. Upload the PDF to the Storage Bucket
3. Create an context grounding index using `uipath` CLI, from the newly created storage bucket
4. The index would take some time to be created, proceed first and when later trying to reference from an agent, check to ensure the index creation has completed.

Once the context grounding index is created, we need to create the agent itself. 
Once basic agent is created following all the hints in CLAUDE.md, we need to use `uip agent context add` command to add context grounding index reference to the agent, so the agent can query it to inform conversation with user.

## The frontend

Tech Stack: React 18 web app, vite, typescript, npm

The UX should approximate a virtual job recruiting booth where the recruting agent would casually discuss, assess the candidate and share info about the AI company OpenArrrI. Please make up info about this company and write the info into the system prompt. The frontend should use UiPath Typescript SDK to integrate the conversational agent - see: https://uipath.github.io/uipath-typescript/llms-full-content.txt for details.
The app would use External Applications auth from UiPath Platform, specifically PKCE flow, so no backend component is needed for the redirect. 

Here are some key UX features that we need to implement:
 - on session start, we should send an invisible message to the conversational agnt to elicit a "hello / introduction" message to the user. So from the user's point of view, the agent speaks first.
 - before agent response starts to stream, show an animated typing indicator
 - any tool use event would create a special messagea block showing what tool is being run, tool parameters and when available, tool results


Check your work, the use of UiPath Typescript SDK Conversational Agent capability is complex. Be sure to double check once coding is done, against relevent portion of https://uipath.github.io/uipath-typescript/llms-full-content.txt ONE MORE TIME to make sure you implemented everything correctly. Check specifically for streaming output handling to ensure first time success.

## Dev setup
make sure we can use `npm dev` and `npm build` to develop the app. Build the project to ensure it works. Launch the dev server at the end and invite the user to test.

## Deply as UiPath Coded App
UiPath provides a coded app hosting feature that can host the React app we are building on an internet facing URL. Once user confirm that the app works on dev server, let user know that you would deploy the app as hosted UiPath Coded App. Use the CLI to do this deployment.

## Support CLI tools

uip CLI tool - `uip` is a key tool for interacting with UiPath Agents platform.
Download necessary skills and tools using this CLI tool on your own to gain access to skills and tools necessary for accomplishing your task. Use -h parameter to learn how the CLI works.

run `uip skills` to discover commands that are needed as part of the project setup to installed necessary skills to develop on UiPath platform.

uipath CLI too - `uipath` - another key tool that has some additional features missing from `uip` such as the ability to create context grounding index. Check this if some commands are not available from `uip`
