# First workflow, resource registration and stewardship

## Goal

Demonstrate one end-to-end resource record before adding payments, token incentives or agent autonomy.

## Actors

- **Host**, lists a resource and states what access is permitted.
- **Steward**, accepts responsibility for keeping the listing accurate.
- **Community user**, requests or records a collection or use event.
- **Operator**, resolves disputes and handles removals or safety reports.

## Workflow

1. Host creates a resource record.
2. The system validates required fields and assigns an identifier.
3. The system stores a location index at a privacy-appropriate precision.
4. Steward accepts or declines an assignment.
5. Host or steward updates status and availability.
6. A user records a request or collection event.
7. Host or steward confirms, declines or cancels the event.
8. Each status change records who made it and when.

## Initial success criteria

- A resource can be created, retrieved and updated.
- Invalid records are rejected with actionable errors.
- Status history is retained.
- Public visibility can be separated from private contact details.
- A resource is not represented as verified solely because someone submitted it.
- A user can report an incorrect or unsafe listing.

## Out of scope

Payments, tokens, automated ownership verification, autonomous agents, DAO governance and cross-chain settlement.
