# Sentry Setup Guide

This guide covers the necessary steps to initialize Sentry for error tracking and user feedback in our project.

## 1. Account & Project Creation
1. Go to [sentry.io](https://sentry.io/) and create an account (or log in).
2. Create a new **Project** and select your platform (e.g., React, Vanilla JS, or Node.js depending on the stack).
3. Copy the **DSN** (Data Source Name) provided after project creation.

## 2. Installation
Depending on your package manager, install the Sentry SDK. For example, in a React/JS environment:
```bash
npm install @sentry/browser @sentry/tracing
# OR
npm install @sentry/react
```

## 3. Initialization
In your application's entry point (e.g., `main.js`, `index.js`, or `App.jsx`), initialize Sentry with your DSN:

```javascript
import * as Sentry from "@sentry/browser"; // or @sentry/react

Sentry.init({
  dsn: "YOUR_SENTRY_DSN_HERE",
  
  // Set tracesSampleRate to 1.0 to capture 100% of transactions for performance monitoring
  tracesSampleRate: 1.0,

  // Additional configuration for feedback or session replays can be added here
});
```

## 4. User Feedback Setup
To implement user feedback loops (like a crash report dialog):
```javascript
try {
  // Your code...
} catch (error) {
  Sentry.captureException(error);
  // Show the feedback dialog
  Sentry.showReportDialog({ eventId: Sentry.lastEventId() });
}
```
*Note: Ensure to verify your setup in the Sentry dashboard by triggering a test error.*
