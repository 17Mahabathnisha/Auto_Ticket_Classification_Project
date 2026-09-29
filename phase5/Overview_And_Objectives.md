Team ID : SWTID-2026-2295
Team Name :Auto Ticket Classification using Flow Designer
Team Size : 5
# Phase 5: Flow Designer Workflow Initialization - Overview & Objectives

## 📌 Phase Overview
The objective of Phase 5 is to initialize the automated backend triage engine using ServiceNow Flow Designer (Workflow Studio). We configure the root trigger condition to ensure the workflow executes in real time whenever an uncategorized ticket is submitted.

---

## 🎯 Key Objectives
1. Create a new flow named `Auto Classify School IT Tickets`.
2. Configure the event-driven trigger on table `Incident WorkFlow` (`u_incident_workflow`).
3. Define trigger condition criteria to only target tickets where `Category is Empty`[cite: 4].