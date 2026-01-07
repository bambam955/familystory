---
status: draft
author: Bennett Moore
creation_date: 2025-12-27
---

# Frontend Architecture

The frontend for FamilyStory will be built as a web app using Flutter/Dart.

## Design Decisions

### Flutter/Dart as Primary Tooling

Dart, a relatively new high-level programming language developed by Google, and Flutter, the cross-compilation tooling ecosystem designed around it, combine to form a very powerful platform for creating apps of any kind.

Flutter/Dart was chosen for this project's frontend for a few major reasons.

First, Flutter's tooling has the unique ability of being able to take one Dart codebase and cross-compile it for multiple platforms: web, Android, iOS, and so on. This is a major selling point of Flutter. While we won't take full advantage of this for MVP, since the MVP only includes a web app, it is very possible that other platforms could follow in the future.

Second, Flutter's UI library has been designed to optimize performance by minimizing the amount of component rebuilds that must be performed. This will be extremely important for our purposes when implementing a performant family tree canvas viewer, as we'll need to figure out how to dynamically load the view without requiring already rendered parts to be rebuilt.

Another advantage of Dart in this regard is that it's fully a compiled language, which is generally optimal for performance purposes. It also simplifies deployment.

Third, both Flutter and Dart are extremely actively maintained and modernized. The `pub` package manager provides quick access to a fast-growing array of packages; the tooling, including hot reload, linters, formatters, and code generation, is very up-to-date; and deployments are simple and easily automated with the `flutter build` CLI.

### API Interface

TBD. `http` package?

## Task List

TBD
