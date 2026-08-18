<div align="center">

# Noah Brauner

Computer Science and Economics, Harvard

Game theory, quantitative finance, and automated insulin delivery.

[Red/Black papers](https://github.com/SwiftlyNoah/redblack-research) &nbsp;·&nbsp;
[playredblack.com](https://playredblack.com) &nbsp;·&nbsp;
[LinkedIn](https://www.linkedin.com/in/noahbrauner/) &nbsp;·&nbsp;
[nbrauner@college.harvard.edu](mailto:nbrauner@college.harvard.edu)

</div>

---

## Red/Black: solving a hidden-information card game

*2026 · [four papers](https://github.com/SwiftlyNoah/redblack-research) · [play it](https://playredblack.com)*

Red/Black is a bluffing game on a 52-card deck where only color matters. I built
the game, then spent a summer trying to solve it, which meant pinning down how far
from optimal my best strategy is rather than training a bot that looks strong.

The game has **2.4 × 10³³ information sets**, enumerated exactly rather than
estimated, so it cannot be solved directly. Every route to an answer passes through
an abstraction, and an abstraction can quietly destroy the quantity you are trying
to measure. Most of the work is about preventing that.

Against the strongest best-response probe I could build, the final strategy measures
an exploitability lower bound of **−0.025, 95% CI [−0.044, −0.005]**, over 10,000
paired games on a payoff range of 2. The probe loses, so the bound is negative. That
says the probe ran out of room, not that the strategy is unbeatable. Its predecessor
measured +0.034 on identical seeds; the difference resolves at **p = 3 × 10⁻⁵**.

The result comes from splitting one job across two solvers. Subgame values need to be
unique and symmetric so that thousands of solutions compose without selection noise,
which a quantal-response ladder provides. Policies need sharpness, which CFR+ provides.
So values come from one solver, frozen, and policies from the other, re-solved against
them.

The flagship paper also documents the experiment that failed first. I removed a
provably-bad action from the solved game and expected an improvement. Exploitability
quadrupled. The strategy store doubles as the bot's model of its opponent, and a model
asserting an action is impossible breaks the moment a real opponent plays it. Pruning
your own play is defense. Pruning your model of the world is blindness.

---

## Reinforcement learning against a theorem prover

*2025–2026 · co-authored*

A closed-loop RL pipeline that fine-tunes Qwen3-8B against the Lean 4 compiler, using
compilation as an exact reward. There is no learned reward model, so there is nothing
to game.

GSM8K accuracy moved from **79.0% to 86.5%** (n = 200, p = 0.0046), with no measured
regression across five alignment and sycophancy benchmarks.

---

## Automated insulin delivery

I work on Loop, an automated insulin delivery system, and I use it myself.

At [the Tidepool Project](https://www.tidepool.org) I built features for Tidepool
Loop, which is FDA-approved. As an open-source contributor to DIY Loop I have shipped
changes used by more than 20,000 patients. This is most of my history on GitHub and it
is the work I would defend hardest: it made my own type 1 diabetes easier to carry, and
it is the clearest case I know of code mattering to people who will never read it.

Commits: [tidepool-org/Loop](https://github.com/tidepool-org/Loop/commits/dev/?author=SwiftlyNoah)
&nbsp;·&nbsp; [LoopKit/Loop](https://github.com/LoopKit/Loop/commits/dev/?author=SwiftlyNoah)
&nbsp;·&nbsp; [LoopKit/LoopKit](https://github.com/LoopKit/LoopKit/commits/dev/?author=SwiftlyNoah)

---

## Selected work

| | |
|:--|:--|
| [**PikesvilleOpportunity**](https://github.com/SwiftlyNoah/PikesvilleOpportunity) | Econometrics paper on opportunity and place, written for Ec 50 |
| [**NoahCoin**](https://github.com/SwiftlyNoah/NoahCoin) | An ECDSA-signed cryptocurrency and backend server, written from scratch in Python |
| [**ActivityDetector**](https://github.com/SwiftlyNoah/ActivityDetector) | Classifies movement type from iPhone motion data, with a neural net tuned across layer counts, widths, and temporal input strategies |
| [**TidemanVisualizer**](https://github.com/SwiftlyNoah/TidemanVisualizer) | Visualizes the Tideman ranked-pairs voting method |
| [**CapstoneMachineLearning**](https://github.com/SwiftlyNoah/CapstoneMachineLearning) | Pneumonia classification from chest radiographs, deployed on-device with CoreML |
| [**HideAndCSeek50**](https://github.com/SwiftlyNoah/HideAndCSeek50) | A geolocation hide-and-seek game, inspired by *Jet Lag: The Game* |
| [**TheCrimsonApp**](https://github.com/SwiftlyNoah/TheCrimsonApp) | An iOS article reader for thecrimson.com |

---

## Shipped

Apps published by Noble and Greenough School and Appier LLC, written by me and free to
download. Together they have passed **8,000 downloads and 2 million sessions**, with
hundreds of daily active users.

[Nobles 2.0](https://apps.apple.com/us/app/nobles-2-0/id1597945731), a platform for
students and teachers &nbsp;·&nbsp;
[Happiness Hacker](https://apps.apple.com/us/app/happiness-hacker/id6469530403), a daily
journal and mood tracker &nbsp;·&nbsp;
[Know Me](https://apps.apple.com/us/app/know-me-quiz-your-friends/id1526856498), a game
about how well your friends know you

Also in production: [the Nobles clubs directory](https://nobilis.nobles.edu/clubs), a Vue
app for student organizations.

---

<div align="center">

`Python` &nbsp;·&nbsp; `C` &nbsp;·&nbsp; `SQL` &nbsp;·&nbsp; `TypeScript` &nbsp;·&nbsp; `Swift`

CFR and CFR+ &nbsp;·&nbsp; equilibrium computation &nbsp;·&nbsp; Monte Carlo &nbsp;·&nbsp;
statistical inference &nbsp;·&nbsp; distributed compute

</div>
