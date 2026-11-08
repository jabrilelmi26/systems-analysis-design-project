# Business Problem and Requirements

## Fictional stakeholders
- Student borrower: see available equipment and know due date.
- IT desk attendant: check inventory in/out, detect overdue loans.
- IT administrator: track equipment condition and audit activity.

## Scope
Included: inventory lookup, equipment issue/return, loans, due dates, overdue status, staff reporting.
Excluded: purchasing, payment, identity provider integration, automated enforcement.

## Functional requirements
- **FR-01:** Authorized staff can see whether an asset is available.
- **FR-02:** Staff can create a loan for an eligible borrower and available asset.
- **FR-03:** Each active asset can have at most one active loan.
- **FR-04:** Staff can record return time and condition.
- **FR-05:** Staff can view active and overdue loans.
- **FR-06:** Staff can see who performed check-in/check-out actions.

## Non-functional requirements
- **NFR-01:** Role-based access prevents borrowers from editing inventory.
- **NFR-02:** All timestamps are stored in UTC and displayed locally.
- **NFR-03:** The system avoids storing unnecessary sensitive borrower data.
- **NFR-04:** Backups and restore procedures are documented and tested before production use.

## Assumptions and open questions
- Borrower eligibility is verified by staff outside this prototype.
- Standard loan period is 7 days, subject to stakeholder approval.
- What should happen if equipment is reported lost or damaged?
- What is the required retention period for loan history?

## Acceptance example
Given asset LAP-001 is available and borrower B-101 is eligible, when an authorized attendant checks it out, a new active loan is created and LAP-001 becomes unavailable. A second active checkout attempt must fail.
