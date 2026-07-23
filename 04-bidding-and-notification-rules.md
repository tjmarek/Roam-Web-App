# ROAM Bidding and Notification Rules

## Bidding Rules
- Only authenticated drivers can bid.
- Only drivers whose equipment type matches the load should see it by default.
- Drivers can only bid on loads with status Open.
- One active bid per driver per load for beta.
- Bid must include an amount.
- Bid note is optional.

## Acceptance Rules
- Only the load owner can accept a bid.
- Accepting a bid immediately changes the load status to Assigned.
- Accepting a bid immediately closes all other bids on that load.
- After a load is assigned, no new bids may be submitted.

## Notification Events

### Notify poster when:
- A new bid is submitted.
- A driver withdraws a bid.

### Notify driver when:
- Their bid is accepted.
- Their bid is declined.
- A load they bid on is cancelled.

## Beta Notification Channels
Priority order:
1. In-app notifications.
2. Email notifications.
3. SMS later, not in beta.

## Notification Payload Ideas
- New bid: "You received a new bid on [load title]."
- Bid accepted: "Your bid was accepted for [load title]."
- Bid declined: "Your bid was not selected for [load title]."
- Load cancelled: "A load you bid on was cancelled."

## Audit Trail Events
Store basic history for:
- Load created.
- Load updated.
- Bid submitted.
- Bid withdrawn.
- Bid accepted.
- Bid declined.
- Load cancelled.

## Matching Logic for Beta
Keep it simple:
- Match by equipment type first.
- Then filter by service area using city, ZIP, or radius if available.
- If location logic gets complicated, use a simpler beta rule: drivers choose regions manually and only see loads in those regions.
