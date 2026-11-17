# Build Better workshop dashboard

A static, browser based dashboard for timing and reviewing three LEGO build rounds in a professional skills workshop.

## Run locally

Open `index.html` in a browser, or serve this directory with any static web server. The app has no package dependencies or build step. For GitHub Pages, publish the repository root from the `main` branch.

## Workshop workflow

1. Open the gear menu, set an admin password (at least 6 characters), add a session name, and enter one team per line.
2. Select a team, start the team timers individually or together with **START ALL**. Use **STOP** to pause one timer, edit its time, then **RESUME** or submit. **PAUSE ALL** pauses every running timer. Use manual time entry if a result needs recording without the stopwatch.
3. Results are revealed automatically once all teams submit, or use **STOP BUILD** to lock the round and reveal submitted results.
4. Select Builds 2 and 3 in the progress bar and repeat. The chart shows each team's time trend; the summary reports the fastest recorded build and the greatest Build 1 to Build 3 improvement.
5. Export CSV from admin controls, then reset the dashboard before the next workshop session.

## Data and deployment notes

Session data and the admin password are stored in the current browser's `localStorage`. This is a single-browser facilitator tool: data is not shared with participants' separate devices, synced to a server, or protected against someone with browser developer tools. The dashboard is intended for staff on the facilitator device; it has no password prompt. For the requested team selection from each team's own device with a shared live leaderboard, a backend service and real administrator authentication are needed. Keep this browser open during the session and export before clearing storage.

The supplied logos are stored in `assets/teams/` and displayed for the matching `Team 1` through `Team 16` names. The default roster includes all 16 teams. The archive contained both `Team 8.png` and `Team 8 V2.png`; the dashboard uses the explicitly versioned `Team 8 V2.png`. To use a logo for a renamed team, preserve the matching `assets/teams/team-N.png` filename or update the image mapping in `app.js`.
