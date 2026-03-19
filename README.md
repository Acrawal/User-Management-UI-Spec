# User Interface Specification Document: User Management Screen

## 1. Overview
This document describes the functional and visual requirements for the User Management interface. The screen allows administrators to list, filter, and create/edit user records.

## 2. UI Components & Layout

### 2.1 User List Table (Left Side)
- **Columns:** ID, User Name, Email, Enabled.
- **Sorting:** Each column header contains up/down arrows for ascending and descending sort.
- **Filtering:** Each column has a filter icon (funnel) to trigger search/filter inputs.
- **Selection:** Clicking a row highlights the user and loads their details into the right-hand form.

### 2.2 Top Navigation Bar
- **New User Button:** A blue button with a '+' icon. When clicked, it resets the form on the right for a new entry.
- **Hide Disabled User Checkbox:** When checked, rows where 'Enabled' is 'false' are filtered out from the table.
- **Save User Button:** A blue button on the far right to commit changes or save a new user.

### 2.3 User Detail Form (Right Side) - "New User" Section
- **Username:** Text input field (Required).
- **Display Name:** Text input field (Required).
- **Phone:** Numerical/Text input field for contact information.
- **Email:** Text input with email format validation (e.g., name@domain.com).
- **User Roles:** A multi-select dropdown menu.
  - *Options:* Guest, Admin, SuperAdmin.
- **Enabled Checkbox:** A boolean toggle to set the user's active status.

## 3. Page Behavior & Logic
- **Initial State:** The table should load all users (unless 'Hide Disabled' is pre-checked). The form should be empty or show a "Select a user to edit" placeholder.
- **Search/Filter:** Filtering should happen in real-time or upon pressing 'Enter' in the filter field.
- **Validation:** The 'Save User' button should trigger a check for mandatory fields (Username, Email).
- **Feedback:** Upon saving, a success toast or notification should appear.

## 4. Technical Requirements
- **Language:** React/Angular/Vue (depending on stack).
- **Styling:** Consistent padding (e.g., 10px) between form elements and table borders.
- **Accessibility:** Use semantic HTML tags for the table and form labels.
