---
layout: default
title: Formatting Rules
parent: Style Guide
---

# Formatting Rules

In general, most code MAY be formatted according to the formatter settings files in the git repository. The style that defines those files is defined in this section, and MUST be followed.

# Indentation

* Tabs MUST be used for indentation wherever possible. The only exception to this is when the usage of tabs will break functionality, in which case spaces MAY be used.
* Continuation lines MUST be indented twice.

# Line wrap

* Lines SHOULD NOT be truncated simply because they are too long
* Long lines SHOULD be split up where it makes sense (for example, long sequences of chained methods and long arrays should be split up over multiple lines)
* In wrapped arrays, the last item MUST have a separator appended to it to reduce the size of git diffs and make merges easier

# End-of-line characters

* A single linefeed character MUST be used for newlines.
* A newline MUST be inserted at the end of every file.

# Trailing whitespace

* Lines MUST NOT have any trailing whitespace characters immediately before the newline character.

# Annotations

* Empty lines MUST NOT be present between annotations and the declarations they affect.
