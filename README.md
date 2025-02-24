# Expo Linking.getInitialURL() Returns Null Inconsistently

This repository demonstrates a bug where `Linking.getInitialURL()` in Expo inconsistently returns `null`, even when a deep link is available.  The issue appears to be related to app state and background processes, making it difficult to reliably reproduce.

## Bug Description

The `Linking.getInitialURL()` method within the Expo SDK sometimes fails to retrieve the initial URL from a deep link, returning `null` instead of the expected URL string. This behavior is intermittent and dependent on factors that are not yet fully understood.

## Reproduction Steps

The exact steps to reproduce this bug are not consistent. However, the `bug.js` file contains example code that demonstrates the potential failure. To observe the issue, try opening a deep link to the app under various conditions (e.g., freshly launched, in the background, after a period of inactivity).

## Solution

The solution presented in `bugSolution.js` attempts to mitigate the issue by adding a small delay and multiple attempts using `setTimeout` to fetch the URL. This is not a guaranteed solution and further investigation into the underlying cause of the inconsistency is needed.  Consider using a more robust deep-link handling library if this issue proves persistent.