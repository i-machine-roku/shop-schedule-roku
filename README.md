# shop-schedule-roku

**Status: idea, not started.**

Planned native Roku (BrightScript/SceneGraph) port of [`shop-schedule`](https://github.com/i-machine-things/shop-schedule) — currently a Raspberry Pi kiosk that polls Gmail for the Foreman Report PDF, parses it, and displays `schedule.html` on a shop floor display.

Rationale: a Roku is cheaper, quieter, and more reliable than a Pi for a static wall-mounted display, and can be distributed as a private channel (see [`seerr-roku`](https://github.com/i-machine-roku/seerr-roku) for the reference implementation/CI pattern).

Not scaffolded yet — will need to read `shop-schedule`'s actual README/CLAUDE.md first to understand the real parsing/polling logic before porting anything.
