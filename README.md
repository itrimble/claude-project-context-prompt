# Claude Development Toolkit: Context Templates & MCP Configuration

## Author

* **Ian Trimble**
    * GitHub: [itrimble](https://github.com/itrimble)
    * LinkedIn: [linkedin.com/in/itrimble](https://www.linkedin.com/in/itrimble/)
    * Website: [remnantsecurity.com](https://remnantsecurity.com)

## Overview

This repository provides a complete toolkit for optimizing your development workflow with Anthropic's Claude AI assistant. It includes two essential components:

1. **Project Context Templates** - Structured templates for providing comprehensive project context to Claude
2. **MCP Configuration Guide** - Setup instructions for Model Context Protocol (MCP) servers and permission management

Together, these tools enable Claude to function as a knowledgeable team member with access to your development environment and full project understanding.

## 🚀 Quick Start

### For Project Context Templates
1. Copy the [Universal Project Context Template](#universal-project-context-prompt-template-for-claude) below
2. Create a `Claude.md` file in your project
3. Fill out all sections with your project details
4. Use when starting new Claude conversations

### For MCP Setup
1. Follow the [MCP Configuration Guide](#mcp-configuration-guide) below
2. Configure permission rules for your development tools
3. Enable Claude Code access to your repositories and tools

---

# 📋 Project Context Templates

## Purpose

When working with advanced AI assistants like Anthropic's Claude, providing comprehensive and structured project context is crucial for obtaining accurate, relevant, and efficient assistance. This section contains a detailed template designed to help you compile and provide full project context to Claude. It's especially useful for:

* Onboarding the AI to a new or complex project
* Re-establishing context when starting new chat sessions
* Ensuring consistent understanding if multiple team members interact with the AI on the same project

The goal is to minimize repetitive explanations and enable Claude to act as a knowledgeable team member from the get-go by having well-documented context.

## How to Use This Template (`Claude.md`)

1. **Create a `Claude.md` File:** For your project, create a Markdown file (e.g., named `Claude.md`, `ProjectContext.md`, or similar)
2. **Fill Out the Template:** Copy the "Universal Project Context Prompt Template for Claude" below into your `Claude.md` file. Thoroughly fill out each section with the specific details of your project
3. **Keep it Updated:** Treat this `Claude.md` file as a living document. Update it as your project evolves (new technologies, architectural changes, major issues resolved/discovered)
4. **Provide Context to Claude:**
    * When starting a new chat or needing to ensure Claude has full context, you can copy and paste relevant sections, or the entire content of your filled-out `Claude.md`, into your conversation with Claude
    * You can also use it as your own reference to quickly answer Claude's questions about the project
5. **Iterate:** Based on your interactions with Claude, you might find additional points of context that are useful to add to your project's `Claude.md` file

## Universal Project Context Prompt Template for Claude

*(Copy the following into your project's `Claude.md` or similar context document and fill it out)*

---
Claude, to quickly re-establish full project context as if from a detailed `Claude.md` (like a previous session's output), I need you to understand the following key information areas. Please confirm, or I can provide details for each:

1. **Project Core & Status:**
    * Name, Primary Goal/Description
    * Context Version/Date (e.g., vYYYY-MM-DD)

2. **Tech Environment (Crucial: Specify Versions):**
    * Platform(s) (iOS, Web, Android, etc.)
    * Languages & Main Frameworks/SDKs
    * Key Libraries (and purpose)
    * Database(s), Auth/Payment Systems
    * Build Tools, IDE, Deployment Targets

3. **Coding Standards & Architecture:**
    * Code Style Guide(s) Used
    * Naming Conventions (brief examples)
    * Architectural Pattern(s) (MVVM, Clean Arch, etc.)
    * State Management, Dependency Manager, Testing Strategy

4. **Codebase Structure:**
    * Overview of Main Directory Layout
    * Key Files/Modules & Their Roles (Entry points, Config, Core Logic, Models, Services, UI, Utils - include paths if complex)

5. **Current Session Context:**
    * Brief Summary of Last Key Interaction/Problem
    * My Immediate Goal / What I Need Your Help With Now
    * Any Specific Questions I Have for You

6. **Active Issues & Challenges:**
    * Relevant Known Bugs or Current Technical Hurdles

7. **Essential Constraints & Preferences:**
    * Key Project Constraints (Performance, Accessibility, etc.)
    * Important 3rd-Party Service Details (if any)
    * My Preferences for your assistance style (if specific)

Goal: Rapidly bring you to full operational knowledge for project `[Your Project Nickname, e.g., NotepadClone2_iOS]`. Please indicate if you need elaboration on any of these points to proceed effectively.

**I. Project Initialization & Overview**
    A. `Project Name`: [User to fill: Official name of the project]
    B. `Project Nickname/Alias (for Claude)`: [Optional: A short name you'll use when talking to Claude about this project, e.g., "NotepadClone2_iOS"]
    C. `Project Description`: [User to fill: Brief overview, main purpose, core functionalities, and target users/audience]
    D. `Primary Contact/Developer (Your Name/Alias)`: [User to fill: e.g., "Ian"]
    E. `Context Version/Date`: [User to fill: e.g., vYYYY-MM-DD - Helps track context updates]

**II. Development Environment & Technology Stack**
    A. `Primary Platform(s)`: [User to fill: e.g., iOS, Android, Web (Frontend/Backend), Desktop macOS/Windows/Linux, API, etc.]
    B. `Core Programming Language(s)`: [User to fill: e.g., Swift, Kotlin, Java, Python, JavaScript, TypeScript, C#, Ruby, Go, PHP - **Specify versions if critical**]
    C. `Main Frameworks/SDKs/Engines`: [User to fill: e.g., SwiftUI, UIKit, Jetpack Compose, Android SDK, React, Angular, Vue.js, Node.js, Express.js, Django, Flask, Ruby on Rails, .NET, Spring Boot, Unity, Unreal Engine - **Specify versions if critical**]
    D. `Key Libraries (External/Third-Party & Purpose)`: [User to fill: List significant libraries and briefly what they are used for, e.g., Alamofire for networking, Redux for state management - **Specify versions if critical**]
    E. `Database(s) & ORM/ODM (if any)`: [User to fill: e.g., CoreData, SQLite, Realm, Supabase, PostgreSQL, MySQL, MongoDB, Firebase Firestore; SQLAlchemy, Prisma, Mongoose - **Specify versions if applicable**]
    F. `Authentication System (if any)`: [User to fill: e.g., Supabase Auth, Firebase Authentication, Auth0, Okta, custom JWT, OAuth providers used]
    G. `Payment System (if any)`: [User to fill: e.g., Stripe, PayPal, Braintree, Apple In-App Purchase, Google Play Billing]
    H. `Build System & Primary IDE/Editor`: [User to fill: e.g., Xcode, Android Studio, IntelliJ IDEA, VS Code, Gradle, Webpack, Vite, Maven - **Specify IDE/Build System versions if relevant**]
    I. `Version Control System & Hosting`: [User to fill: e.g., Git; GitHub, GitLab, Bitbucket]
    J. `Deployment Target(s) & Environment Info`: [User to fill: e.g., iOS 17.0+, Android API 26+, specific browser versions, Node.js v18+, server OS, Docker version]
    K. `Bundle Identifier / Package Name / Group ID (if applicable)`: [User to fill]
    L. `Relevant Team/Organization/Account IDs (if shareable and necessary)`: [User to fill]

**III. Coding Standards & Architectural Design**
    A. `Code Style Guide(s) Followed`: [User to fill: e.g., Apple's Swift API Design Guidelines, Google Java Style Guide, Airbnb JavaScript, PEP 8, project-specific guide link]
    B. `Naming Conventions (Examples)`: [User to fill: e.g., camelCase for functions/variables, PascalCase for classes/types, SCREAMING_SNAKE_CASE for constants]
    C. `Primary Architectural Pattern(s)`: [User to fill: e.g., MVVM, MVC, MVP, MVI, Clean Architecture, Microservices, Monolith, Layered Architecture, ECS (Entity Component System)]
    D. `State Management Approach (if applicable, esp. for UI apps)`: [User to fill: e.g., Redux, MobX, Zustand, Provider, Riverpod, Bloc, Jetpack Compose State, SwiftUI ObservableObjects/@State/@EnvironmentObject]
    E. `Dependency Manager(s) Used`: [User to fill: e.g., Swift Package Manager, CocoaPods, Carthage, Gradle, npm, yarn, pip, Poetry, Bundler, Maven]
    F. `Testing Framework(s) & Strategy`: [User to fill: e.g., XCTest, JUnit, Mockito, Espresso, Jest, React Testing Library, PyTest, RSpec; Focus on Unit/Integration/E2E testing, TDD/BDD approach?]

**IV. Project Structure & Key Files/Modules**
    A. `Directory Structure Overview`: [User to fill: Brief description of main source code folders and their organization, e.g., `src/features/`, `app/services/`, `lib/utils/`, `game/scenes/`]
    B. `Key File/Module Descriptions (and their paths if complex)`:
        1. `Application Entry Point(s)`: [User to fill: e.g., `main.swift`, `NotepadCloneApp.swift`, `MainActivity.kt`, `index.js`, `App.vue`, `Program.cs`, `manage.py`]
        2. `Core Application Logic/State (e.g., App Delegate, Global State Store)`: [User to fill: File(s) responsible for global state or core application lifecycle events]
        3. `Main Configuration Files (Project settings, manifests, environment)`: [User to fill: e.g., `Info.plist`, `AndroidManifest.xml`, `build.gradle`, `package.json`, `project.xcodeproj`, `.env` structure]
        4. `Key Data Models / Entities / Data Structures`: [User to fill: List important data models and their file locations/modules]
        5. `Core Services / Managers / API Clients`: [User to fill: e.g., `NetworkManager.swift`, `AuthService.ts`, `DatabaseHelper.java`, `PaymentProcessor.rb`]
        6. `Main UI Views / Screens / Components (if applicable)`: [User to fill: Key reusable UI elements or primary screens/views]
        7. `Important Utilities / Helpers / Shared Libraries`: [User to fill: Common utility functions/classes and their locations]

**V. Conversation & Immediate Task Context**
    A. `Summary of Last Interaction or Current Problem (if resuming)`: [User to fill: Briefly, what was the last thing discussed or the specific problem that led to providing this context?]
    B. `Current Goals / What I Need Help With Right Now`: [User to fill: What specific task(s) do you want Claude to assist with immediately?]
    C. `Specific Questions for Claude (if any)`: [User to fill: List any direct questions you have at this moment.]

**VI. Current Issues, Challenges & Known Bugs**
    A. `Active Bugs / Issues Being Tracked (relevant to current task)`: [User to fill: List critical or relevant problems that Claude should be aware of]
    B. `Key Technical Challenges or Design Hurdles`: [User to fill: e.g., "Optimizing real-time collaboration feature", "Integrating a complex third-party SDK", "Refactoring legacy module X"]
    C. `Known Technical Debt or Areas Slated for Future Improvement (optional)`: [User to fill]

**VII. Additional Notes, Constraints & Preferences**
    A. `Key Project Constraints or Requirements`: [User to fill: e.g., Strict performance targets, specific device compatibility, accessibility (WCAG) level, data privacy regulations (GDPR/CCPA), offline support]
    B. `Important Third-Party Service Integration Details (if not covered elsewhere)`: [User to fill: e.g., Specific API endpoints frequently used, unusual configurations for services like Firebase, AWS, Azure]
    C. `User Preferences for Claude's Assistance (if not covered by a general style guide)`: [User to fill: e.g., "Prefer concise code examples first, then explanation", "Avoid suggesting overly complex solutions for this MVP phase", "Focus on maintainability over raw performance unless specified"]
    D. `Any other information critical for Claude to understand this project context`: [User to fill: Anything else that doesn't fit above but is important]

---

# ⚙️ MCP Configuration Guide

## What is MCP?

Model Context Protocol (MCP) is a standardized way for Claude to interact with external tools and services. By configuring MCP servers and permission rules, you enable Claude Code to:

* Access your file system and repositories
* Execute development tools and commands
* Interact with databases, APIs, and services
* Manage your development workflow efficiently

## Prerequisites

* Claude Desktop application or Claude Code CLI
* Development environment with tools you want Claude to access

## Setting Up MCP Servers

### Available MCP Servers

Here are the essential MCP servers for development workflows:

* **applescript_execute** - Mac automation and system control
* **context7-mcp** - Enhanced context management  
* **desktop-commander** - File system operations and command execution
* **github** - GitHub repository management
* **image-viewer** - Image file handling
* **iterm-mcp** - Terminal integration
* **mcp-dockmaster** - Docker container management
* **moom** - Window management automation
* **notes** - Note-taking and documentation
* **openmemory** - Persistent memory across sessions
* **playwright** - Browser automation and testing
* **screenpipe** - Screen recording and analysis
* **screenshot** - Screenshot capture
* **taskmaster-ai** - Project and task management
* **wcgw** - Advanced shell operations
* **weather** - Weather data integration

### Installation

Most MCP servers can be installed via npm or pip. Check the specific server documentation for installation instructions.

## Configuring Permission Rules

### Essential File System Access

```bash
# Allow access to your main development directory
FileSystem(/Users/ian/Scripts/*)

# Or broader access if needed
FileSystem(/Users/ian/*)
```

### Git & Version Control

```bash
# Core Git operations
Bash(git *)

# GitHub CLI operations  
Bash(gh repo *)
Bash(gh pr *)
Bash(gh issue *)
```

### Development Tools

```bash
# Code editors
Bash(code *)

# Node.js ecosystem
Bash(npm *)
Bash(yarn *)
Bash(node *)

# Python development
Bash(python *)
Bash(pip *)
Bash(pipx *)

# iOS/Swift development
Bash(xcode-select *)
Bash(swift *)
Bash(swiftc *)
Bash(xcrun *)

# Container operations
Bash(docker *)
Bash(docker-compose *)

# Database tools
Bash(psql *)
Bash(sqlite3 *)

# Package management
Bash(brew *)

# System utilities
Bash(htop *)
Bash(nmap *)
Bash(grep *)

# Automation tools
Bash(ansible *)
Bash(ansible-playbook *)

# Media tools
Bash(obs *)
```

### Setting Up Permission Rules

1. **Open Claude Desktop/CLI**
2. **Navigate to Tools/Settings** 
3. **Add Permission Rules:**
   - Click "Add a new rule..."
   - Enter the rule (e.g., `FileSystem(/Users/ian/Scripts/*)`)
   - Set to "Allow"
   - Confirm

4. **Priority Order for Setup:**
   1. File system access to your repositories
   2. Git operations
   3. Your primary development language tools
   4. Package managers and build tools
   5. Additional utilities as needed

## Verification

After setup, verify your configuration:

```bash
# Check MCP server status
claude --mcp-debug

# Test file access
# Claude should be able to read/write files in permitted directories

# Test command execution
# Claude should be able to run permitted bash commands
```

## Security Considerations

* **Principle of Least Privilege** - Only grant access to directories and commands you actually need
* **Regular Audits** - Periodically review and update permission rules
* **Environment Separation** - Consider separate configurations for different projects
* **Backup Configurations** - Document your permission rules for easy restoration

## Troubleshooting

### Common Issues

1. **Permission Denied Errors**
   - Verify the exact path in your FileSystem rules
   - Check that directories exist and are accessible

2. **Command Not Found**
   - Ensure tools are installed and in your PATH
   - Add specific Bash rules for the commands you need

3. **MCP Server Failed to Connect**
   - Check server installation
   - Verify configuration files
   - Review logs with `--mcp-debug` flag

### Getting Help

* Check MCP server documentation
* Review Claude Desktop settings
* Use `claude --help` for CLI options
* Enable debug mode for detailed error logs

---

# 🎯 Why This Toolkit Matters for LLMs

Providing both comprehensive context and proper MCP configuration helps Large Language Models (LLMs) like Claude:

* **Reduce Ambiguity:** Specifics about your tech stack, architecture, and goals prevent generic or inapplicable advice
* **Improve Accuracy:** Correct version numbers and library details lead to more accurate code snippets and troubleshooting
* **Maintain Consistency:** Adherence to your project's coding standards and architectural patterns
* **Increase Efficiency:** Saves time by avoiding repetitive questions and clarifications from the AI
* **Enable Automation:** Direct access to your development environment for hands-on assistance
* **Enhance Collaboration:** Allows the AI to function more like a team member with persistent knowledge and tool access

By investing time in both context preparation and MCP configuration, you can significantly enhance the quality and relevance of the assistance you receive from Claude.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request with:

* Additional MCP server configurations
* Enhanced context template sections
* Real-world usage examples
* Documentation improvements

## License

This project is open source and available under the [MIT License](LICENSE).
