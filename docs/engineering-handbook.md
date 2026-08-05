# StockFlow Engineering Handbook

## Purpose

This document defines the engineering practices, architectural decisions,
development workflow, and standards used throughout the StockFlow project.

The goal is to build StockFlow using practices that resemble a professional
software engineering environment.

---

## Project Overview

StockFlow is a warehouse management system designed to model real-world
inventory and order management workflows.

The project is also a professional portfolio project intended to demonstrate
practical software engineering skills, including application architecture,
backend development, database design, testing, documentation, version
control, and deployment.

---

## Engineering Philosophy

The goal of StockFlow is not simply to produce a working application.

The project should demonstrate how a professional software engineer
approaches a software problem.

We will prioritize:

- Understanding requirements before implementation
- Clear architectural decisions
- Maintainable code
- Meaningful testing
- Security
- Documentation
- Version control
- Code review
- Incremental development
- Continuous improvement

We will favor understanding over blindly copying solutions.

---

## AI-Assisted Development

AI tools may be used as development assistants.

Appropriate uses include:

- Explaining unfamiliar concepts
- Reviewing code
- Suggesting implementation approaches
- Generating boilerplate
- Writing tests
- Debugging
- Refactoring
- Improving documentation

The developer remains responsible for:

- Understanding the code
- Architectural decisions
- Testing
- Security
- Code quality
- Final implementation decisions

AI-generated code should not be accepted without understanding what it does
and why it is appropriate for the project.

---

## Repository Architecture

StockFlow uses a monorepo architecture.

The repository contains the frontend, backend, and engineering documentation
within a single Git repository.

Initial structure:

    stockflow/
    |-- client/
    |-- server/
    `-- docs/

### Rationale

A monorepo provides a straightforward development environment for StockFlow
while keeping the frontend and backend clearly separated.

It also allows the complete application architecture and documentation to be
managed together.

The frontend and backend remain separate applications with a defined API
boundary.

---

## Technology Direction

### Frontend

- React
- TypeScript

### Backend

- Node.js
- Express
- TypeScript

### Database

- PostgreSQL
- Prisma ORM

### Development Tools

- Git
- GitHub
- VS Code

Additional technologies such as Docker, automated testing, CI/CD, and cloud
deployment will be introduced as the project develops.

---

## Development Workflow

Development should follow an incremental workflow:

    Plan
      |
      v
    Create Issue
      |
      v
    Create Feature Branch
      |
      v
    Implement
      |
      v
    Test
      |
      v
    Review
      |
      v
    Pull Request
      |
      v
    Merge

Features should be small enough to understand, test, and review effectively.

---

## Definition of Done

A feature is considered complete when:

- Code has been implemented
- Appropriate tests have been created
- Errors have been handled
- Documentation has been updated when necessary
- Code has been reviewed
- Linting passes
- Tests pass
- The feature has been merged

---

## Documentation Principle

Project documentation is treated as part of the software.

Important architectural and engineering decisions should be documented
alongside the code.

Documentation should evolve as the project evolves rather than being treated
as a one-time task.