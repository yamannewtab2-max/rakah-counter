# Rak‘ah

A single-purpose Rak‘ah counter: it exists so you never lose track of which Rak‘ah you are on.

One self-contained `index.html`. No build step, no dependencies, no network calls — open it and it works (offline too).

## How it works

**Setup** — tap a prayer name to include or skip it, use `−` / `+` to set how many times it repeats (hold to speed up), pick the rest between prayers, press **Start**.

**Counter** — the whole screen is the button. Two numbers only:

```
0        Rak‘ahs completed so far (starts at 0)
25       seconds left on double-tap protection
```

- One tap per Rak‘ah — tap as you finish one, the top number goes up by one (0 → 1 → 2 …).
- Tapping after the last Rak‘ah ends the prayer.
- A tap is only accepted 25 seconds after the previous one (protection against tapping twice by accident).
- The background shifts a calm shade per Rak‘ah as a second memory cue.
- After each prayer: a full-screen rest countdown (e.g. `300`), then the next prayer starts by itself.
- Hold the screen for 1.2 s to leave the counter.

State is kept in `localStorage` and all timers are timestamp-based, so locking the phone, backgrounding the app or reloading resumes exactly where you were.
