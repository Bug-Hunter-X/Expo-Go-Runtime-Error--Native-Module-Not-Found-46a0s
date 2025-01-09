# Expo Go Runtime Error: Native Module Not Found

This repository demonstrates a common error encountered when developing Expo managed workflow projects that utilize third-party libraries with native module dependencies.  Expo Go, while convenient for development and testing, does not support native modules.  This results in a runtime crash when the app attempts to load the missing module.

## The Problem

The `bug.js` file showcases a simplified example that uses a hypothetical library (`react-native-unavailable-module`) which requires a native module.  When running this app in Expo Go, it will fail with an error indicating that the native module is not found.

## The Solution

To resolve this issue, consider using one of the following approaches:

1. **Use Expo's Managed Workflow with Libraries that Don't Require Native Modules:**  The easiest solution is to find alternative libraries that do not have dependencies on native modules. Expo's managed workflow is designed for ease of use and rapid development but has limitations regarding native modules.

2. **Use Expo's Bare Workflow:**  Expo's bare workflow allows you to have complete control over your project and integrate native modules seamlessly.  However, it comes with more setup complexity.

3. **Use EAS Build:**  Use EAS Build to build a standalone app with native modules. This allows you to test your app on physical devices or emulators but requires a build process.

The `bugSolution.js` file demonstrates how to adapt the code to avoid the native module dependency, thereby making it compatible with Expo Go.  Alternatively, instructions are provided to adapt to a bare workflow.