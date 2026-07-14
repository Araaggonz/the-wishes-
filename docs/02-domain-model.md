# Domain Model

## Purpose

This document defines the core business entities of **The Wishes** and describes how they relate to one another.

The objective is to establish a shared understanding of the application's domain before designing the database, backend, or user interface.

---

# Core Domain

The Wishes revolves around a single central concept:

> **A Wish.**

Every other entity exists to create, organize, share, fulfill, or manage wishes.

---

# Domain Entities

## User

A User represents a registered person within the platform.

Every user owns a personal Wishlist where wishes are created and managed.

A user may participate in multiple Shared Spaces simultaneously.

### Responsibilities

- Register and authenticate.
- Create wishes.
- Organize wishes.
- Share wishes.
- Join Shared Spaces.
- Fulfill wishes from other users.
- Configure personal preferences.

---

## Wishlist

A Wishlist belongs exclusively to one User.

It contains every Wish created by that user.

A Wishlist is private by default.

Individual wishes can later be shared with one or more Shared Spaces.

### Characteristics

- One owner.
- Unlimited wishes.
- Private by default.

---

## Wish

A Wish represents anything that would make a user happy.

A wish may represent:

- Physical products
- Experiences
- Trips
- Events
- Handmade gifts
- Moments
- Services

A wish is intentionally flexible and should never require unnecessary information.

### Required Information

- Image
- Title

### Optional Information

- Description
- Brand
- Price
- Store
- Purchase link
- Color
- Notes
- Custom specifications

---

## Shared Space

A Shared Space is a private environment where members can discover and fulfill wishes shared by other participants.

Examples:

- Partner
- Family
- Friends
- University
- Coworkers

A Shared Space may operate in two different modes.

### Personal Mode

Only the owner shares wishes.

Other members can only fulfill them.

Example:

Ara creates a birthday wishlist and shares it with friends.

Friends cannot add their own wishes.

---

### Collaborative Mode

Every member owns their personal Wishlist but can choose to share wishes inside the Shared Space.

Every participant may become both:

- Wisher
- Doer

depending on the action being performed.

---

## Member

A Member represents the relationship between a User and a Shared Space.

Members can have different permissions.

### Roles

- Owner
- Secondary Owner (optional)
- Member

---

## Folder

Folders organize wishes according to the occasion.

Examples

- Birthday
- Christmas
- Valentine's Day
- Graduation

A Wish may belong to multiple folders.

---

## Category

Categories classify what the wish represents.

Examples

- Books
- Clothing
- Technology
- Home
- Games
- Experiences

Each category may define its own optional attributes.

Example:

Clothing

- Size
- Fit
- Material

Technology

- Model
- Storage
- Color

Books

- Author
- Publisher
- Saga

---

## Wish Status

Every Wish shared inside a Shared Space has a lifecycle.

Available

The wish can be fulfilled by any eligible member.

↓

Reserved

One member is deciding whether to fulfill the wish.

The reservation expires automatically after 24 hours if it is not confirmed.

While reserved:

- Other members cannot reserve it.
- The reserving member may cancel the reservation.

↓

Completed

The member confirms the wish has been fulfilled.

Completed wishes disappear from active views while remaining stored in history.

---

## Wish History

Completed wishes are never deleted.

History allows future features such as:

- Gift history
- Personal statistics
- Yearly summaries
- Memories
- Analytics

---

## User Preferences

Each user owns personal application settings.

Examples

Notifications

- Important dates
- Birthdays
- Anniversaries
- Holidays

Wish notifications

- Notify when a wish is completed
- Reveal completed wish
- Hide completed wish details

Privacy

- Public profile visibility
- Notification preferences

---

# Relationships

User

owns

→ Wishlist

User

belongs to

→ Shared Spaces

Wishlist

contains

→ Wishes

Wish

belongs to

→ Categories

Wish

may belong to

→ Multiple Folders

Wish

may be shared with

→ Multiple Shared Spaces

Shared Space

contains

→ Members

Member

references

→ User

Wish

has

→ Status

Completed Wishes

move to

→ Wish History

---

# Domain Principles

The following principles guide every future decision.

## People before products

The application exists to strengthen relationships rather than promote purchases.

---

## Wishes before shopping

A wish represents something meaningful to the user, not necessarily a product.

---

## Privacy by choice

Users decide who can see each individual wish.

---

## Flexibility over rigid structures

Only essential information should be required.

Everything else is optional.

---

## Surprise should be preserved

The fulfillment process should protect the surprise whenever possible.

---

## Simplicity first

Every new feature should reduce effort, not increase complexity.

---

# Domain Summary

The Wishes is not centered around groups or shopping.

The platform revolves around **Wishes**.

Users create wishes.

Wishes are organized.

Wishes are shared.

Other users fulfill wishes.

Everything else exists to support this journey.