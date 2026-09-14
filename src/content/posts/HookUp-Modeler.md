---
author: Mehdi Akbarzadeh
pubDatetime: 2026-02-10T10:00:00Z
title: "Automated Piping Assembly & Hook-up Modeler in AVEVA E3D/PDMS"
postSlug: automated-hookup-piping-modeler
featured: true
draft: false
tags:
  - AVEVA E3D/PDMS
  - PML
  - Instrumentation
  - Automation
description: A custom PML macro that automatically verifies and models instrumental tappings, vents, and drains to enforce 100% compliance with governing Hook-up drawings.
---

## 1. The Problem
Modeling typical piping assemblies, such as instrumental tappings, test drains, and vents, is a repetitive, time-consuming and tiring activity for mid to large scale projects.
Because these configurations should be modeled thousands of times per project, manual modeling inevitably results in human error and creates discrepancies between the model and the project's approved Hook-up drawing or Piping Assembly drawing.
This forces Lead Engineers to spend valuable man-hours on manual cross-checking and rework.

## 2. The Logic Flow
To eliminate this issue, I developed a macro in PML:
- **Data Input:** The user is prompted to specify the assembly type, tag, and branching component.
- **Automated Document Verification:** Before generating any geometry, the macro queries the selected elements and branching component to check against the project’s governing document rules and specifications.
- **Error Prevention & Warnings:** If any validation check fails, the macro instantly halts execution and returns a detailed warning to the user, showing exactly what is the issue.
- **Automated Execution:** Upon successful verification, the macro instantly generates a new `BRAN` element, assigns the correct tag, and builds all required piping components natively in a fraction of a second.

## 3. The Result
This macro will reduce the modeling time of each assembly from an average of 5 minutes to under 10 seconds. Multiplying this to the number of all the Pressure, Temperature, Level, Vent and Drain tappings that should be modeled will yield to a considerable reduction in required man/hour for both modeling and afterwards checking activities.

## 4. Video Demonstration
<iframe 
  width="100%" 
  height="400" 
  src="https://www.youtube.com/watch?v=R8X6r9Ouv-Q" 
  title="YouTube video player" 
  frameborder="0" 
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
  allowfullscreen>
</iframe>