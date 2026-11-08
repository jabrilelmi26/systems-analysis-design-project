# Data Dictionary and Business Rules

| Table | Key fields | Purpose |
|---|---|---|
| BORROWER | borrower_id | Synthetic borrower identifiers and eligibility |
| ASSET | asset_id, asset_tag | Equipment condition and lifecycle status |
| STAFF | staff_id, role | Authorized desk operator |
| LOAN | loan_id, borrower_id, asset_id, processed_by | Checkout, due date, return history |
| AUDIT_EVENT | event_id, loan_id, actor_staff_id | Append-only record of checkout-related changes |

Business rules: Asset tags must be unique. A loan's `returned_at` is null while active. Each asset may have at most one active loan (enforce with database constraint or transaction logic). A damaged returned item stays unavailable pending inspection. Audit records should not store passwords.
