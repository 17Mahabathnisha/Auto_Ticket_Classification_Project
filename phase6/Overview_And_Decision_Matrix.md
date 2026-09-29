# Phase 6: Conditional Branching Logic & Decision Matrix

## 📌 Phase Overview
The objective of Phase 6 is to construct the multi-branch keyword decision tree inside Flow Designer[cite: 3]. The engine parses keywords within the ticket's `Short Description` field and executes automated `Update Record` actions to commit the correct `Category` and `Subcategory` directly to the database[cite: 3].

---

## 🎯 Key Objectives
1. Implement conditional branching for 4 distinct issue domains: Network, Hardware, Access, and Performance[cite: 3].
2. Accommodate common spelling variants and synonyms (e.g., `WiFi`, `Network`, `Projector`, `Prajector`, `Forgot password`, `Password`, `Login`, `Slow Computer`, `Slow`, `Hanging`)[cite: 3].
3. Bind dynamic record update actions to commit changes to the active incident record[cite: 3].

---

## 📋 Keyword Decision & Classification Matrix

| Rule # | Branch Type | Condition (Short Description Contains) | Assigned Category | Assigned Subcategory | Target Resolution Team |
| :---: | :--- | :--- | :--- | :--- | :--- |
| **Rule 1** | `If` | `WiFi` **OR** `Network` | **Network** (`network`) | **Wi-Fi** (`wi-fi`) | Network Infrastructure Team |
| **Rule 2** | `Else If` | `Projector` **OR** `Prajector` | **Hardware** (`hardware`) | **Projector** (`projector`) | Classroom AV & Hardware Support |
| **Rule 3** | `Else If` | `Forgot password` **OR** `Password` **OR** `Login` | **Access** (`access`) | **Forgot Password** (`forgot password`) | Identity & Access Management |
| **Rule 4** | `Else If` | `Slow Computer` **OR** `Slow` **OR** `Hanging` | **Performance** (`performance`) | **Slow computer** (`slow computer`) | Desktop & Lab Systems Support |