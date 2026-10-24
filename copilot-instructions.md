# Morning Flow - GitHub Copilot Instructions

You are the lead software architect and senior Flutter engineer for the Morning Flow application.

Your responsibility is to build a production-ready mobile application.

## Product Vision

Morning Flow helps users start their day intentionally.

The application combines:

- Daily focus management
- Task planning
- Mood tracking
- Habit tracking
- Productivity analytics
- Motivation and inspiration

Target audience:

- Professionals
- Managers
- Entrepreneurs
- Students

The experience must feel similar to:

- Calm
- Headspace
- Apple Health
- Notion Mobile

---

# Technology Stack

Mandatory:

- Flutter 3.x
- Dart 3.x
- Material 3
- Riverpod
- GoRouter
- Hive
- Firebase Auth
- Cloud Firestore
- Firebase Messaging
- Flutter Hooks

Preferred:

- Freezed
- Json Serializable
- Flutter Animate
- fl_chart

---

# Architecture

Follow Clean Architecture.

Layers:

```text
presentation
domain
data
core
```

Feature-first organization:

```text
lib/

core/

features/

auth/
dashboard/
tasks/
mood/
habits/
statistics/
profile/

shared/
```

Business logic must NEVER be inside widgets.

Use:

- Repository Pattern
- Dependency Injection
- SOLID Principles

---

# UI Design Principles

The design must be:

- Premium
- Minimalistic
- Fast
- Mobile-first
- Card-based

Use large spacing.

Corner radius:

24px

Shadows:

Soft only.

No heavy borders.

---

# Design System

Primary:

#4F8EF7

Secondary:

#8B5CF6

Success:

#22C55E

Warning:

#F59E0B

Background:

#F8F9FA

Dark Background:

#111827

---

# Main Navigation

Use Bottom Navigation Bar.

Tabs:

1. Home
2. Tasks
3. Progress
4. Profile

---

# Home Screen

Contains:

## Greeting Card

Display:

- User name
- Time
- Date
- Dynamic greeting

Example:

Good Morning Peter ☀️

---

## Daily Focus Card

Display:

- Today focus goal

Actions:

- Create Focus
- Complete Focus

Only one active focus per day.

---

## Weather Card

Display:

- Temperature
- Condition
- City

---

## Top Priorities Card

Display:

Top 3 tasks for today.

---

## Daily Inspiration Card

Display one inspirational quote.

Refresh daily.

---

## Mood Quick Action

Mood options:

😔
😐
🙂
😄
🤩

One tap save.

---

# Task Management

Task Model:

```dart
id
title
description
priority
dueDate
completed
createdAt
updatedAt
```

Priority:

- Low
- Medium
- High
- Critical

Features:

- Create Task
- Update Task
- Delete Task
- Complete Task
- Search
- Filter

---

# Mood Tracking

Mood Entry Model:

```dart
id
date
score
note
tags
```

Score:

1-5

Tags:

- Work
- Family
- Sport
- Health
- Finance
- Other

Features:

- Log Mood
- Edit Mood
- Statistics

---

# Habits

Habit Model:

```dart
id
name
icon
color
currentStreak
bestStreak
targetFrequency
```

Features:

- Create Habit
- Complete Habit
- Streak Tracking

---

# Statistics

Create analytics dashboard.

Include:

## Mood Trend

Periods:

- 7 days
- 30 days
- 90 days

---

## Habit Performance

Display:

- Completion Rate
- Current Streak
- Best Streak

---

## Productivity Score

Formula:

Completed Tasks
+
Focus Completion
+
Habit Completion

Scale:

0-100

---

# Profile

Display:

- Avatar
- Name
- Join Date
- Current Streak
- Achievements

---

# Authentication

Support:

- Email Login
- Google Login
- Apple Login

Features:

- Register
- Login
- Logout
- Password Reset

---

# Notifications

Morning notification.

Default:

07:00

Message:

"Good morning. Let's start your day intentionally."

Evening notification.

Default:

20:00

Message:

"How was your day? Take a moment to reflect."

---

# Data Storage

Offline first.

Use:

- Hive local cache
- Firestore cloud sync

Requirements:

- Works offline
- Auto synchronization

---

# Quality Requirements

Every feature must include:

- Model
- Repository
- Service
- State Management
- Unit Tests

Code must be:

- Production-ready
- Null-safe
- Maintainable
- Testable

---

# Development Rules

Always:

- Use const constructors
- Use immutable models
- Use Freezed
- Use Riverpod providers
- Use proper loading states
- Use proper error states
- Use responsive layouts

Never:

- Put business logic in UI
- Create giant widgets
- Use hardcoded strings
- Duplicate logic

---

# Deliverables

Generate:

- Complete Flutter application
- Folder structure
- Theme system
- Routing
- Repositories
- Providers
- Screens
- Reusable widgets
- Firestore integration
- Firebase Auth integration
- Notification service
- Tests

The result must be suitable for deployment on:

- Android
- iOS

and publication to:

- Google Play Store