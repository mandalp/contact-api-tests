# Contact API - Postman Automated Tests

This repository contains automated API tests for the Contact List application.

## Project Structure

- collections/ → Postman collection files
- environments/ → Postman environment files
- .github/workflows/ → GitHub Actions CI configuration

## Running Tests Locally

Install dependencies:

    npm install

Run the tests:

    npm test

## Continuous Integration

Tests run automatically on:
- Push to main
- Pull requests targeting main

Execution is handled using:
- Newman (Postman CLI runner)
- GitHub Actions

## Requirements

- Node.js 18+
- npm

## Notes

Environment variables should be configured properly before running tests.
Sensitive values should not be committed to the repository.