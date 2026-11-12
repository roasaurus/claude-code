---
description: Find ad spend without sales or profit and propose pauses to the Actions inbox
argument-hint: "[7|14|30|90]"
---
Run the wasted-spend skill. Arguments: $ARGUMENTS

Read a number of days from the arguments (ignore them if the line above still shows a literal placeholder). Days must be
7, 14, 30 or 90 (with or without "d" or "days"); without days use 14. For any other number of days, reply only with the
valid options (7, 14, 30, 90) and stop: do not run it for another period.

List the candidates first. Propose pauses or lower budgets to the Actions inbox only for the ones I confirm; they wait
there for an owner or admin to approve. Nothing is applied directly.
