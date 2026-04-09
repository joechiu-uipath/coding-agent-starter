# Create agent-powered web app using Claude Code

## Goal
Your goal is to help me create a custom web application that is a React web app with a chat UI to talk with a conversational agent that is authored and hosted on UiPath low-code agent platform.

## The conversational agent
This agent should behave like a recruiter for an AI company called OpenArrrI and he talks like a pirate. It should have a unique name like <PirateAgent434> - ensure its name is unique. 

I want the agent to be able to query our current job openings captured in a PDF file. I have a job-opening.pdf in the project folder with relevant data. Make sure this PDF is made into a Context Grounding index, so the agent can query it.

## The frontend

Tech Stack: React 18 web app, vite, typescript, npm

The UX should approximate a virtual job recruiting booth where the recruting agent would casually discuss, assess the candidate and share info about the AI company OpenArrrI. Please make up info about this company and write the info into the system prompt.

Here are some key UX features that we need to implement:
 - use External Applications auth from UiPath Platform, specifically PKCE flow, so no backend is needed for the redirect.
 - on session start, we should send an invisible message to the conversational agnt to elicit a "hello / introduction" message to the user. So from the user's point of view, the agent speaks first.
 - before agent response starts to stream, show an animated typing indicator
 - any tool use event or context grounding query would create a special messagea block showing what tool is being run, tool parameters and when available, tool results

## Deply as UiPath Coded App
I want to host this app and make it accessible online. Ask me to confirm that the app works locally on dev server, then deploy the app as a hosted UiPath Coded App.
