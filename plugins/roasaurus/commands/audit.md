---
description: Audit the store's ad accounts and rank fixes by measured profit
argument-hint: "[platform] [7|14|30|90]"
---
Run the ads-audit skill for this store. Arguments: $ARGUMENTS

Read a platform name and a number of days from the arguments (ignore them if the line above still shows a literal
placeholder). Days must be 7, 14, 30 or 90 (with or without "d" or "days"); without days use 30. For any other number of
days, reply only with the valid options (7, 14, 30, 90) and stop: do not run the audit for another period.

Report the findings ranked by measured profit over the period. Propose changes only when I ask for them.
