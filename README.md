# Node.js Intermittent Server Crash Bug

This repository demonstrates a bug where a Node.js server intermittently crashes due to unhandled exceptions.  The server generally functions correctly, but occasionally terminates without providing informative error messages.

## Bug Description

A seemingly simple HTTP server can unpredictably crash. The crashes appear random and lack sufficient logging to diagnose the root cause.  This makes debugging and resolving the issue difficult.

## Solution

The solution involves comprehensive error handling using a `try...catch` block within the request listener and improved logging of errors using `console.error` to capture relevant details during crashes.  This approach prevents the process from terminating unexpectedly and provides valuable debugging information.  Additional logging statements during normal operation can also help identify potential issues before they cause a crash.