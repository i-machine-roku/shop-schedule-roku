# shop-schedule-roku

**Status: idea, not started.**

Planned native Roku (BrightScript/SceneGraph) port of [`shop-schedule`](https://github.com/i-machine-things/shop-schedule) — currently a Raspberry Pi kiosk that polls Gmail for the Foreman Report PDF, parses it, and displays `schedule.html` on a shop floor display.

Rationale: a Roku is cheaper, quieter, and more reliable than a Pi for a static wall-mounted display, and can be distributed as a private channel (see [`seerr-roku`](https://github.com/i-machine-roku/seerr-roku) for the reference implementation/CI pattern).

Not scaffolded yet — will need to read `shop-schedule`'s actual README/CLAUDE.md first to understand the real parsing/polling logic before porting anything.

## Cross-reference: `shop-schedule`

This repo is the Roku counterpart to [`shop-schedule`](https://github.com/i-machine-things/shop-schedule). The two projects share the same data source and the same display goal, so keep them in step:

| Concern | Source of truth (`shop-schedule`) | Roku port (this repo) |
|---------|-----------------------------------|-----------------------|
| Foreman's Report intake (Gmail poll, SMB/web drop) | [`update_schedule.py`](https://github.com/i-machine-things/shop-schedule/blob/master/update_schedule.py), [`process_drop.py`](https://github.com/i-machine-things/shop-schedule/blob/master/process_drop.py) | Not started |
| PDF parsing and work-centre grouping | [`update_schedule.py`](https://github.com/i-machine-things/shop-schedule/blob/master/update_schedule.py) | Not started |
| Work-centre sidebar filter | [README: Work center filter](https://github.com/i-machine-things/shop-schedule#work-center-filter) | Not started |
| Auto-scroll schedule and overdue highlighting | [README: Display](https://github.com/i-machine-things/shop-schedule#display), [`public/kiosk.html`](https://github.com/i-machine-things/shop-schedule/blob/master/public/kiosk.html) | Not started |
| Page rotation between display pages | [README: Page rotation](https://github.com/i-machine-things/shop-schedule#page-rotation), [`pages.json.example`](https://github.com/i-machine-things/shop-schedule/blob/master/pages.json.example) | Not started |

When porting a behaviour, link the matching `shop-schedule` file or README section in the PR description. If the source changes its report format or config keys, update the table above and the port together.

`shop-schedule` links back to this repo from its README.
