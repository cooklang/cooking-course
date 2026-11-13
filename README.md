# Cooking course in Cooklang

Learn basic cooking technique by cooking dishes.

Each lesson is one recipe in [Cooklang](https://cooklang.org), a plain-text recipe format.
The steps cook the dish. The notes between the steps explain the technique: why the pan
starts cold, why the mushrooms get a splash of water first, why a steak rests, why
yesterday's rice fries better.
After a lesson you should be able to cook the dish again without the recipe.

The course is for people who already cook from recipes and want the mechanism, not just
the rule. The notes go down to the chemistry and physics: they name each reaction (the
Maillard reaction, the Amadori rearrangement, starch gelatinization), give the numbers,
and end with the terms to look up.

## Status

**All nine modules are in draft.** The 36 lessons are written and nobody has cooked them
yet: the amounts and times are untested, and the lessons have no photos or video links.
Each lesson's front matter shows its `status`, and a lesson is marked `tested` only after
people have cooked it and reported back.

Five lessons are cooked below official food-safety figures on purpose, because the dish
is defined that way: the salmon, the soft-boiled eggs, the French omelette, the mayonnaise
and the carbonara. Each one says so in a `Safety:` note, gives the official figure, and
says how to meet it.

## Syllabus

Nine modules, four lessons each. The modules do not depend on each other. Start with
module 0 if you want the plain versions first. The last lesson of each module combines
what the module taught; where the dish allows, its ingredients are slots that you fill
with what you have.

Dishes may change as lessons are tested.

| Module | Lessons |
|---|---|
| 0 · Basics | Plain rice (absorption) · Buttered pasta (boiling pasta) · Boiled eggs, soft to hard (timing) · Blanched green beans (blanching, salt) |
| 1 · Heat in a pan | Crispy chicken thighs (rendering fat) · Mushrooms on toast (water before browning) · Steak with pan sauce (searing, deglazing, resting) · Any-vegetable stir-fry |
| 2 · The oven | Tray of roast vegetables (dry heat, space) · Roast chicken (salting ahead, carryover) · Slow-baked salmon (cooking to a temperature) · Sheet-pan dinner |
| 3 · Wet heat | Tomato soup (sweating, simmer against boil) · Poached chicken and stock (collagen to gelatin) · Beef stew (braising) · Any-bean soup |
| 4 · Eggs and emulsions | French omelette (how egg sets) · Green salad with vinaigrette (emulsifying) · Mayonnaise (a stable emulsion, and mending a broken one) · Carbonara |
| 5 · Starch | Rice pilaf (absorption, gelatinization) · Spaghetti aglio e olio (finishing pasta in the pan) · Mashed potatoes (even cooking, loose starch) · Fried rice (retrogradation) |
| 6 · Tasting and fixing | Bitter leaf salad (salt against bitterness) · Lentils with lemon (salt, then acid) · Tomato pasta, tuned (umami, fat) · Chickpea stew, fixed (one change at a time, and rescues) |
| 7 · Mastering the knife | Tomato salsa (grip, claw, dicing an onion) · Chimichurri (mincing, garlic strength) · Coleslaw (thin slices, matchsticks, salting) · Diced vegetable soup (cutting to a size) |
| 8 · Mastering the machines | Slow-cooker beef chilli · Air-fryer potato wedges · Pressure-cooker risotto · Microwave jacket potatoes |

The knife lessons describe grips and cuts in words. That is the weakest way to teach
them; they are first in line for video links.

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
  `Science:`, `If it goes wrong:`, `Safety:`, `Watch:`, `Next time:`.
- A `Science:` note gives the mechanism by its proper name, with figures where they have
  been measured, and closes with `Look up:` and the search terms.
- A `Watch:` note links a short video of the one moment that is hard to describe in words.
- Where the last lesson of a module uses slots, it names them as ingredients (`protein`,
  `hard vegetables`) with the choices in brackets, so the amounts still scale and still
  make a shopping list.
- Amounts are metric and temperatures are in °C. Oven temperatures are for a conventional
  oven, with the fan setting in brackets.
- A `Science:` note stands on its own within its module: it never relies on a lesson from
  another module.
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

Pick any lesson; module 1 is a good place to start.

## Licence

The lessons, notes and photos in this repository are licensed under
[CC BY 4.0](LICENSE): you may share and adapt them, including commercially, as long as
you give credit. Credit "Cooklang cooking course" with a link to this repository.

Videos linked from lessons belong to their owners and are not covered by this licence.
If you send a correction or a photo, you agree to it being published under the same licence.
