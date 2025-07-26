# DevSync - Project Collaboration Platform

DevSync is a full-stack collaboration platform that helps developers find and contribute to meaningful projects. It connects project maintainers and contributors through GitHub OAuth, with real-time updates and task tracking using Firebase Firestore.

---

## Overview

DevSync allows:

- Project owners to create and manage projects with tech stack tags.
- Developers to discover projects based on their preferred technologies.
- Real-time messaging and task assignment within projects.
- GitHub integration for repository creation, collaborator management, and pull request tracking.

---

## Key Features

### Project Discovery
- Search and filter projects by technologies.
- View detailed project descriptions, tags, and roles.

### Contributor Management
- Maintainers can:
  - Approve or reject collaboration requests.
  - Automatically add users as GitHub collaborators.
  - Assign tasks to contributors.
- Contributors can:
  - Send requests to join a project.
  - View and complete assigned tasks.
  - Link pull requests to tasks for verification.

### Authentication
- GitHub OAuth only.
- GitHub access is used to create repositories, manage collaborators, and track pull requests.

### Real-Time Collaboration
- Firebase Firestore handles:
  - Messaging
  - Join requests
  - Task updates

---

## Tech Stack

| Layer           | Technology                  |
|----------------|-----------------------------|
| Frontend        | React.js                    |
| Backend         | Spring Boot                 |
| Database        | MySQL                       |
| Real-Time DB    | Firebase Firestore          |
| Authentication  | GitHub OAuth                |
| GitHub API      | Repo and PR management      |

---

## Project Workflow

1. Users log in via GitHub OAuth.
2. Maintainers create a project and specify tech stack.
3. Contributors search and request to join relevant projects.
4. Join requests are stored in Firestore for real-time updates.
5. Approved contributors are added to the GitHub repo.
6. Tasks are created and assigned to contributors.
7. Contributors complete tasks and submit PRs linked to the tasks.
8. A backend job verifies PR status via GitHub and updates the task.

---
