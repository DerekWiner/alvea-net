# Alvea.net initial data model

This is a proposed data contract for the first resource coordination workflow, not an implemented database schema.

## Resource

- `resource_id`, stable application identifier
- `resource_type`, initially one agreed pilot category
- `description`, short description
- `location_index`, H3 cell or equivalent geographic index
- `visibility`, public, community-only or private
- `status`, available, unavailable, pending-confirmation or removed
- `created_at` and `updated_at`, timestamps
- `host_id`, reference to the host record

## Host

- `host_id`, stable identifier
- `display_name`, public label where appropriate
- `contact_reference`, optional reference to private contact details
- `verification_status`, unverified, self-attested or reviewed

A host record does not itself prove ownership or legal authority to grant access.

## Stewardship assignment

- `assignment_id`
- `resource_id`
- `steward_id`
- `status`, proposed, accepted, declined, ended
- `valid_from` and optional `valid_until`

## Status event

- `event_id`
- `resource_id`
- `actor_id`
- `previous_status` and `new_status`
- `occurred_at`
- `note`, optional and privacy-reviewed

## Collection or use event

- `use_event_id`
- `resource_id`
- `requester_id`
- `status`, requested, confirmed, completed, declined or cancelled
- `requested_at` and optional `completed_at`
- `confirmation_actor_id`, where applicable

## Data minimisation

Do not expose precise private addresses or personal contact information by default. Use the least precise location that still supports the intended coordination workflow. Keep an audit trail of changes, but do not treat a timestamp or a user-submitted record as independent verification.
