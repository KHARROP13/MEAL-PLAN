# Autumn 6 Week Plan (v2)

The autumn update to the original [K & P — 6 Week Plan](https://kharrop13.github.io/MEAL-PLAN/). Same engine and layout, rebuilt content, and — after an audit — honest numbers.

Plan starts **Monday 21 September 2026**.

## What this version fixes

**v1 linked to search boxes, not recipes.** Seven of the twelve dinners pointed at a site-search URL (`bbcgoodfood.com/search?q=...`) or a category page rather than an actual recipe. That was a pattern carried over from the summer plan. Every link in v2 now opens a specific recipe page that was fetched and checked. Two dishes have no link at all — the Chermoula Cauliflower (your Roasting Tin book) and the Puy Lentil & Squash bowl (your own assembly) — and they say so on the card instead of sending you somewhere useless.

**v1's calorie and protein numbers were optimistic.** They followed the summer plan's pattern (a dinner giving 38g protein for 440 kcal) rather than being derived from real recipes. Rebuilt from published recipe nutrition plus standard portion values, a vegetarian dinner is closer to 570 kcal for 33g. Every figure in v2 is now `(servings × the recipe's own per-serving nutrition) + the protein you add`, and both halves of that sum are visible at the top of `index.html`.

**Consequence: 140g protein and 1,400 kcal can't both hold.** Meals across the 42 days average 1,350 kcal and 95g protein. Closing the last 45g costs 280 kcal even from a shake and a skyr pot, landing the day near 1,630. You chose to protect protein, so the target is 140g and the calorie line is set at 1,600 — where it honestly lands, rather than a number you'd miss every day. The "How To" tab explains this in full. **Worth flagging to your coach, since 1,400 was their figure.**

Other things the audit turned up and changed:

- **Soup nights were your weakest protein night** (Ribollita gave you 26g). Now every soup night has a proper protein swap and runs 32–45g.
- **A ginger-garlic soy stir-fry was sitting in a Mediterranean plan** the night after your SE Asian delivery. Removed.
- **The Mezze Plate was a cold, no-cook assembly** — wrong for November. Replaced with the Moroccan tagine.
- **One soup a week didn't really deliver "more soups and stews."** Now six different soups, one per week, each matching that week's cuisine, plus stews (tagine, gigantes, chickpea) among the dinners.
- **Week themes didn't match their contents** — "French Bistro Autumn" contained za'atar aubergine, a Turkish soup and a stir-fry. Themes now describe what's actually in the week.
- **The kale salad sat on Tuesday and Saturday, four days apart.** Moved to Tuesday and Thursday.
- **Ribollita only serves 4** but the Thursday-dinner-plus-lunches pattern needs more — the week note now tells you to make it 1½×. The other soups serve 6, which covers the week with a portion spare.
- The page was render-tested in a browser: no JS errors, every tab and all 42 days render, no horizontal overflow on a phone.

## How the plan works

- **Breakfast** — overnight oats or stovetop porridge, seven variations, one per day of the week. Protein comes from Greek yoghurt and a scoop of powder.
- **Lunch (Kiska)** — Mon salad · Tue kale · Wed salad · **Thu kale** · **Fri soup** · Sat salad · **Sun soup**. The Friday and Sunday soups come out of Thursday's pot.
- **Lunch (Paul)** — Tossed, every day, unchanged.
- **Dinner** — one base dish, protein added separately at the end. Thursday is soup night. Tuesday is Taco Tuesday (chicken or turkey mince — no beef). Wednesday is the SE Asian delivery.
- **No red meat for Paul** anywhere: chicken, turkey, fish, seafood and eggs only.

## The recipes

Seventeen linked recipes, each opened and verified as free with no paywall or login:

**Soups (one per week)**
| Week | Soup | Source | Serves | Published nutrition |
|---|---|---|---|---|
| 1 | [Fasolada (Greek White Bean Soup)](https://www.themediterraneandish.com/greek-bean-soup-fasolada/) | The Mediterranean Dish | 6 | none — estimated |
| 2 | [Turkish Red Lentil Soup](https://www.themediterraneandish.com/turkish-lentil-soup/) | The Mediterranean Dish | 6 | 283 kcal / 10.6g |
| 3 | [Ribollita (Tuscan White Bean & Kale)](https://skinnyspatula.com/ribollita-tuscan-white-bean-soup/) | Skinny Spatula | 4 | 271 kcal / 13g |
| 4 | [Harira](https://www.themediterraneandish.com/harira-recipe/) | The Mediterranean Dish | 6 | 304 kcal / 22.3g |
| 5 | [Spicy Spinach & Lentil Soup](https://www.themediterraneandish.com/mediterranean-spicy-spinach-lentil-soup/) | The Mediterranean Dish | 6 | 250 kcal / 16.7g |
| 6 | [Hearty One-Pot Lentil Stew](https://www.themediterraneandish.com/vegan-lentil-soup-recipe/) | The Mediterranean Dish | 6 | 247 kcal / 15.4g |

**Dinners** — [Ratatouille Butter Bean Traybake](https://boldbeanco.com/blogs/beanspo-recipes/ratatouille-butter-bean-traybake) (Bold Bean Co, Monday 21st), [Briam](https://www.themediterraneandish.com/briam-greek-roasted-vegetables/), [Souvlaki with Tzatziki](https://www.themediterraneandish.com/greek-chicken-souvlaki-recipe-tzatziki/), [Shakshuka](https://www.themediterraneandish.com/shakshuka-recipe/), [Za'atar Roasted Aubergine](https://www.themediterraneandish.com/roasted-eggplant-recipe/), [Gigantes Plaki](https://www.themediterraneandish.com/gigantes-plaki-greek-giant-beans/), [Gemista](https://www.themediterraneandish.com/gemista-greek-stuffed-vegetables/), [Spinach & Chickpea Stew](https://www.themediterraneandish.com/spinach-chickpea-stew/), [Moroccan Vegetable Tagine](https://www.themediterraneandish.com/moroccan-vegetable-tagine-recipe/), [Menemen](https://www.themediterraneandish.com/menemen-recipe/), [Lemon-Garlic Baked Cod](https://www.themediterraneandish.com/baked-cod-recipe-lemon-garlic/).

**Not linked, and the card says why** — Chermoula Roasted Cauliflower (your Roasting Tin book) and Warm Puy Lentil & Roasted Squash Bowl (your own assembly).

Nine of the seventeen publish their own per-serving nutrition; those figures are used directly. The other eight don't, so the figure is my estimate from the ingredient list — every day card marks which is which in amber, and the Sources tab lists them all.

## Adding this to your repo

1. Create an `autumn/` folder in `KHARROP13/MEAL-PLAN` and put `index.html` in it — the summer plan stays untouched at the root.
2. Commit and push. GitHub Pages will serve it at `https://kharrop13.github.io/MEAL-PLAN/autumn/`.
3. To make it the homepage instead, overwrite the root `index.html` and move the summer one to `/summer/`.

Either of you can edit `index.html` on GitHub directly. The recipe list, the protein-swap values and the week structure are all plain data at the top of the `<script>` block, each with a comment explaining what it does.
