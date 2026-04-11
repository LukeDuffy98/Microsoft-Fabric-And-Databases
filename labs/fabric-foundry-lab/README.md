# Fabric + Foundry Lab

This guide is written for delivery inside LabDesktops.

Use the banner shown in the desktop for your lab credentials, guardrails, and any session-specific notes.

## Lab Goals

By the end of this lab, you will:

1. Confirm you can access the event environment cleanly.
2. Create and test an AI agent in Azure AI Foundry.
3. Connect the agent to Microsoft Fabric data.
4. Validate the end-to-end experience using realistic questions.

## Before You Start

1. Work only in the browser and tools already opened in the lab desktop.
2. Use an InPrivate or Incognito session if the facilitator instructs you to open any new browser windows.
3. If a page shows the wrong account, stop and correct that before moving on.

## Part 0: Access Check

### What success looks like

- You can open the required portals.
- You can identify the resource names provided for this session.
- You do not see sign-in prompts for personal accounts.

### Steps

1. Open the Azure portal.
2. Confirm you are signed in with the lab account shown in the banner.
3. Open Azure AI Foundry and confirm you can reach the project or workspace prepared for this event.
4. Open Microsoft Fabric and confirm you can access the workspace prepared for this event.

### If something is wrong

- If you see the wrong account, sign out and retry with the lab account only.
- If Azure AI Foundry or Fabric does not load, ask the facilitator to verify your assigned access.

## Part 1: Readiness Validation

### What success looks like

- You can see the prepared model deployment.
- You can see the prepared Fabric workspace artifacts.
- You know which resources are shared and which are yours.

### Steps

1. In Azure AI Foundry, locate the model deployment assigned for this workshop.
2. In the Foundry project, identify the place where you will create or edit your agent.
3. In Microsoft Fabric, locate the workspace, lakehouse, warehouse, or semantic model used in this lab.
4. Verify that any resource names referenced by the facilitator match what you see.

## Part 2: Build the Agent

### What success looks like

- Your agent exists.
- It has clear instructions.
- It answers grounded questions using the workshop context.

### Steps

1. Create a new agent in the prepared Foundry project.
2. Give it a name that matches the event scenario.
3. Add concise instructions that define:
   the assistant role,
   the tone,
   what data it should use,
   what it should avoid claiming.
4. If this lab includes grounding documents, upload them now from the provided workshop files.
5. Run a small set of test prompts and note any weak responses.

### Suggested test prompts

1. Ask a factual question that should be answered from the grounding material.
2. Ask a question that requires the assistant to explain a result clearly.
3. Ask a question that should be declined if the information is unavailable.

## Part 3: Connect Fabric Data

### What success looks like

- The agent can use Fabric-backed context or tools.
- Responses improve when data is required.
- You can explain what came from data versus what came from instructions.

### Steps

1. Open the prepared Fabric data asset for this workshop.
2. Review the main tables, views, or semantic model entities used by the scenario.
3. Connect the Fabric data capability required by the workshop to your Foundry agent.
4. Ask a question that requires live or structured data.
5. Compare the result with an earlier non-data-backed response.

## Part 4: Validate the Experience

### What success looks like

- The agent can answer both grounded and data-driven questions.
- You understand the boundaries of the solution.
- You can describe one improvement you would make next.

### Steps

1. Test three final prompts that cover:
   a grounded content question,
   a Fabric data question,
   a question the agent should handle carefully.
2. Record which answer was strongest and why.
3. Identify one gap in instructions, data modeling, or tool configuration.

## Wrap-Up

Use the remaining time to discuss:

1. Which parts of the workflow were shared infrastructure versus per-student resources.
2. How grounding and Fabric data changed the answer quality.
3. What would need to change before using this pattern in a real organization.

## Facilitator Notes For This File

Before the event, replace the placeholders in this guide with:

1. The final scenario language.
2. The exact Foundry and Fabric artifact names students should open.
3. Any file names that will be downloaded or uploaded during the lab.
4. Relative screenshot links from `./assets/` where students may need visual guidance.