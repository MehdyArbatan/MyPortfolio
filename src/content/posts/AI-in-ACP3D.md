---
author: Mehdi Akbarzadeh
pubDatetime: 2026-06-10T10:00:00Z
title: "Embedding Gemini AI in AutoCAD Plant 3D (experimental stage)"
postSlug: embedded-ai-plant3d
featured: true
draft: false
tags:
  - AutoCAD Plant 3D
  - C#
  - AI
  - API
  - Innovation
description: An experimental C# plugin integrating Google's Gemini AI SDK directly inside AutoCAD Plant 3D to execute spatial commands via natural language prompts.
---

## 1. The Problem
Plant Design software relies heavily on rigid GUI menus, custom toolbar buttons, or exact command-line syntax. Some operations such as querying database attributes, re-routing piping runs, or performing situational check ups (e.g. Valve Tag check, disconnected components and …) require designers to execute multiple manual clicks and navigation steps. This slows down modeling workflows and creates a steep learning curve for beginner  engineers. It also would tire out the user and consequently increase the human error factor.

## 2. The Logic Flow
To demonstrate the feasibility of natural language interaction inside industrial plant design software, I engineered a C# plugin that embeds Google's Gemini AI directly within AutoCAD Plant 3D:
- **In-App Chatbot UI:** Built a custom palette/window using C# and the AutoCAD .NET API that operates natively inside the Plant 3D workspace.
- **Natural Language Parsing:** When a user types an instruction (e.g., *"Perform a check up and find all Manual Valves’ which tags do not follow F21-MV-xxxx template."*), Gemini processes the prompt and produces the set of actions needed to be done.
- **Automated Execution:** The C# plugin parses the structured response and executes native AutoCAD commands, physically querying and manipulating the 3D target objects in real time.

## 3. The Result
This Proof of Concept (PoC) proves that modern AI Large Language Models (LLMs) can be successfully integrated into plant design software. It opens the door for future capabilities like conversational P&ID auditing, automated component placement, and instant database querying.

## 4. Video Demonstration
<iframe width="100%" height="400" src="https://www.youtube.com/watch?v=s-gw4zM3Q9g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
