# Game Bible: Wasteland Restoration (working title)

Nov 23, 2026 · @Liam

## Pitch and pillars

A first-person survival and automation game in which a human wakes in a sealed rover on a toxic, colourless wasteland and slowly cleans it up, building ever larger machines until nature can return.

- **Inspirations:** WALL-E (a lonely, cluttered world still beautiful and being cleaned up), Fallout (a wasteland that is beautiful despite itself), Subnautica (creature style, not horror).
- **Pillar 1, beauty at every stage:** the player should think "I love this" and "I can't wait to change it" at the same time, from the grey start to the regrown end.
- **Pillar 2, impatience drives progress:** doing it by hand is too slow, and that frustration pushes the player to automate.
- **Pillar 3, colour is earned:** the world begins colourless, so the first sight of green is a milestone.
- **Perspective:** first person.

## Core loop

Venture out, gather, return to the rover to process, get loot, automate a little more, and go out again further.

1. **Venture:** short trips into the wasteland, limited by toxic air and the respirator.
2. **Gather:** collect sand, dirt and scrap, and find story fragments.
3. **Process:** the rover's macerator turns scrap into random loot: refined materials, seeds or tech scrap.
4. **Automate:** each unlock removes a chore and extends the next trip.
5. **Repeat,** going further and restoring more.

**Early automation path**

- Input and output buffer chests on the macerator, so it works through a queue while the player is out.
- Digging down through sand, dirt and sludge until harder material appears that can't be processed yet.
- The first fully autonomous line: a vacuum hoover on a flexible pipe that sucks sand into a tank or machine.
- Getting the robot to work for the player.

**Open:** whether the rover can craft, and what comes after the first line.

## Player, robot and co-op

The player is a human woken by the rover's alarm when their life-preservation pod fails, and the robot is their first friend.

- **The player:** wakes knowing why from the atmosphere alone. They slowly learn their purpose and the land's history from fragments and from the robot.
- **The robot:** starts broken, and the player fixes it. It is an interactive AI in the style of the Verity mod for Minecraft, with a funny personality. Commands must be precise, and vague commands lead to funny outcomes. The player gets it working early on.
- **Co-op:** friends sleep in other chambers in the rover. How death, shared inventory and the robot work in co-op is still open.
- **Build note:** a small command system of verbs, targets and quantities is the cheaper way to get the vague-command comedy than free-text AI.

## The rover

The rover is a sealed, tracked vehicle, possibly an old work vehicle built to carry people, and it is the player's home, processing base and air supply until they are established.

- Houses the pods, including friends' chambers for co-op.
- Holds the macerator and processor.
- Refills the player's respirator.
- Ramp door with hydraulics: lowering it is the player's first view of the world.

## Danger and gating

Early trips are short because the world is hostile, and each hazard later turns into an unlock or a resource.

| Hazard          | Effect                                                  | Later                                                  |
| --------------- | ------------------------------------------------------- | ------------------------------------------------------ |
| Toxic air       | Respirator needed, refilled from the rover's air system | Sets early trip length                                 |
| Electro storms  | Weather events the player must wait out                 | Power generation                                       |
| Radiation zones | Block exploration until later                           | Power generation                                       |
| Mobs            | Subnautica-style creatures, not horror                  | Part of the ecosystem                                  |
| Terrain hazards | Deep trenches and similar                               | Introduced only once the player can recover their body |

**Death and recovery**

- Staying out too long before the player has extended travel kills them, and their inventory stays on the body.
- To retrieve it, wait for the weather event to pass.
- For a radiation death, use a grappling hook or a consumable that gives brief radiation protection.
- World design must be planned so players can always get back to their body.

## Goal, world and tone

The goal is to restore the playable world and reintroduce nature; the player never preserves the trashed land.

- **First moment:** the ramp lowers on its hydraulics onto derelict, eroding towers and thick wind carrying dirt and debris. The world lacks colour but is beautiful in its own way, and it should make the player say "wow" and "I can't wait to get rid of it".
- **Storytelling:** atmosphere, a radio station or recording that doesn't match the real date (a clue to the long sleep), fragments in the wasteland, and the robot.
- **Nature as milestone:** seeds appear in loot from early on, and the first green, plant or wildlife is a major moment.
- **Open:** whether there is a definite ending or the world stays open.

## First 30 minutes (demo target)

This sequence is the target for a first playable demo.

1. Wake up. The pod failure is understood instantly from the atmosphere and alarm.
2. Explore the rover and find the subtle clue of a long sleep: a radio station or recording that disagrees with the reported date.
3. Fix the robot and loot the medkit.
4. Lower the ramp and see the wasteland for the first time.
5. Collect sand and dirt, salvage scrap, and talk to the robot for advice, the old world and the player's purpose.
6. Return to the rover and process materials, receiving random loot (refined materials, seeds, tech scrap).
7. Realise it will take a while, build the buffer chests, and keep digging and farming. Notice the hole being dug, and possibly harder material beneath that can't be processed yet.
8. Befriend the robot and learn to put it to work.

## What makes it fun

The stories players tell should come from progress they earned and surprises they didn't expect.

- **The top moment:** seeing green for the first time, or introducing nature and wildlife.
- Finally reaching dirt, so other materials can be processed.
- A lucky, logical processor drop from scrap (random) that unlocks the next step in automation.
- Setting up the first fully autonomous line, with the vacuum hoover and flexible pipe filling a tank.
- The robot's funny misunderstandings when a command isn't precise, and a growing friendship.
- Visibly healing a world that was beautiful at every stage.

## Visual style and development

The engine is undecided between Godot and Unreal, and a time-boxed test scene will decide it.

- **Style:** stylized, not photorealistic, but it must deliver beautiful scenery. Strong silhouettes, fog, wind-blown particles, lighting, colour grading and sound carry the look.
- **Engine:** Unity is ruled out because of its past pricing model. Unreal's main advantages (Nanite, Lumen, World Partition) matter most for photorealism and huge worlds; Godot is generally the default for stylized 3D by a solo developer, though very large worlds need workarounds. A custom Rust engine is parked for now.
- **Team:** solo developer, possibly with friends who enjoy map making helping with world design.
- **Platform and scope:** not yet decided.

## Next step: engine test, and open questions

The next step is a one to two week test that builds the same scene in Godot and Unreal and picks the engine that gets to "wow" faster.

**The test scene:** the rover's ramp lowering onto a windy, colourless wasteland (the first-30-minutes step 4), seen in first person.

- ☐ Rover interior and ramp door with hydraulic animation
- ☐ Distant eroding towers with silhouettes against haze
- ☐ Wind-blown dirt and debris particles
- ☐ Fog and atmospheric lighting, with colour grading
- ☐ A small patch of rubble and scrap with a pickup
- ☐ First-person movement at a stable frame rate on your PC

**How to decide:** after each engine, record the time spent and judge how good it looks, how easy it was to work in, and the frame rate. Choose the engine that looks closest to your vision with the least fighting. Stop at the time limit, even if neither is finished.

**Still open**

- How co-op works, and what happens to the robot and to death in co-op.
- Whether the rover can craft, and the later automation steps.
- The end state, platform, scope and a working title.