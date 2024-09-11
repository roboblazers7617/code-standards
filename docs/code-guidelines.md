---
layout: default
title: Code Guidelines
---

# Don’t change behavior depending on environment

Methods like `isFMSConnected()` SHOULD NOT be used to ensure that code behavior is consistent when practicing and on the field.

# Avoid magic numbers

Constants such as motor speeds and sequence delays MUST be exposed in the constants file.
