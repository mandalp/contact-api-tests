# Contact API - Postman Automated Tests

[![Run Postman Tests](https://github.com/mandalp/contact-api-tests/actions/workflows/postman-tests.yml/badge.svg)](https://github.com/mandalp/contact-api-tests/actions/workflows/postman-tests.yml)

## Overview

This repository contains an automated API test suite for the [Contact List application](https://thinking-tester-contact-list.herokuapp.com/) - [[API Documentation](https://documenter.getpostman.com/view/4012288/TzK2bEa8#abe537df-fccc-4ee6-90d2-7513e3024d6b)].

The purpose of this project is to demonstrate structured API validation, negative testing strategy, boundary analysis, and CI integration using Postman and GitHub Actions.

The test suite validates both positive flows and business rule validations such as:

- Required field validation
- Maximum length constraints
- Custom validations (email, phone, postal code)
- Date validation logic
- Response contract structure verification

---

## Tech Stack

- Postman (Collections & Environments)
- Newman (Postman CLI runner)
- Node.js
- GitHub Actions (CI)
- JavaScript (Postman test scripts)

---

## Project Structure

- collections/ → Postman collection files
- environments/ → Postman environment files
- .github/workflows/ → GitHub Actions CI configuration

---

## Testing Strategy

### Positive Scenarios
- Successful contact creation
- Response persistence validation
- ID generation validation
- Response structure verification

### Negative Scenarios
- Missing required fields
- Maximum length violations
- Invalid email format
- Invalid phone format
- Invalid postal code
- Invalid birthdate (including calendar validation)

### Contract-Level Assertions

Tests validate:

- HTTP status codes
- Field-level error structure
- Validation type (`required`, `maxlength`, `user defined`)
- Exact boundary limits
- Correct error targeting
- Absence of unexpected validation errors

This protects the API against silent regressions and unintended contract changes.

---

## Running Tests Locally

Install dependencies:

    npm install

Run the tests:

    npm test

---

## Continuous Integration

Tests run automatically on:
- Push to main
- Pull requests targeting main

Execution is handled using:
- Newman (Postman CLI runner)
- GitHub Actions

---

## Requirements

- Node.js 18+
- npm

---

## 👩‍💻 About the Author

This repository is part of my **professional QA Engineer portfolio**.

**Amanda Lopes**  
QA Engineer with experience in functional, exploratory, UI and API testing, focused on automation, test strategy, and delivering high-quality software through reliable and maintainable test solutions.

🔗 LinkedIn: https://www.linkedin.com/in/mandalps
