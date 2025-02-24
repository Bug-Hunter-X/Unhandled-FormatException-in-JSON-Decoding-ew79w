# Unhandled FormatException in JSON Decoding

This repository demonstrates a common error in Dart applications involving JSON decoding and provides a solution.

The `bug.dart` file showcases code that fails to handle a `FormatException` that can occur when `jsonDecode` encounters invalid JSON data.  The `bugSolution.dart` demonstrates a robust approach that gracefully handles this potential error.

## Problem

The original code doesn't properly catch the `FormatException` thrown by `jsonDecode` if the server returns an unexpected response or malformed JSON.  This can lead to app crashes.

## Solution

The solution involves using a `try-catch` block to explicitly handle the `FormatException`.  This allows for graceful error handling, preventing app crashes and providing better user experience.  The solution also includes more robust error handling for HTTP status codes and other potential issues.