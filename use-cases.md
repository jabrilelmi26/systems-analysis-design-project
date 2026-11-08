# Use Cases (Fictional)

## UC-01: Check out asset
**Actor:** IT desk attendant
**Preconditions:** Staff authorized; borrower eligible; asset available.
**Main flow:** Search asset → confirm condition → select borrower → set due date → save loan → provide receipt.
**Alternate flow:** If asset already has an active loan, block checkout and show current availability.
**Postcondition:** One active loan exists, audit event recorded.

## UC-02: Return asset
**Actor:** IT desk attendant
**Main flow:** Locate active loan → inspect asset → capture condition → mark returned → create audit event.
**Alternate flow:** If damaged, flag asset for review rather than available.

## UC-03: Review overdue loans
**Actor:** IT administrator
**Main flow:** Open overdue report → filter by due date → review list → follow approved follow-up process.
**Privacy rule:** Do not export or publish borrower information outside approved tools.
