# Fabric + Foundry Lab

This guide is written for delivery inside LabDesktops.

Use the banner shown in the desktop for your lab credentials, guardrails, and any session-specific notes. Do not switch to a different browser profile during the workshop unless the facilitator asks you to.

## Overview

This workshop is a guided, portal-first lab covering Azure AI Foundry and Microsoft Fabric. You will not need to write code during the core path.

By the end of the session, you should have:

1. Confirmed access to the lab environment.
2. Built and tested an AI agent in Azure AI Foundry.
3. Grounded that agent with workshop knowledge.
4. Connected the agent to Microsoft Fabric data.
5. Compared static grounding with live data-backed responses.

> **Important:** Complete all labs in the same InPrivate or Incognito session used at the start of the workshop. This reduces the chance of accidentally using your own Microsoft account instead of the lab account.

## Labs At A Glance

| Lab | Title | Purpose |
|---|---|---|
| **Lab 0** | Sign in and start clean | Confirm you are in the correct browser session and can access Azure |
| **Lab 1** | Environment and access readiness | Verify Foundry, model, Fabric, and data access before building |
| **Lab 2** | Build and ground an AI agent | Create an agent, define instructions, and add knowledge |
| **Lab 3** | Connect live Fabric data | Add a Fabric-backed tool and test real data answers |
| **Lab 4** | Wrap-up and review | Consolidate what you built and discuss next steps |

## What Has Already Been Prepared For You

To keep the workshop focused on the hands-on workflow, the environment is prepared in advance. You do not need to build the core platform yourself.

You should already have:

1. A lab account and credentials.
2. Access to the Azure subscription used for the event.
3. Access to a personal or assigned Azure AI Foundry project.
4. Access to a Microsoft Fabric workspace containing the workshop data.
5. A shared model deployment available in Foundry.
6. A workshop knowledge file available for grounding steps.
7. Any shared Fabric data agents, semantic models, lakehouses, or reports required by the scenario.

## Important Working Rules

1. Stay inside the resources, workspaces, and projects assigned for the workshop.
2. Use only the prepared Foundry and Fabric assets unless the facilitator explicitly asks you to create something new.
3. If something looks missing, first check the account shown in the top-right corner before assuming permissions are broken.
4. If time is tight, focus on the core path first. Optional sections are marked clearly.

## Lab 0 — Sign In And Start Clean

## Overview

This short setup lab makes sure you are signed in correctly before the main hands-on work begins.

> **Lab duration:** ~5 to 10 minutes  
> **Format:** Browser only

## Prerequisites

1. You have the lab credentials provided in the session banner or by the facilitator.
2. You are starting from the desktop environment prepared for the lab.

## Step-By-Step Instructions

### Step 1 — Open A Clean Browser Session

1. Use the browser already provided in the lab desktop.
2. If you need to open a fresh session, use a new InPrivate or Incognito window.
3. Do not reuse a browser window that may already be signed in with your personal or company account.

> **What success looks like:** You have a clean browser session ready for lab sign-in.

### Step 2 — Open The Azure Portal

1. Navigate to:

   ```text
   https://portal.azure.com
   ```

2. Wait for the sign-in flow to appear.

> **What success looks like:** You see the Microsoft sign-in experience or land directly in the portal with the correct lab user.

### Step 3 — Sign In With Your Lab Account

1. Enter the lab username shown in the LabDesktops banner.
2. Continue through the sign-in flow.
3. Enter the password or temporary access pass if your session requires one.

### Step 4 — Handle Any Sign-In Prompts

1. If asked whether to stay signed in, choose the option recommended by the facilitator.
2. If prompted for additional verification, complete it using the lab instructions you were given.
3. If the flow redirects unexpectedly to a personal or company tenant, stop and ask for help.

### Step 5 — Confirm You Landed In The Correct Environment

1. Once the portal loads, check the top-right account indicator.
2. Confirm the displayed account is your lab user.
3. Stay in this same browser session for the rest of the workshop.

> **What success looks like:** You are signed in to Azure with your lab account and can reach the portal home page.

## ✅ You're Ready

You are now signed in correctly and ready to verify access to the workshop resources.

## Troubleshooting

| Issue | Resolution |
|---|---|
| Portal opens with the wrong account | Sign out fully, open a new InPrivate or Incognito window, and repeat Lab 0 |
| Sign-in loops or returns to an unexpected tenant | Close the browser window and restart from a clean session |
| You do not know which credentials to use | Use the values shown in the LabDesktops banner or ask the facilitator |
| MFA or temporary access prompt is unclear | Ask the facilitator before guessing or using a personal method |

## Lab 1 — Environment And Access Readiness

## Overview

This lab checks access to the resources you need before the build work starts.

> **Lab duration:** ~10 to 15 minutes  
> **Format:** Portal-based

## What Is Already Prepared For You

The workshop environment should already provide access to:

1. An Azure AI Foundry project.
2. A model deployment in that project.
3. A Microsoft Fabric workspace.
4. A Lakehouse, warehouse, semantic model, or other prepared data asset.

> **Quick troubleshooting check:** If you do not see the expected project, workspace, or resource, first confirm you are still in the same browser session from Lab 0 and signed in as the lab user.

## Step-By-Step Checks

### Step 1 — Confirm You Are Still Using The Lab Account

1. In a browser tab, open:

   ```text
   https://portal.azure.com
   ```

2. Confirm the account in the top-right corner is still your lab account.

> **Success criteria:** The displayed identity matches the lab credentials used in Lab 0.

### Step 2 — Confirm Azure AI Foundry Access

1. Open a new tab in the same browser session and go to:

   ```text
   https://ai.azure.com
   ```

2. If prompted to sign in, use the same lab account.
3. Open the project list or all-projects view.
4. Find your assigned project.

> **Naming note:** In many workshops, your project name includes your username or student number. Use the exact project name shown in the event instructions.

5. Open the project.

> **Success criteria:** You can enter the project and see navigation items such as **Agents**, **Playgrounds**, **Models + endpoints**, and **Files**.

### Step 3 — Confirm The Model Deployment Exists

1. Inside the project, open **Models + endpoints**.
2. Confirm at least one model deployment is available.
3. If the workshop provides a specific deployment name, confirm that exact deployment exists.

> **Success criteria:** You can see at least one deployment in a healthy state such as **Succeeded**, **Ready**, or equivalent.

### Step 4 — Confirm Microsoft Fabric Access

1. In the same browser session, open:

   ```text
   https://app.fabric.microsoft.com
   ```

2. If prompted, sign in with the same lab account.
3. Open **Workspaces**.
4. Locate the workspace assigned for the event.

> **Success criteria:** You can enter the workspace and see the prepared items.

### Step 5 — Confirm The Data Asset Is Visible

1. Open the workshop Lakehouse, warehouse, semantic model, or other primary data asset.
2. Confirm you can see the expected tables, views, or entities.
3. Preview at least one table or item.

> **Success criteria:** You can browse the data structure. Read access is enough for this step.

## ✅ Lab Complete

If all five checks succeeded, you are ready to start building.

## Troubleshooting

| Issue | Resolution |
|---|---|
| Cannot see your Foundry project | Confirm you are signed in with the lab account, then ask the support team to verify access |
| No model deployments appear | The deployment may still be provisioning or may use a different name; ask the facilitator to confirm |
| Cannot access the Fabric workspace | Ask the support team to verify your Fabric permissions |
| Data tables or artifacts are missing | Ask the support team to confirm the correct workspace and that sample data is loaded |

## Lab 2 — Build And Ground An AI Agent

## Overview

In this lab you will build, configure, and test an AI agent in Azure AI Foundry. You will define the agent's role and behaviour, then ground it with a workshop knowledge file.

> **Lab duration:** ~60 minutes  
> **Format:** Portal only  
> **Core goal:** Create an agent, give it useful instructions, add a knowledge file, and verify that grounded responses are better than ungrounded ones.

> **Time-saving note:** If time is short, focus on creating the agent, uploading the knowledge file, and getting at least one strong grounded response. Optional review and tracing steps can be skipped.

## Pre-Provisioned Resources

The following resources are expected to exist before this lab begins. Actual names may vary slightly in your environment.

| Resource | Type | Purpose |
|---|---|---|
| `<your-foundry-project>` | Azure AI Foundry Project | Your working project for the workshop |
| `<shared-model-deployment>` | Model deployment | The model used for playground and agent testing |
| `<knowledge-file-name>` | Workshop file | The document used to ground the agent |
| `<search-or-storage-resource-if-used>` | Supporting platform resource | Supports knowledge upload or retrieval behind the scenes |

## Prerequisites

1. Completed Lab 0 and Lab 1.
2. Confirmed access to the Foundry project and model deployment.

> **Quick troubleshooting check:** If you cannot see your project or model deployment, first confirm you are still in the same browser session from Lab 0 and signed in as the lab user.

## Part 1 — Navigate To Azure AI Foundry

### Step 1 — Open Azure AI Foundry

1. Open:

   ```text
   https://ai.azure.com
   ```

2. Sign in with the lab account if required.
3. Wait for the Foundry home page to load.

### Step 2 — Open Your Lab Project

1. Locate **Projects** or the **All projects** section.
2. Open your assigned project.
3. Review the left navigation so you know where to find **Agents**, **Playgrounds**, **Models + endpoints**, and **Files**.

> **What success looks like:** You are inside your assigned Foundry project and can navigate its main sections.

## Part 2 — Explore The Model Deployment

### Step 3 — View Available Model Deployments

1. Open **Models + endpoints**.
2. Locate the workshop deployment.
3. Check that it is healthy and available for testing.

### Step 4 — Run A Quick Playground Test

1. Open the chat playground or equivalent test surface in Foundry.
2. Use the workshop deployment.
3. Ask a simple baseline question that does not require domain knowledge.

Example prompts:

```text
Summarize what a responsible enterprise AI assistant should do when it does not know the answer.
```

```text
Explain the difference between general model knowledge and answers grounded in enterprise documents.
```

> **What success looks like:** You receive a normal baseline answer from the deployed model.

## Part 3 — Create And Configure An Agent

### Step 5 — Navigate To Agents

1. In the left navigation, click **Agents**.
2. Click **New agent** or the equivalent create option.
3. Open the agent configuration page.

> **What success looks like:** You see a page where you can define the agent name, model, instructions, tools, and related settings.

### Step 6 — Configure The Agent Identity

1. Give the agent a clear name tied to the workshop scenario.
2. Select the model deployment specified for the workshop.
3. Add instructions that define the role, tone, boundaries, and expected data sources.

You can start from a structure like this and adapt it to the final scenario:

```text
You are a workshop AI assistant for the current event scenario.
Use the provided knowledge and approved Fabric data sources when available.
Be clear, professional, and practical.
If information is missing or uncertain, say so instead of guessing.
Do not invent facts, policies, metrics, or recommendations.
```

4. Save the agent.

> **Tip:** If there are multiple collapsible sections, complete the required fields first: **Name**, **Model deployment**, and **Instructions**.

> **What success looks like:** The agent is saved and visible in the agent list or page header.

### Step 7 — Run An Initial Agent Test

1. Open the playground or test panel for the newly created agent.
2. Ask one or two scenario-relevant questions.
3. Note where the answer feels generic or too broad.

Example prompts:

```text
What kinds of questions should this assistant be able to answer for our event scenario?
```

```text
When should this assistant say that it does not have enough information?
```

> **What success looks like:** The agent responds, but the answers still rely mainly on general instructions and model knowledge.

### Step 8 — Optional: Refine The Instructions

If time allows:

1. Tighten the instructions.
2. Add clearer boundaries.
3. Re-test with a question that previously felt vague.

> **Optional success criteria:** The updated response is more controlled, more precise, or more appropriately cautious.

## Part 4 — Ground The Agent With Knowledge

### Step 9 — Upload The Knowledge File

> **File required:** Use the knowledge file provided for the workshop. If the facilitator supplied a specific file name, use that exact file. If you do not know where the file is, ask before continuing.

1. Open **Files** in the Foundry project.
2. Click **Upload file** or the equivalent add action.
3. Select the workshop knowledge file.
4. Wait for the file to finish processing.

> **What success looks like:** The uploaded file appears in the list with a usable status such as **Ready**.

### Step 10 — Attach The Knowledge To The Agent

1. Return to your saved agent.
2. Open the knowledge, files, or grounding section.
3. Attach the uploaded document.
4. Save the updated agent configuration.

> **What success looks like:** The knowledge source is attached to the agent and remains present after saving.

### Step 11 — Test The Grounded Agent

Ask questions that the knowledge file should improve.

Example prompts:

```text
Summarize the key guidance contained in the workshop knowledge file.
```

```text
What factors or practices does the document recommend that a participant should pay attention to?
```

```text
Which questions can this assistant answer confidently from the document, and which still require live data?
```

> **Observation:** Compare the answers here with your earlier ungrounded tests. Grounded answers should be more specific and better aligned to the workshop material.

> **What success looks like:** At least one response is clearly improved by the attached knowledge file.

## Part 5 — Optional Review And Explore

### Step 12 — Optional: Review The Agent Configuration Summary

1. Open the agent again.
2. Review the **Instructions**, **Model**, and **Knowledge** sections.
3. Confirm you can explain what each of those components contributes to the final behaviour.

### Step 13 — Optional: Review Traces Or Usage

If the feature is available in your environment:

1. Open the trace or monitoring view.
2. Review how the response was produced.
3. Note where this would matter for trust, debugging, or governance.

## ✅ Lab Complete

You have successfully:

- [x] Navigated Azure AI Foundry and opened your assigned project
- [x] Confirmed the workshop model deployment exists
- [x] Created and configured an AI agent
- [x] Tested the base agent behaviour
- [x] Grounded the agent with a knowledge file
- [x] Observed the difference between grounded and ungrounded responses
- [ ] *(Optional)* Refined instructions iteratively
- [ ] *(Optional)* Explored tracing or usage views

## Key Takeaways

1. Instructions shape behaviour, tone, and boundaries.
2. Knowledge grounding improves relevance for workshop-specific material.
3. A grounded agent is still different from a live-data agent. The next lab closes that gap.

## Troubleshooting

| Issue | Resolution |
|---|---|
| Cannot find your Foundry project | Confirm you are signed in with the correct lab account and ask support to verify project access |
| The workshop deployment is missing | The deployment name may vary or still be provisioning; ask the facilitator to confirm |
| File upload fails | Confirm you are in the correct project and using the expected file; retry after the project finishes loading |
| The agent is not referencing the file | Confirm the file status is ready and the knowledge source was saved to the agent |
| Responses are slow | This can happen in shared lab environments; wait a few seconds and retry |

## What's Next?

Next you will connect the agent to live Fabric data so it can answer questions backed by structured information rather than only instructions and static files.

## Lab 3 — Connect Live Fabric Data

## Overview

This lab builds on the agent from Lab 2 by connecting it to real data in Microsoft Fabric.

> **Lab duration:** ~75 minutes  
> **Format:** Portal-based  
> **Core goal:** Get at least one successful response that clearly comes from live Fabric data.

> **Time-saving note:** If time is short, focus on opening the shared Fabric data experience, connecting it to your agent, and getting one strong live-data answer. Optional advanced sections can be skipped.

## Pre-Provisioned Resources

The following resources are expected to exist before this lab begins.

| Resource | Type | Purpose |
|---|---|---|
| `<fabric-workspace>` | Microsoft Fabric Workspace | Contains the workshop data and prepared assets |
| `<primary-data-asset>` | Lakehouse, warehouse, or semantic model | Holds the structured data used in the lab |
| `<shared-fabric-data-agent>` | Fabric AI capability | Provides a natural-language interface to the data |
| `<your-foundry-project>` | Azure AI Foundry Project | Contains the agent you built in Lab 2 |
| `<your-agent-name>` | Azure AI Foundry Agent | The agent you will enhance with live data |

> **Note:** Resource names may vary slightly in your environment. Use the exact names shown in the event instructions or on-screen.

## Prerequisites

1. Completed Lab 2.
2. Verified access to the Fabric workspace in Lab 1.
3. Confirmed your Foundry agent is saved and working.

## Part 1 — Explore The Fabric Workspace

### Step 1 — Open Microsoft Fabric

1. In the same browser session from Lab 0, open:

   ```text
   https://app.fabric.microsoft.com
   ```

2. Sign in with the lab account if required.
3. Wait for the Fabric home page to load.

### Step 2 — Open The Lab Workspace

1. Click **Workspaces**.
2. Locate the workshop workspace.
3. Open it and review the listed items.

> **What you will see:** The workspace may contain a Lakehouse, semantic model, report, data agent, or other prepared assets depending on how the event is set up.

### Step 3 — Explore The Main Data Asset

1. Open the Lakehouse, warehouse, or semantic model used by the workshop.
2. Review the key tables, views, or entities.
3. Preview at least one item so you understand what kind of data the agent will query.

> **What success looks like:** You can describe the kinds of information available in the Fabric environment.

### Step 4 — Optional: Review The Semantic Model Or Relationships

If a semantic model is present:

1. Open it.
2. Review the fields or entities that look most relevant.
3. Note where the model may simplify end-user questioning.

## Part 2 — Use The Shared Fabric Data Experience

### Step 5 — Open The Shared Fabric Data Agent

1. Return to the workspace item list.
2. Locate the shared Fabric data agent or equivalent AI capability prepared for the event.
3. Open it.

> **If you do not see it:** In some environments it may appear under a different item label. Ask the facilitator if the name differs.

> **What success looks like:** The shared Fabric data experience opens successfully.

### Step 6 — Inspect What It Connects To

1. Review any configuration view or summary.
2. Confirm which data asset or model it uses.
3. Confirm that it is the shared event resource rather than a personal student copy, unless the facilitator has told you otherwise.

### Step 7 — Run A Test Query In Fabric

Ask one or two natural-language questions that should be answerable from the prepared data.

Example prompts:

```text
What are the main categories or entities represented in this dataset?
```

```text
Show an example question that this data source can answer reliably.
```

```text
Summarize one useful trend or pattern visible in the available data.
```

> **Optional:** If time is tight, one successful query is enough before moving on.

> **What success looks like:** The Fabric experience returns a meaningful answer that is clearly based on the prepared data.

## Part 3 — Add The Fabric Capability To Your Foundry Agent

### Step 8 — Return To Azure AI Foundry

1. Return to the browser tab containing your Foundry project.
2. Open the agent you created in Lab 2.

### Step 9 — Locate The Tools Section

1. Open the tools, functions, or integrations section of the agent.
2. Choose the option to add a tool, function, or external capability.

### Step 10 — Add The Fabric Data Tool

1. Add the workshop Fabric data capability using the method shown by the facilitator.
2. If a function name is generated or required, note it carefully.
3. Save the agent after the tool is added.

> **What success looks like:** The agent now shows a Fabric-backed tool in its tool list.

### Step 11 — Update The Instructions To Use The Tool

Update the agent instructions so it knows when to use the live data source.

You can start from language like this and adapt it to the workshop setup:

```text
When a question depends on current or structured workshop data, use the configured Fabric data tool.
Do not estimate values when the tool can retrieve them.
If the tool does not return enough information, say that clearly.
```

Save the updated instructions.

> **What success looks like:** The instructions clearly distinguish between knowledge-file answers and live-data answers.

## Part 4 — Query The Data-Enhanced Agent

### Step 12 — Test A Live-Data Question

Ask a question that should cause the agent to use the Fabric-backed tool.

Example prompts:

```text
Use the available workshop data and summarize one meaningful pattern or comparison.
```

```text
Answer using the live Fabric data rather than general guidance.
```

```text
What can you tell me from the current dataset that would not be available from the knowledge file alone?
```

> **What success looks like:** The answer clearly depends on live or structured data rather than only instructions or static grounding.

### Step 13 — Compare With Earlier Answers

1. Compare this response with one of your earlier grounded-only responses from Lab 2.
2. Note where live data changed the specificity, confidence, or factual basis of the answer.

## Part 5 — Optional: Return To Fabric And Explore Further

### Step 14 — Optional: Revisit The Workspace

1. Return to Fabric.
2. Open the data asset again.
3. Explore another table, view, or entity that looks relevant to the scenario.

### Step 15 — Optional: Identify Data Improvement Opportunities

1. Note any missing fields or ambiguous data.
2. Consider what would need to improve before using this in a real production workflow.

## Part 6 — Optional: Ask More Advanced Questions

### Step 16 — Optional: Try A More Complex Prompt

Ask a question that combines reasoning and data retrieval.

Examples:

```text
Based on the available data, what is one insight that would be useful to explain to a business stakeholder?
```

```text
Use the live data to identify one trend, then explain why it matters.
```

## Part 7 — Optional: Deploy The Agent As A Web App

### Step 17 — Optional: Deploy The Agent

If the feature is available in your region and subscription:

1. Use the built-in deployment or publish option in Foundry.
2. Follow the on-screen steps.
3. Record the generated URL if one is produced.

### Step 18 — Optional: Test The Deployed Experience

1. Open the resulting web experience.
2. Ask one live-data question.
3. Confirm the response quality remains acceptable outside the Foundry editing experience.

## ✅ Lab Complete

You have successfully:

- [x] Explored the prepared Fabric workspace and data assets
- [x] Used the shared Fabric data experience to query workshop data
- [x] Connected a Fabric-backed capability to your Foundry agent
- [x] Updated the agent instructions to use live data when needed
- [x] Verified at least one live-data answer
- [ ] *(Optional)* Explored additional data assets
- [ ] *(Optional)* Asked more advanced analytical questions
- [ ] *(Advanced)* Deployed the agent as a web application

## Key Takeaways

1. Knowledge files improve relevance, but live data tools improve factual freshness.
2. Tool choice and instructions matter as much as the raw data connection.
3. The most useful assistants combine instructions, grounding, and live tools in a controlled way.

## Troubleshooting

| Issue | Resolution |
|---|---|
| Cannot access the Fabric workspace | Confirm you are signed in with the lab account and ask support to verify access |
| Cannot find the shared Fabric data capability | It may use a different display name in your environment; ask the facilitator for the exact item |
| The Foundry agent is not using the tool | Re-check the tool configuration and the instruction update, then test again |
| The response sounds estimated rather than data-backed | Strengthen the instruction telling the agent to use the live data tool when answering structured questions |
| Responses are slow | This is expected in some shared environments; wait a few seconds and retry |
| Deployment to web app is unavailable | Skip the advanced deployment section; availability varies by region and subscription setup |

## What's Next?

The final lab is a short wrap-up to consolidate what you built and connect it to real-world delivery patterns.

## Lab 4 — Wrap-Up And Review

## Overview

This short closing lab helps consolidate the main ideas from the workshop.

> **Lab duration:** ~10 to 15 minutes  
> **Format:** Discussion and review

## Recap

By this point, you should have seen a practical pattern for building a portal-first AI assistant:

1. Instructions define the behaviour and boundaries.
2. Knowledge grounding improves relevance using workshop documents.
3. Live Fabric tools add factual, structured answers.
4. Optional tracing or review features improve trust and explainability.

## Discussion Prompts

Use the remaining time to discuss:

1. What changed when you moved from base model answers to a configured agent?
2. What changed again after adding a knowledge file?
3. What changed again after connecting live Fabric data?
4. Which part of the solution would need the most work before production use?
5. Which controls would matter most for access, safety, and governance?

## Optional Quick Demos

If time allows, revisit:

1. The saved agent configuration in Foundry.
2. The attached knowledge file.
3. The connected Fabric-backed tool.
4. Any trace or deployment view used during the session.

## ✅ Workshop Complete

You have now worked through a complete AI workshop pattern that combines:

- structured instructions
- grounded documents
- live data access
- step-by-step portal-based delivery

## Facilitator Notes For This File

Before the event, replace the placeholder values in this guide with:

1. The final scenario language.
2. The exact Foundry project, deployment, Fabric workspace, and data-asset names.
3. The exact knowledge file name used in Lab 2.
4. The exact Fabric data capability name used in Lab 3.
5. Relative screenshot links from `./assets/` anywhere the UI may be hard to recognize.