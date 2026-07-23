# ROAM MVP Scope

## MVP Outcome
The MVP should feel like a real working marketplace, even if advanced features are not included yet.

## Must-Have Features

### Authentication
- Email and password sign up.
- Login and logout.
- Password reset.
- Role selection during onboarding: shipper or driver.

### Profiles
- Shipper profile: company name, contact name, phone, email.
- Driver profile: name, company name, phone, email, equipment type, service radius, home base ZIP or city.

### Load Posting
Fields:
- Load title.
- Equipment needed: dump truck or flatbed.
- Pickup city or job location.
- Delivery city if needed.
- Load date.
- Description.
- Material or cargo type.
- Estimated weight or load size.
- Optional budget.

### Marketplace Discovery
- Open loads feed.
- Basic filter by equipment type.
- Basic filter by location.
- Sort by newest.
- Load detail page.

### Bidding
- Submit bid amount.
- Optional bid note.
- Track submitted bids.
- Shipper can accept or decline bids.

### Assignment
- Accepting a bid assigns the load.
- Assigned load appears in both shipper and driver dashboards.
- All non-winning bids are closed.

### Notifications
- In-app notification for new bid to poster.
- In-app notification for accepted or declined bid to driver.
- Email notification as a bonus if easy to implement.

## Nice-to-Have Features
- Driver can edit a pending bid.
- Driver can withdraw a pending bid.
- Map view.
- SMS notifications.
- Saved searches.
- Favorite routes or territories.

## Do Not Build Yet
- Stripe or integrated payments.
- Driver ratings.
- Insurance and compliance document workflows.
- Live location tracking.
- Dispatch board with drag-and-drop.
- Multi-tenant company accounts.
- AI pricing suggestions.

## MVP Definition of Done
- Users can authenticate.
- A shipper can post a load.
- A driver can bid on it.
- The shipper can accept one bid.
- The winning driver gets the assignment.
- App is deployable and usable by test users.
