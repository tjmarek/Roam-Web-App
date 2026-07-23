# ROAM Data Model

## Suggested Core Tables

### users
- id
- email
- password_hash or auth_provider_id
- role (shipper, driver, admin)
- full_name
- phone
- created_at
- updated_at
- is_active

### shipper_profiles
- id
- user_id
- company_name
- contact_name
- city
- state
- default_posting_radius
- created_at
- updated_at

### driver_profiles
- id
- user_id
- company_name
- equipment_type
- home_city
- home_state
- zip_code
- service_radius_miles
- is_available
- created_at
- updated_at

### loads
- id
- shipper_user_id
- title
- equipment_type
- status (draft, open, assigned, completed, cancelled)
- pickup_city
- pickup_state
- delivery_city
- delivery_state
- load_date
- description
- material_type
- estimated_weight
- budget_amount
- accepted_bid_id
- created_at
- updated_at

### bids
- id
- load_id
- driver_user_id
- bid_amount
- note
- status (pending, accepted, declined, withdrawn)
- created_at
- updated_at

### notifications
- id
- user_id
- type
- title
- body
- related_load_id
- related_bid_id
- is_read
- created_at

## Relationships
- One user has one role.
- One shipper user can create many loads.
- One driver user can create many bids.
- One load can have many bids.
- One load can have zero or one accepted bid.
- One user can receive many notifications.

## Status Logic

### Load Status
- draft: created but not published.
- open: visible for bids.
- assigned: a winning bid has been accepted.
- completed: job finished manually later.
- cancelled: closed without assignment.

### Bid Status
- pending: active bid waiting for shipper decision.
- accepted: winning bid.
- declined: shipper rejected bid or another bid was accepted.
- withdrawn: driver removed bid before decision.

## Data Rules
- A driver cannot submit a bid if the load is not open.
- A load can only have one accepted bid.
- If a bid is accepted, all other pending bids for that load become declined.
- If a load is cancelled, all pending bids become declined.
- Only the shipper who created the load can accept or decline bids on that load.
