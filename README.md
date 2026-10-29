# Ant Manor

A phone-portrait 2D browser prototype: the Swarm Siege mechanic in a dollhouse cutaway.

Tap a room to throw a glass ball of ants. It shatters against the back wall and the ants drop to the nearest floor, then crawl along floors, up walls, across ceilings, over furniture and up the stairs and ladders. A swarm eats any food at or below its size, every bite flies to the colony, and the colony hatches new ants into the next ball. Swarms that meet merge, and a swarm with nothing in reach slowly widens its search. Ants only live about 20 seconds once they land. Eat the red objectives before the clock runs out.
- **Level 1, Tea Party (noon):** Pie (10 ants), Cake (22)
- **Level 2, Sweet Shop (sunset):** Sundae (14), Macaron tower (22), Gingerbread house (30)
- **Level 3, Midnight Feast (night):** Jelly (16), Roast (28), Cheese wheel (32)

The tuning panel (beside the game on desktop, behind the sliders button on a phone) changes the clock, hatch cost, bite rate, crawl speed, sight range, lifespan, starting ants and size gates. Press R to restart.

## Version 1

A rules variant lives at [/v1/](https://keremreboot.github.io/ant-manor/v1/), with the same houses and food:
- Ants never die, so a swarm that runs out of food goes looking for more.
- Any swarm can eat any food. More ants eat it faster.
- Every food is worth a set number of eggs, laid in batches at checkpoints as it is eaten. Eggs fly to the colony and hatch into the next ball.
- Nothing is written on the food. The objective chips at the top show how much of each objective has been eaten.
- The clocks are 70, 75 and 80 seconds.

Its tuning panel adds bite speed, egg value and the number of egg checkpoints. Its settings are saved separately from the original.

Everything is in `index.html` (and `v1/index.html`); the only outside requests are Google Fonts. `window.antManor` exposes the state and an `advance(seconds)` step for balance experiments from the console.
