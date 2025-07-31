# Serenio

# Personal Assistant iOS App for Neurodiverse Productivity

### Description

- Serenio is a highly integrated and accessible iOS application designed to support individuals with ADHD and ASD by consolidating essential iPhone utilities into one user-centric interface
- Built in Swift using a personal Apple Developer account, Serenio combines tools like a stopwatch, alarm scheduler, calendar, reminders, and note-taking, all designed to promote focus, routine, and self-management
- The app also integrates OpenAI API functionality and future extensibility for even richer assistance

---

## NOTICE

- Please read through this `README.md` to better understand the project's source code and setup instructions
- Also, make sure to review the contents of the `License/` directory
- Your attention to these details is appreciated — enjoy exploring the project!

---

## Problem Statement

- Navigating multiple apps to manage tasks, reminders, thoughts, and schedules can be overwhelming — especially for individuals with ADHD and ASD
- There is a need for a single, intuitive application that centralizes cognitive aids and organizational tools into one personalized ecosystem

---

## Project Goals

### Centralize Core Productivity Tools

- Merge timers, notes, alarms, calendars, and media into a unified application to reduce app-switching and cognitive load

### Learn, Practice, and Deploy Advanced iOS Development

- Utilize Apple’s developer ecosystem (Swift, UIKit/SwiftUI, AVFoundation, PencilKit, etc.) to gain mastery over app design, deployment, and accessibility tailoring

---

## Tools, Materials & Resources

### Development Toolchain

- Xcode, Swift, SwiftUI/UIKit, AVFoundation, PencilKit, CloudKit, OpenAI API

### Hardware & Deployment Platform

- iPhone, Apple Pencil, Apple Developer Account, macOS development machine

### Reference Material

- Apple Human Interface Guidelines, OpenAI API Documentation, iOS Accessibility Resources

---

## Design Decision

### Native iOS App in Swift

- Chosen for performance, low latency, deep hardware integration, and optimal access to native iOS features (e.g., Calendar, Reminders, Audio, Touch/Pencil input)

### Minimized Interface Switching

- Every tool lives within a tabbed interface or modular workspace to reduce distractions caused by jumping between apps

### Local-first with Cloud Syncing Options

- User data is stored locally with optional iCloud/CloudKit sync to preserve user privacy and offline functionality

---

## Features

### Core Utility Integration

- Stopwatch, Timer, Calendar View, Alarm Scheduler, and Apple Reminders synced into a cohesive interface

### Notes and Rich Input System

- Quick text-based note pad for typing (keyboard only) and a separate advanced note canvas with Apple Pencil support via PencilKit

### Multimedia and AI Integration

- Built-in music player with playlist management and OpenAI API integration for journaling, task planning, or motivational support

---

## Block Diagram

```plaintext
                                ┌─────────────────────────────┐
                                │       Serenio App (iOS)     │
                                └────────────┬────────────────┘
                                             ↓
                ┌──────────────────────────────────────────────┐
                │                Main Features                 │
                │  ┌────────────┬───────────┬────────────────┐ │
                │  │ Stopwatch  │ Calendar  │ Alarm Scheduler│ │
                │  ├────────────┴───────────┴────────────────┤ │
                │  │  Reminders │ Quick Notes │ Rich Notes   │ │
                │  └────────────┬─────────────┬──────────────┘ │
                │               ↓             ↓                │
                │        PencilKit Input    Keyboard UI        │
                └────────────────┬─────────────────────────────┘
                                 ↓
                ┌──────────────────────────────────────────────┐
                │  Music Player   │    OpenAI API Interface    │
                └─────────────────┴────────────────────────────┘

```

---

## Functional Overview

- Serenio is structured into modular sections accessible via a tabbed interface
- Each module operates independently but within a unified codebase, enabling the user to engage with timers, scheduling, reminders, music, notes, or AI-powered journaling, all without leaving the app

---

## Challenges & Solutions

### Maintaining Focus in a Multi-Tool Interface

- Introduced strict design constraints (limited colors, distraction-free UI modes, single-task zones) to reduce cognitive fatigue

### iOS Permissions and API Access Across Tools

- Used entitlements and system frameworks responsibly to access Calendar, Reminders, Photo Library, and Media Player APIs with proper privacy protections

---

## Lessons Learned

### Embracing Apple's Design Philosophy

- Following iOS HIG (Human Interface Guidelines) created a more intuitive and familiar experience that required less user training and allowed deep system integration

### Managing Feature Complexity with SwiftUI

- Modularizing features using SwiftUI views and MVVM helped reduce technical debt and simplified future expansion without cluttering existing logic

---

## Project Structure

```plaintext
root/
├── License/
│   ├── LICENSE.md
│   │
│   └── NOTICE.md
│
├── .gitattributes
│
├── .gitignore
│
└── README.md

```

---

## Future Enhancements

- Add Home Screen widget support for timers and reminders
- Integrate voice journaling using speech-to-text
- Enable biometric access (Face ID / Touch ID) for personal notes
- Sync to third-party productivity tools (Notion, Trello, Google Calendar)
- Implement real-time AI coaching mode with mood tracking
