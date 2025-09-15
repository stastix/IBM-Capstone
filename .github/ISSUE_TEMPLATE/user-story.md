---
name: User Story
about: This template defines a user story
title: ''
labels: ''
assignees: ''

---

**As a** registered user
**I need** to create a book listing with title, author, condition, price, and an optional photo
**So that** other users can view and purchase my used book

### Details and Assumptions

Users must be authenticated to create a listing

Each listing must include title, author, condition, and price

Optional photo can be uploaded

Each listing gets a unique ID in the database 

### Acceptance Criteria

Given I am a logged-in user
When I send a POST request to /books with valid title, author, condition, price (and optional photo)
Then the book is saved in the database and a success response with the book ID is returned

Given I am not logged in
When I attempt to create a book listing
Then the API returns an unauthorized error


Given I send a POST request with missing required fields
When the request is processed
Then the API returns a validation error describing the missing fields
