# Game Build Sprint

A browser-based software development activity for A-level (Year 12/13) students. Teams build a Rock Paper Scissors game one function at a time, using code blocks or Python, then compare each function with code written by an AI.

Nothing needs to be installed and no logins are required. It runs on school PCs, laptops and Chromebooks.

## What students do

The class plays the part of developers at a small games studio. The game is split into six tickets. For each one, a team writes a single function, runs automatic tests, and sees that part of their game switch on.

| Stage | Function | Software development idea |
|---|---|---|
| 1. Who beats who? | `beats(a, b)` | Turning a specification into code |
| 2. Decide the round | `round_result(player, computer)` | Reusing tested functions |
| 3. Understand what players type | `clean_move(text)` | Input validation |
| 4. Who wins the match? | `match_winner(player_score, computer_score, best_of)` | Edge cases and testing |
| 5. Feature request: Lizard and Spock | `beats(a, b)` updated | Changing code and maintainability |
| 6. Build the computer opponent | `choose_move(history)` | A simple AI strategy, tested in a tournament against five bots |

**Code blocks or Python.** Teams can snap blocks together (with a live view of the Python they create) or type Python. They can switch at any time, and convert blocks into Python.

**Compare with AI.** After passing a stage, teams ask an AI to write the same function, run the AI's code through the same tests, see both versions side by side, and record a verdict. There are two ways to do this:

- **Use a chatbot.** Students use any chatbot their school allows in another tab and paste its code in.
- **Simulated assistant.** "Pixel" is a pretend AI with prepared answers, selected by default for schools where chatbots are blocked. Like a real AI it makes realistic mistakes and explains its code confidently either way. A vague prompt gets clearly flawed code, and even a detailed prompt usually gets a subtle bug first, such as an off-by-one error, swapped player and computer, or a capital letter that breaks the specification. When students tell Pixel what went wrong, it corrects itself. After each test, the page explains what went wrong, so students see why human developers still need to check AI-written code.

**Play the game.** The game panel uses the team's own functions, so it grows as they work: results, typed moves, best-of matches, lizard and Spock, and finally playing against their own strategy.

At the end, teams get a score breakdown, a code for the leaderboard, and can download their finished game as a Python file to run at home.

## Running a session

- **Audience:** Year 12/13 students or equivalent.
- **Group size:** 30–60 students in teams of 3–5.
- **Time:** about 60 minutes: 7-minute brief, about 43 minutes of sprint time, and a debrief.
- **Equipment:** one laptop per team and a projector for the facilitator.
- **Network:** the page loads Python (Pyodide), Blockly and CodeMirror from `cdn.jsdelivr.net` and `cdnjs.cloudflare.com`. Test it on the school's network beforehand.

## Links

- Students: the GitHub Pages URL for this repository.
- Facilitator: the same URL with `facilitator.html` added to the end. It has the countdown, leaderboard, run sheet, debrief prompts, troubleshooting tips and model solutions.

## Scoring

- Stages 1–5: 100 points each.
- Stage 6: 60 points, plus 10 for each of the five bots beaten. Beating 3 passes the stage.
- Each hint: −15 points.
- AI comparison with a verdict: +25 points per stage.

## Notes

- All code runs in the student's browser. No personal data is collected, and progress is saved only on that device.
- The leaderboard code is tied to the team name and score. It discourages casual cheating but isn't secure.
- University details, links, points and the option to allow AI comparison before a stage is passed are in the `CONFIG` block near the top of the script in `index.html`. The countdown length is in `facilitator.html`. If you change `CODE_SECRET`, change it in both files.

## Contact

[School of Computing and Engineering, University of Bradford](https://www.bradford.ac.uk/undergraduate/subjects/computing)
