# Postman Collections for Registration Tests

This repository contains Postman collections for testing the registration flow of an application, including both negative and successful test scenarios. These collections are designed to be imported into Postman and executed seamlessly, with all necessary variables pre-configured as collection variables.

## Collections Overview

### 1. **Negative Tests Collection**
This collection contains tests to validate the application's error handling and input validation during the registration process. The included tests are:

- **Negative Test:** Attempt to create an account with an already registered email.
- **Negative Test:** Attempt to register with a weak password (e.g., too short or missing special characters).
- **Negative Test:** Attempt to register with an invalid email format.
- **Negative Test:** Attempt to register with missing required fields (confirmation url).
- **Negative Test:** Attempt to register with missing required fields (email).
- **Negative Test:** Attempt to register with missing required fields (password).

### 2. **Successful Registration Flow Collection**
This collection covers the complete happy path for user registration and associated functionalities. The included tests are:

- **Register:** Create a new account.
- **Confirm Email:** Verify the account using the confirmation email.
- **Resend Confirmation:** Resend the confirmation email.
- **Forgot Password:** Request a password reset email.
- **Change Password:** Update the account password after resetting it.

The successful registration flow uses the [Mailosaur API](https://mailosaur.com/) to retrieve and parse the confirmation email, extracting necessary values for the confirm call. All required variables such as server ID and domain are pre-configured in the collection variables, so no additional setup for Mailosaur is needed.

## Getting Started

### Prerequisites

1. [Postman](https://www.postman.com/downloads/) installed on your machine.

### Importing the Collections

1. Clone or download this repository.
2. Open Postman and navigate to the **Import** option.
3. Import the collections.
4. Ensure the collection variables are configured correctly.

### Configuring Variables

All required variables are defined as collection variables. Key variables include:

- **API Base URL:** The base URL for the application under test.
- **Mailosaur Server ID and Domain:** Pre-configured in the collection variables for retrieving test emails.

Ensure these variables are updated with appropriate values if necessary before running the collections.

### Running the Tests

1. Select the desired collection (Negative Tests or Successful Registration Flow).
2. Click the **Run** button to execute the collection in the Postman Runner.


