# Hi, I'm Yui Shibata 

**Accounts Receivable Accountant**

I automate the repetitive parts of hotel AR — OTA reconciliations, journal entries, prepayment reversals, and revenue allocations — so the books close faster and with fewer manual errors.

**Tools:** Python · Excel Power Query (M) · Excel VBA · QuickBooks Online · Business Importer · Google Drive

---

## 🛠️ Automations

| Project | What it does | Built with | Status |
|---|---|---|---|
| [OTA JE Generator](#ota-je-generator) | Detects the OTA from a dropped evidence file and generates the journal entry | Python | ✅ In use |
| [OTA Journal Entry Workflows](#ota-journal-entry-workflows) | Turns OTA payout and reservation data into JEs for each property | Power Query (M) | ✅ In use |
| [Prepayment Reversal Macro](#prepayment-reversal-macro) | Reverses customer prepayments to A/R once guests check out | Excel VBA | ✅ In use |
| [OTA Fee Withholding Checklist](#ota-fee-withholding-checklist) | Builds the monthly evidence checklist from the QuickBooks Transaction Report | Power Query (M) | ✅ In use |
| [F&B Revenue Allocation](#fb-revenue-allocation) | Simplifies the monthly F&B sales and fee split across outlets | Excel | 🔄 Improving |
| [Petty Cash JE Generator](#petty-cash-je-generator) | Turns the Mews payment report into a Business Importer upload for petty cash JEs | Python | ✅ In use |

---

### OTA JE Generator
Replaces per-OTA folders with **one drop location per hotel**. The script reads each evidence file, identifies which OTA it came from, and generates the journal entry automatically.
- Keeps the team's standard Excel table formatting
- Highlights cancellations in **yellow** and negative amounts in **red** for review
- Adds a **Check** sheet to confirm totals before upload

### OTA Journal Entry Workflows
Power Query pipelines that merge OTA payout data with reservation data to produce journal entries for multiple properties.
- Handles missing values in merges and filters
- Falls back to alternate guest-name fields when reservation data is incomplete
- Conditional formatting flags guests that don't match between the JE and reservation data

### Prepayment Reversal Macro
Automates reversing customer prepayments to A/R after a guest's stay — removing copy-paste and retyping while keeping the Business Importer output **exactly the same**.
- Assigns reversal JE numbers starting from the next QuickBooks JE number
- Nets partial refunds into a single reversal; closes guests that net to zero with no JE
- Applies each item in the month of check-out

### OTA Fee Withholding Checklist
Replaces a monthly copy-paste process with a Power Query that builds the OTA fee withholding evidence checklist directly from the QuickBooks Transaction Report.

### F&B Revenue Allocation
Streamlining the monthly workbook that allocates F&B revenue and payment fees across outlets (café, bar and restaurant), updated for the latest allocation rules.

### Petty Cash JE Generator
Reads the Mews payment report and writes a ready-to-upload Business Importer file for petty cash journal entries across all properties.
- Auto-suggests the property from the Mews report, then prompts for the JE number and journal date
- Keeps the standard Business Importer template formatting, one tab per property
- Highlights lines in **yellow** for review when they're missing an accounting category or have a negative amount

---

## 📈 Impact
- Fewer manual steps in daily bank and OTA reconciliation
- Consistent, review-ready output with built-in checks and highlights
- Repeatable month-end processes that are easier to hand over to a backup

---
