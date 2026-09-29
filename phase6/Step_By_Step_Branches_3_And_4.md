Team ID : SWTID-2026-2295
Team Name :Auto Ticket Classification using Flow Designer
Team Size : 5
# Phase 6: Step-by-Step Configuration (Branches 3 & 4) & Verification

## ⚙️ Configuration Guide (Continued)

### Branch 3: Password / Access Issue Logic
1. Click **Add Flow Logic** → select **Else If**[cite: 3].
2. **Condition Label**: `SD is Forgot password`[cite: 3].
3. **Condition**:
   - `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Forgot password`[cite: 3]
   - **OR** `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Password`[cite: 3]
4. Inside the `then` branch, add **Update Record**:[cite: 3]
   - **Record**: `Trigger -> Incident WorkFlow Record`[cite: 3]
   - **Fields**:
     - `Category` = `Access`[cite: 3]
     - `Subcategory` = `Forgot Password`[cite: 3]
5. Click **Done**[cite: 3].

---

### Branch 4: Slow Computer / Performance Issue Logic
1. Click **Add Flow Logic** → select **Else If**[cite: 3].
2. **Condition Label**: `SD is Performance`[cite: 3].
3. **Condition**:
   - `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Slow computer`[cite: 3]
   - **OR** `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Performance`[cite: 3]
4. Inside the `then` branch, add **Update Record**:[cite: 3]
   - **Record**: `Trigger -> Incident WorkFlow Record`[cite: 3]
   - **Fields**:
     - `Category` = `Performance`[cite: 3]
     - `Subcategory` = `Slow computer`[cite: 3]
5. Click **Done**[cite: 3].

---

## ✅ Phase Verification Checklist
- [x] All 4 conditional branches implemented with exact string matching operators[cite: 3].
- [x] Update Record actions configured for each branch targeting the trigger record[cite: 3].
- [x] Category and Subcategory fields populated dynamically based on decision criteria[cite: 3].
- [x] Logic validated against syntax and data type constraints[cite: 3].