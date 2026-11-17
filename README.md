# Professional Skills Workshops: PSW 1 Dashboard

A lightweight facilitator dashboard for timing LEGO team builds in undergraduate engineering workshops. It supports three builds per workshop session, individual and group timers, results, progress comparisons, CSV export, and four separately saved workshop sessions.

## Start the dashboard

Open `index.html` in a modern browser. For a hosted copy, publish the repository root with GitHub Pages. The dashboard has no build step, package installation, or server-side database.

Use the gear button to set up the selected session:

1. Set the session name if you want a custom label.
2. Set **Number of teams** from 1 to 16. This controls the visible team timers. It works in Session 1 as well as Sessions 2–4. Changing the count keeps saved times and hidden teams; it does not delete them.
3. Optionally edit team names, one per line. The default roster is Team 1 through Team 16, with matching logos in `assets/teams/`.

The session selector stores each session separately. Team 4 in Session 1 and Team 4 in Session 2 are treated as different workshop teams. Whole Cohort Leaders compares completed teams across sessions and labels each result with its session.

## Run a workshop

1. Select the build with the Build One, Build Two, and Build Three controls.
2. Start teams individually or choose **Start All**. Stop a team to record its time, or pause and resume its timer. **Pause All** pauses active timers; **Resume All** continues them.
3. After a team submits, use **Continue** to unsubmit its time and restart its timer from that saved time. Use **Correct time** to edit the submitted result.
4. Choose **Submit All** to stop and submit every visible team timer. **Stop Build** ends the round and reveals the results. When all visible teams have submitted, results are revealed automatically. Use **Next Build** to continue.
5. The progression chart plots team times across all three builds. Click a team in the key to hide or show its line. Color and line patterns distinguish teams.

## Results and reset

- The round leaderboard supports paged and two-column compact layouts. Its Detail menu switches between seconds and milliseconds.
- The progression summary shows the fastest teams for each build and the most improved team. From Session 2 onward, Whole Cohort Leaders ranks teams by time saved from Build 1 to Build 3 across completed sessions.
- Choose **Export Session CSV** in the gear menu to download the selected session’s times in milliseconds, including best build and Build 1 to Build 3 improvement.
- **Reset Workshop Session** clears only the selected session. Export first if you need to keep its results.

## Where data is stored

Workshop data is stored in the browser’s `localStorage` on the facilitator’s device. It is not shared or synchronized across different browsers or devices. Clearing browser storage or using a different browser profile starts with a fresh dashboard. Export CSV files regularly to keep a copy of session results.
