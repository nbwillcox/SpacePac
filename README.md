# SpacePac

A free, original neon maze chase with a head nod to the classic 80s arcade maze games. You steer a round little probe through glowing mazes, gobble every star-dust pellet, dodge four drones that each hunt you in their own way, and grab power cells to turn the tables. Warp tunnels wrap you from one side to the other, and bonus gems drop in for extra points.

**Play it in your browser:** https://nbwillcox.github.io/SpacePac/

Everything is generated in code: the mazes, hero, drones and gems are vector-drawn on the fly, and all sound effects are synthesized with the Web Audio API. There are no image or audio files and no build step. A sibling of [SpaceGalaShooter](https://github.com/nbwillcox/SpaceGalaShooter), [SpaceCentiShooter](https://github.com/nbwillcox/SpaceCentiShooter) and the rest of the series.

## Controls

| Action | Keys |
| --- | --- |
| Steer | `←` `↑` `↓` `→` or `W` `A` `S` `D` (or a gamepad d-pad / stick) |
| Pause | `P` or `Esc` |

The hero keeps moving until you steer. The direction you ask for is remembered and taken at the next turn, and a turn pressed just a hair too late still counts.

### On a phone or tablet

Play in portrait. Swipe anywhere on the screen to steer: the hero keeps moving until you swipe a new direction and takes the next turn you asked for. The pause button opens the menu. The on-screen controls appear on touch devices automatically; Settings has size, opacity and a left-handed layout. Use your browser's *Add to Home Screen* to install it as a full-screen app.

## Gameplay

- **Goal:** eat every pellet to clear the level. Each level is a new maze: two hand-drawn ones to start, then endless generated mazes, with five neon themes in rotation.
- **The drones** all hunt differently, so learn who is who:
  - **Stalker** (red) chases you directly and speeds up when few pellets are left.
  - **Ambusher** (pink) heads for the spot four tiles ahead of where you are going.
  - **Flanker** (cyan) aims for the mirror-opposite side of the maze, so it tends to come around the other way and pincer you.
  - **Wisp** (amber) is erratic: it wanders at junctions and backs off to its corner when you get close.
  The drones alternate between scattering to their corners and chasing, and they leave the hub one at a time.
- **Power cells** (the big glowing orbs in the corners) stun every drone for a few seconds, shorter on later levels. Eat stunned drones for 200, 400, 800 and 1600 points. An eaten drone flies home as a pair of eyes and comes back out.
- **Bonus gems** appear below the hub twice per level and are worth more each level: Crystal 100, Ring 300, Orb 500, Star 700, Comet 1000, Moon 2000, Sun 3000, Key 5000.
- **Warp tunnels** on the middle row wrap you to the other side; drones slow down inside them.
- **Lives and score:** you have 3 lives, and extra lives come at 10,000 and 50,000 points. Local top-10 high scores are kept in your browser.

## Run it locally

Open `index.html` in a browser, or serve the folder with any static server, for example `python -m http.server`. Test flags: `?level=N` starts on level N, `?god=1` makes the drones harmless, `?touch=1` forces the touch controls on a desktop.

## License

[CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/): free to play, share and remix for non-commercial use, with a link back to https://github.com/nbwillcox/SpacePac. SpacePac is an original game inspired by the arcade golden age; it uses no names, art, sounds or code from any commercial game.
