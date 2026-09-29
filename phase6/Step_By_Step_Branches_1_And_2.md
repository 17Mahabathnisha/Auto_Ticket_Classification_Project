# Phase 6: Step-by-Step Configuration (Branches 1 & 2)

## ⚙️ Configuration Guide

### Branch 1: Wi-Fi / Network Issue Logic
1. Under **Actions**, click **Add Flow Logic** → select **If**[cite: 3].
2. **Condition Label**: `SD is wifi OR network`[cite: 3].
3. **Condition**:
   - `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Wi-Fi`[cite: 3]
   - **OR** `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Network`[cite: 3]
4. Click **Done**[cite: 3].
5. Inside the `then` branch, click **Add an Action** → select **Update Record**:[cite: 3]
   - **Record**: `Trigger -> Incident WorkFlow Record`[cite: 3]
   - **Fields**:
     - `Category` = `Network`[cite: 3]
     - `Subcategory` = `Wi-Fi`[cite: 3]
6. Click **Done**[cite: 3].

---

### Branch 2: Projector / Hardware Issue Logic
1. Click **Add Flow Logic** → select **Else If**[cite: 3].
2. **Condition Label**: `SD is projector OR hardware`[cite: 3].
3. **Condition**:
   - `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Projector`[cite: 3]
   - **OR** `Trigger -> Incident WorkFlow Record -> Short Description` **contains** `Prajector`[cite: 3]
4. Inside the `then` branch, add **Update Record**:[cite: 3]
   - **Record**: `Trigger -> Incident WorkFlow Record`[cite: 3]
   - **Fields**:
     - `Category` = `Hardware`[cite: 3]
     - `Subcategory` = `Projector`[cite: 3]
5. Click **Done**[cite: 3].