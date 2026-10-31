# 🏦 DBS Bank - Frontend React Interview Questions

Welcome to the DBS Bank Frontend Interview prep guide! This repository contains a curated list of real-world, architecture-level React coding challenges and questions asked during the DBS Bank technical rounds for Frontend Software Engineer roles.

Unlike standard LeetCode problems, these questions focus on practical implementation, security, and application architecture.

## 🚀 The Challenges

### 1️⃣ State Management Migration
**Scenario:** An application is currently using the standard React Context API (`useContext`), but it is experiencing performance issues.
**Task:** Explain the core purpose of `useContext`, its rendering bottlenecks, and write out the exact steps to migrate the application's state management from Context API to Redux Toolkit (RTK) without breaking existing components.

### 2️⃣ Secure React Routing
**Scenario:** A user clicks on an account card to view their transaction history.
**Task:** How do you pass sensitive parameters like an `accountId` to the Transaction History page without exposing it in the visible URL? 
*Hint: Implement this using React Router's `location.state`.*

### 3️⃣ Vite Build Security
**Scenario:** You are preparing a React application for production deployment.
**Task:** Write a `vite.config.ts` setup that completely disables source maps for production builds (so proprietary source code isn't exposed to the client) but keeps them active when running the local dev server.

### 4️⃣ API Payload Fallbacks
**Scenario:** The backend API contract occasionally changes without warning.
**Task:** How do you handle UI rendering safely when the backend sends an unexpected property name (e.g., sending `createdAt` instead of `transactionDate`)? Implement fallback logic to ensure the React component doesn't crash on `undefined`.

### 5️⃣ OTP Screen Implementation
**Scenario:** A secure transaction requires two-factor authentication.
**Task:** Build a fully functional 6-digit OTP (One-Time Password) input component from scratch. You must handle:
* Auto-focusing the next input box when a number is typed.
* Backspace shifting (moving focus to the previous box).
* Standard pasting of a full 6-digit code.
* A "resend code" countdown timer.

### 6️⃣ Session Persistence & Route Guards
**Scenario:** A user hard-refreshes the browser while on a protected dashboard page.
**Task:** Handle session persistence and private route redirection. Specifically, write the logic (e.g., using `PerformanceNavigationTiming` API) to detect a browser refresh and force a redirect to the login page if the user is unauthenticated.

### 7️⃣ Dynamic UI Styling
**Scenario:** A user's bank account can have a status of 'ACTIVE' or 'DORMANT'.
**Task:** Implement advanced conditional UI styling using `styled-components`. Dynamically disable an entire table row, modify the mouse cursor to `not-allowed`, fade the opacity, and block all nested action buttons strictly based on the 'DORMANT' account status.

### 8️⃣ Vulnerable Dependency Management
**Scenario:** A security scan flags an outdated version of `lodash` in your project.
**Task:** Explain and demonstrate the steps to safely manage and upgrade vulnerable project dependencies. How do you handle it if the vulnerability is in an *indirect* sub-dependency? (e.g., using npm `overrides` or yarn `resolutions`).

---

## 💡 How to Use This Guide

1. **Build a Sandbox:** Don't just answer these theoretically. Spin up a Vite + React + TypeScript project and build out each scenario.
2. **Focus on Edge Cases:** Banking apps require high reliability. Think about what happens if an API fails, a user pastes letters into the OTP box, or a token expires mid-session.
3. **Explain the "Why":** Interviewers at this level want to know *why* you chose a specific pattern (like Redux over Context) just as much as they want to see the working code.

Good luck with your interview preparation! 🚀