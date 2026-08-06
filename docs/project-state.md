# StockFlow Project State

## Checkpoint 001 — Repository and Monorepo Foundation

**Date:** August 5, 2026
**Status:** Complete
**Git branch:** `main`
**Working tree:** Clean
**Remote:** GitHub
**Current milestone:** Monorepo foundation established

---

## 1. Project Overview

StockFlow is a warehouse management system designed to model real-world inventory and order management workflows.

The project is also being developed as a professional software engineering portfolio project.

The primary goal is to demonstrate practical engineering skills, including:

* Application architecture
* Backend development
* Database design
* Frontend development
* Testing
* Documentation
* Version control
* Security
* Deployment
* Professional development workflow

The project emphasizes understanding engineering decisions rather than blindly implementing generated solutions.

---

## 2. Current Architecture

StockFlow uses a monorepo architecture.

The repository currently contains separate frontend and backend applications managed within a single Git repository.

```text
stockflow/
├── client/
├── server/
├── docs/
├── package.json
├── package-lock.json
├── .gitignore
└── README.md
```

### Application boundaries

```text
StockFlow
│
├── Client
│   └── React + TypeScript
│
├── Server
│   └── Node.js + Express + TypeScript
│
└── Database
    └── PostgreSQL
```

The client and server will remain separate applications with a defined API boundary.

---

## 3. Technology Direction

### Frontend

* React
* TypeScript

### Backend

* Node.js
* Express
* TypeScript

### Database

* PostgreSQL
* Prisma ORM

### Development Tools

* Git
* GitHub
* VS Code
* npm

Additional technologies such as automated testing, Docker, CI/CD, and cloud deployment may be introduced as the project develops.

---

## 4. npm Workspace Configuration

The repository uses npm workspaces.

The root `package.json` defines:

```json
"workspaces": [
  "client",
  "server"
]
```

The root package is marked:

```json
"private": true
```

This prevents the StockFlow root workspace from accidentally being published to the npm registry.

### Workspace packages

Client:

```text
@stockflow/client
```

Server:

```text
@stockflow/server
```

Both application packages are currently marked private.

---

## 5. Current Repository Structure

At this checkpoint:

```text
stockflow/
├── client/
│   └── package.json
│
├── server/
│   └── package.json
│
├── docs/
│   └── engineering-handbook.md
│
├── node_modules/
│   └── ignored by Git
│
├── .gitignore
├── README.md
├── package.json
└── package-lock.json
```

`node_modules/` is intentionally excluded from version control.

`package.json` and `package-lock.json` are tracked project configuration files.

---

## 6. Git History

The repository currently contains these major commits:

```text
chore: initialize repository
docs: add engineering handbook
chore: configure npm workspaces
```

The latest commit established the npm workspace foundation.

The repository has been pushed to GitHub and the local `main` branch is synchronized with `origin/main`.

---

## 7. Completed Setup

The following development environment components have been established:

* Git
* GitHub repository
* SSH authentication with GitHub
* VS Code
* Node.js
* npm
* PostgreSQL
* pgAdmin
* StockFlow Git repository
* Monorepo directory structure
* Engineering Handbook
* npm workspace configuration

---

## 8. Engineering Documentation

The Engineering Handbook is located at:

```text
docs/engineering-handbook.md
```

It defines the project's engineering philosophy, development workflow, definition of done, repository architecture, and principles for AI-assisted development.

The handbook should evolve alongside the project.

Important architectural and engineering decisions should be documented as the project develops.

---

## 9. Development Principles

StockFlow will be developed incrementally.

The general workflow is:

```text
Plan
  ↓
Create Issue
  ↓
Create Feature Branch
  ↓
Implement
  ↓
Test
  ↓
Review
  ↓
Pull Request
  ↓
Merge
```

Features should be small enough to understand, test, and review effectively.

AI may assist with development, but the developer remains responsible for understanding the implementation, architectural decisions, testing, security, and final code quality.

---

## 10. Current State

The project has **not yet begun application implementation**.

The repository and development foundation are established, but the actual frontend and backend applications have not yet been scaffolded.

No production application functionality exists at this checkpoint.

This is intentional.

The project is being built incrementally so that architectural decisions are made before implementation becomes complex.

---

## 11. Next Milestone

### Milestone 002 — Frontend Foundation

The next major task is to establish the React + TypeScript frontend application inside:

```text
client/
```

The frontend setup will be inspected and understood before additional dependencies or application features are introduced.

After the frontend foundation is established, the backend foundation will be created in:

```text
server/
```

---

## 12. Open Decisions

The following decisions remain intentionally open and will be evaluated as development progresses:

* Frontend build tooling configuration
* Backend project structure
* API architecture
* Database schema
* Prisma schema design
* Testing strategy
* Authentication and authorization
* Error-handling strategy
* Logging
* API validation
* Deployment architecture
* CI/CD
* Docker usage
* Cloud platform

These should be decided when they become relevant rather than prematurely.

---

## 13. Checkpoint Rule

This document should be updated at meaningful project milestones.

A checkpoint should capture:

* What has been completed
* Current architecture
* Important decisions
* Git/repository state
* Current technology configuration
* Open questions
* Next milestone

The purpose is to maintain a reliable record of project evolution and provide a clear handoff point if development continues in another conversation or environment.

---

**Checkpoint 001 complete.**
