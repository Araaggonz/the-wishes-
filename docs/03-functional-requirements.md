# Functional Requirements

## Purpose

This document defines the functional requirements for **The Wishes**.

Each requirement describes a capability that the system must provide from the user's perspective. The document intentionally avoids implementation details and focuses exclusively on the expected behavior of the application.

---

# FR-001 User Registration and Authentication

## FR-001 User Registration

The system shall allow users to create an account.

A registered user must provide:

- Unique username
- Display name
- Email address
- Password
- Date of birth

The system shall only allow registration for users who are at least **15 years old**.

---

## FR-002 User Authentication

The system shall allow registered users to log in using their email address and password.

---

## FR-003 Password Recovery

The system shall allow users to recover their password through email verification.

---

## FR-004 Account Management

The system shall allow users to modify:

- Display name
- Username
- Password
- Avatar

Sensitive changes must require email verification.

---

## FR-005 Avatar Selection

The system shall provide a collection of predefined avatars.

Uploading custom profile pictures is outside the scope of the first version.

---

# FR-002 Shared Spaces

## FR-006 Create Shared Space

The system shall allow users to create a Shared Space.

A Shared Space requires:

- Name
- Type (Personal or Collaborative)

Optional information:

- Occasion (Birthday, Christmas, Valentine's Day, etc.)
- Secondary Owner

---

## FR-007 Invitation System

The system shall generate invitation links for Shared Spaces.

The system shall also generate an alphanumeric invitation code as an alternative joining method.

---

## FR-008 Join Requests

Users joining through an invitation must be approved by the Shared Space Owner before becoming members.

---

## FR-009 Member Management

Owners shall be able to:

- Accept invitations
- Remove members
- Assign a Secondary Owner
- Leave the Shared Space

---

## FR-010 Shared Space Types

The system shall support two Shared Space modes.

### Personal

Only the owner may create wishes.

Other members may only fulfill wishes.

### Collaborative

Every member may create and fulfill wishes.

---

# FR-003 Wish Management

## FR-011 Create Wish

The system shall allow users to create wishes.

Required information:

- Title
- At least one image

---

## FR-012 Edit Wish

Users shall be able to modify their own wishes at any time.

---

## FR-013 Delete Wish

Users shall be able to delete their own wishes.

---

## FR-014 Wish Description

Users may optionally provide:

- Description
- Links
- Additional notes

---

## FR-015 Advanced Wish Information

Users may enable Advanced Mode.

Advanced Mode allows category-specific information.

Examples include:

Clothing

- Size
- Material
- Color

Books

- Author
- Publisher
- Series

Technology

- Brand
- Model
- Storage

Users may also create custom specifications.

---

## FR-016 Wish Media

Each wish shall support:

- One or more images
- Optional short videos

---

## FR-017 Wish Sharing

Users shall be able to share individual wishes with one or more Shared Spaces.

Sharing is managed per wish, not per Wishlist.

---

# FR-004 Wish Organization

## FR-018 Categories

The system shall provide predefined categories.

Users may also create custom categories.

Assigning a category is optional.

---

## FR-019 Folders

Users shall be able to create custom folders.

Folders organize wishes according to occasions.

Examples:

- Birthday
- Christmas
- Graduation

Assigning folders is optional.

A wish may belong to multiple folders.

---

## FR-020 Search

The system shall allow users to search wishes.

---

## FR-021 Filters

Users shall be able to filter wishes by:

- Category
- Folder
- Shared Space
- Status

---

# FR-005 Wish Fulfillment

## FR-022 Wish Availability

Every shared wish shall have a fulfillment status.

Available

Reserved

Completed

---

## FR-023 Reserve Wish

Users shall be able to reserve an available wish.

A reservation remains valid for **24 hours**.

During this period:

- Other members cannot reserve the same wish.
- The reserving member may cancel the reservation.

---

## FR-024 Reservation Expiration

If the reservation is not confirmed within 24 hours, the wish automatically becomes Available again.

---

## FR-025 Complete Wish

Users shall be able to mark reserved wishes as Completed.

Completed wishes disappear from active wish views.

---

## FR-026 Gift Giver Privacy

The system shall never reveal the identity of the user who completed a wish.

The gift giver may decide whether to disclose this information personally.

---

# FR-006 Notifications

## FR-027 Notification Preferences

Users shall be able to configure notification preferences.

---

## FR-028 Calendar Notifications

The system may notify users about:

- Birthdays
- Anniversaries
- Holidays
- Other important dates

---

## FR-029 Wish Notifications

Users may choose whether to receive notifications when:

- A wish is reserved
- A wish is completed

Notification details shall be configurable.

---

# FR-007 History

## FR-030 Wish History

Completed wishes shall remain stored in history.

They shall never be permanently removed automatically.

---

## FR-031 History Organization

Users shall be able to browse their history.

History shall include at least:

- Received wishes
- Fulfilled wishes

History shall be ordered from newest to oldest.

---

# Functional Principles

Every functional requirement should support the following principles.

- Simplicity first.
- Privacy by choice.
- Preserve surprise.
- People before products.
- Flexible wish creation.
- Meaningful gift-giving over shopping.
