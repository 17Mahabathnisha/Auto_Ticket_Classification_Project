Team ID : SWTID-2026-2295
Team Name :Auto Ticket Classification using Flow Designer
Team Size : 5
# Phase 4: Dynamic Dependent Field Configuration - Overview & Mapping

## 📌 Phase Overview
The objective of Phase 4 is to establish strict data integrity and eliminate invalid field combinations by implementing a Parent-Child Dictionary Dependency[cite: 5]. When an end-user or IT technician selects a Category, the Subcategory dropdown dynamically filters on the client-side to display only the choices relevant to that category[cite: 5].

---

## 🎯 Key Objectives
1. Configure dictionary-level dependency on the `u_subcategory` column pointing to `u_category`[cite: 5].
2. Map each Subcategory choice value to its exact parent Category key in the `sys_choice` table[cite: 5].
3. Validate client-side dropdown filtering across all 4 category scenarios in the user interface[cite: 5].

---

## 🗺️ Category to Subcategory Dependency Mapping Matrix

| Parent Category (Label / Value) | Child Subcategory (Label / Value) | Enforced Dependency Value |
| :--- | :--- | :--- |
| **Network** (`network`) | **Wi-Fi** (`wi-fi`) | `network` |
| **Hardware** (`hardware`) | **Projector** (`projector`) | `hardware` |
| **Access** (`access`) | **Forgot Password** (`forgot password`) | `access` |
| **Performance** (`performance`) | **Slow Computer** (`slow computer`) | `performance` |