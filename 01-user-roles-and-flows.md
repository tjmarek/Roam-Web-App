# ROAM User Roles and Core Flows

## User Roles

### 1. Shipper / Poster
Can:
- Create an account.
- Create and manage loads.
- View bids on each load.
- Accept one bid or decline bids.
- View assigned loads and status.

### 2. Driver / Carrier
Can:
- Create an account.
- Set profile info including equipment type and service area.
- View open loads that match their equipment and area.
- Submit a bid on an open load.
- View bid status: pending, accepted, declined, withdrawn.
- View loads they won.

### 3. Admin
Can:
- View all users, loads, and bids.
- Suspend accounts.
- Mark fraudulent or duplicate loads.
- Override or close broken marketplace records if needed.

## Core Flow A: Post a Load
1. Shipper logs in.
2. Shipper clicks Post Load.
3. Shipper enters load details.
4. Shipper submits the load.
5. System sets status to Open.
6. Matching drivers can now see the load.

## Core Flow B: Driver Places Bid
1. Driver logs in.
2. Driver opens nearby matching loads.
3. Driver opens a load detail page.
4. Driver submits bid amount and optional message.
5. System records the bid as Pending.
6. Shipper sees the new bid.

## Core Flow C: Shipper Accepts Bid
1. Shipper opens a posted load.
2. Shipper reviews all bids.
3. Shipper accepts one bid.
4. System marks the accepted bid as Accepted.
5. System marks all other active bids as Declined.
6. System updates the load status to Assigned.
7. Winning driver sees the assigned load.

## Core Flow D: Decline or Close Load
1. Shipper may decline a bid without closing the load.
2. Shipper may cancel a load if no longer needed.
3. System marks the load as Cancelled and closes bidding.

## Driver Experience Rules
- Drivers should only see loads that are still Open.
- Drivers should only be able to bid once per load unless editing is explicitly allowed.
- Drivers should not see private poster contact info until their bid is accepted.

## Poster Experience Rules
- Posters should see bid count on each load.
- Posters should see bid amount, bidder name, equipment type, response time, and optional note.
- Posters should only be able to accept one bid.

## Admin Guardrails
- Admin can deactivate bad actors.
- Admin can archive test data.
- Admin can inspect audit history on load and bid changes.
