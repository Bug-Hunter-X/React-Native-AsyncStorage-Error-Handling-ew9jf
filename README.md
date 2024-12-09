# React Native AsyncStorage Error Handling Bug

This repository demonstrates a common bug in React Native applications involving AsyncStorage and its solution.  The bug occurs due to a lack of proper error handling when using AsyncStorage's asynchronous methods, `setItem` and `getItem`.  Without error handling, unexpected behavior or app crashes can occur under various circumstances such as storage limitations or I/O issues.  The solution demonstrates best practices for robust error handling, preventing unexpected application termination.

## Bug
The initial code lacks `.catch` blocks for error handling in AsyncStorage operations. This leaves the application vulnerable to crashes or unexpected behavior when storage operations fail.

## Solution
The solution includes `.catch` blocks to handle potential errors gracefully.  This ensures that the application remains responsive and provides informative feedback to the user even when AsyncStorage operations fail.  Proper logging is also introduced to aid in debugging.