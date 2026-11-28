# Be the Scheduler

The game from our mini lecture SW3, used in [1.2 Operating Systems, Section 8](../../content/Part_1/02_Operating_Systems.md#activity-be-the-scheduler).

## How to open it

* **Offline:** double-click `index.html`. It opens in any web browser (Chrome, Edge, Firefox, Safari) and needs no installation, account or internet connection. It uses only the fonts already on your computer.
* **Online (optional):** <https://schedulercpu.netlify.app>

## What to do

1. Pick a scheduling method (First Come First Served or Round Robin) and watch processes A = 3, B = 2 and C = 1 share one CPU core.
2. Before each run, predict when each process finishes. Then check.
3. Try scheduling the jobs yourself in the shortest-job-first order and compare the waiting times.

## Expected results

| Method | Order on the CPU | C finishes at | Average finish time (shown in the game) | Average waiting time (used in 1.2) |
| :--- | :--- | :--- | :--- | :--- |
| First Come First Served | A A A B B C | 6 | 4.67 | 2.67 |
| Round Robin, 1-unit slice | A B C A B A | 3 | 4.67 | 2.67 |
| Shortest Job First | C B B A A A | 1 | 3.33 | 1.33 |

The game shows the average **finish** time; Section 1.2 uses the average **waiting** time. For each job, waiting time = finish time − the CPU time it needs, so both tell the same story.

## No computer?

Use the paper version in [1.2 Operating Systems, Section 8](../../content/Part_1/02_Operating_Systems.md#activity-be-the-scheduler). It has the same questions and the answers.
