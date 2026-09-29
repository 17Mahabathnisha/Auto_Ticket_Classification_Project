# Phase 2: Step-by-Step Configuration Guide

## ⚙️ Step-by-Step Configuration Guide

### Step 1: Access the Tables Module
1. Navigate to the Left Application Navigator[cite: 7].
2. Search for **System Definition** → select **Tables**[cite: 7].
3. Click the **New** button to open the Table creation interface[cite: 7].

---

### Step 2: Define Core Table Attributes
Configure the basic attributes on the table form[cite: 7]:

| Field | Configuration Value | Description |
| :--- | :--- | :--- |
| **Label** | `Incident WorkFlow` | Display label for human users and form headers[cite: 7]. |
| **Name** | `u_incident_workflow` | Underlying database table identifier (auto-prefixed with `u_`)[cite: 7]. |
| **Application** | `Global` | Global application scope[cite: 7]. |
| **Create Module** | *Unchecked* | Keeps navigation clean and accessed via targeted workflows[cite: 7]. |
| **Extends Table** | *None* | Standalone base custom entity[cite: 7]. |

---

### Step 3: Configure Table Controls & Auto-Numbering
Switch to the **Controls** tab on the Table form to set up automatic sequential numbering[cite: 7]:

| Control Field | Value | Explanation |
| :--- | :--- | :--- |
| **Auto-number** | `true` (Checked) | Activates ServiceNow database sequence generator[cite: 7]. |
| **Prefix** | `INC` | Standard Incident identifier prefix[cite: 7]. |
| **Starting Number** | `500` | Initial sequence starting point[cite: 7]. |
| **Number of Digits** | `5` | Enforces 5-digit zero-padded formatting (e.g., `INC00500`, `INC00501`, `INC00511`)[cite: 7]. |
| **Create Access Controls** | `true` (Checked) | Auto-generates CRUD Access Control Lists (ACLs)[cite: 7]. |
| **User Role** | `u_incident_workflow_user` | Default access role[cite: 7]. |

---

### Step 4: Save and Commit Table Schema
1. Click **Submit** in the upper-right corner[cite: 7].
2. The ServiceNow database engine generates the physical database table, schema dictionary entries, and numbering sequence rules[cite: 7].