# Cooking course in Cooklang

Learn basic cooking technique by cooking dishes.

Each lesson is one recipe in [Cooklang](https://cooklang.org), a plain-text recipe format.
The steps cook the dish. The notes between the steps explain the technique: why the pan
starts cold, why the mushrooms get a splash of water first, why a steak rests.
After a lesson you should be able to cook the dish again without the recipe.

The course is for people who already cook from recipes and want to know why the steps work.

## Status

**Module 1 is in draft.** Its four lessons are written and nobody has cooked them yet:
the amounts and times are untested, and the lessons have no photos or video links. Each
lesson's front matter shows its `status`, and a lesson is marked `tested` only after people
have cooked it and reported back. Modules 2 to 5 are not written.

## Syllabus

Five modules, four lessons each. The modules do not depend on each other. The last lesson
of each module combines what the module taught and is written as ratios, so you fill in
the amounts.

This is the planned list. Dishes may change as lessons are tested.

| Module | Lessons |
|---|---|
| 1 · Heat in a pan | Crispy chicken thighs (rendering fat) · Mushrooms on toast (water before browning) · Steak with pan sauce (searing, deglazing, resting) · Any-vegetable stir-fry |
| 2 · The oven | Tray of roast vegetables (spacing) · Roast chicken (dry brine, carryover cooking) · Slow-baked salmon (doneness by temperature) · Sheet-pan dinner |
| 3 · Wet heat | Tomato soup (sweating, simmer vs boil) · Poached chicken and stock (gelatin) · Beef stew (braising) · Any-bean soup |
| 4 · Eggs and emulsions | French omelette (how egg sets) · Vinaigrette (emulsion ratio) · Mayonnaise (and fixing a broken one) · Carbonara |
| 5 · Starch | Rice pilaf (absorption) · Pasta finished in the pan (pasta water) · Mashed potatoes (waxy vs floury) · Fried rice |

## How a lesson is written

A lesson is a `.cook` file, numbered within its module, with a photo of the same name
next to it:

```
1 Heat in a pan/
  1 Crispy chicken thighs.cook
  1 Crispy chicken thighs.jpg
```

Inside the file:

- **Steps** say what to do and what to look for ("until the skin releases on its own").
- **Notes** (lines that start with `>`) say why. They carry a label: `Technique:`, `Why:`,
  `If it goes wrong:`, `Safety:`, `Watch:`, `Next time:`.
- A `Watch:` note links a short video of the one moment that is hard to describe in words.
- The last lesson of a module names its ingredients as slots (`protein`, `hard vegetables`)
  with the choices in brackets, so the amounts still scale and still make a shopping list.
- The front matter records the lesson number, the technique and the lesson's `status`:
  `draft`, `testing` or `tested`.
- Every claim about why something works has a source, kept in a `--` comment beside the
  note that makes it.

## Using the course

Download or clone this repository and open the folder in a Cooklang app: the
[Cook apps](https://cooklang.org/app/), the desktop editor, or
[CookCLI](https://cooklang.org/cli/) (`cook server` in the folder gives you a web view).

One thing to know: the apps show notes in the recipe view, but cook mode (one step per
screen) does not show them yet. Read the lesson through before you start cooking. Showing
notes in cook mode is being worked on.

A web version of the lessons and a weekly email are planned.

## Testing a lesson

Lessons need test cooks. If you cook one, open a
[test cook report](../../issues/new?template=test-cook-report.yml): did it work, how long
things really took, where you got lost, and a photo if you have one. A lesson moves from
`testing` to `tested` after two people have cooked it and reported back.

Module 1 is the place to start.

## Licence

The lessons, notes and photos in this repository are licensed under
[CC BY 4.0](LICENSE): you may share and adapt them, including commercially, as long as
you give credit. Credit "Cooklang cooking course" with a link to this repository.

Videos linked from lessons belong to their owners and are not covered by this licence.
If you send a correction or a photo, you agree to it being published under the same licence.
