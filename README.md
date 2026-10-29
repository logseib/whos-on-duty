# Who's on duty?

Small static site showing which TAA dean is on duty tonight in the boys' and girls' dorms. Duty day runs 7:00 AM to 7:00 AM, Phoenix time.

- `index.html` - the whole app (no build step).
- `data/schedule.json` - semester schedule: per-dorm date ranges (`schedule`) plus dated `exceptions` (breaks, trips, special coverage). Exceptions win over the schedule.
- `data/overrides.json` - optional file-based overrides (same shape as live ones). Live overrides made from the site's button win over this file.
- `data/config.json` - where live overrides are stored. The write key inside is encrypted with the deans' PIN.
- `img/` - dean photos (from the public Thunderbird Adventist Academy staff page).

Order of precedence for a given dorm and day: live override, then `overrides.json`, then `exceptions`, then `schedule`.

Each new semester: replace `schedule` and `exceptions` in `data/schedule.json`.
