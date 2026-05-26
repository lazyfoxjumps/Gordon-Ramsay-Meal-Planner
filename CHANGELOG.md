# Changelog

All notable changes to the Gordon Ramsay Meal Planner skill are documented here.

The format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/), and this project uses [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.2.0] - 2026-05-23

### Added
- **Notion sync** (optional, opt-in per session). Push longer outputs straight to Notion when the Notion MCP is connected.
  - Recipe vault: one Notion page per recipe with properties for cuisine, effort, cost tier, dietary tags, prep time, and calories.
  - Meal plan board: weekly plans as a Notion database, one row per meal, linked to recipe pages.
  - Grocery list: checkbox to-do database grouped by aisle, syncs to phone.
  - Search-first-then-create pattern so existing databases get reused instead of duplicated.
- **Google Calendar sync** (optional, opt-in per session). Schedule the whole week so the user actually does it.
  - Meal events with ingredients in the description and a 30-minute prep reminder.
  - Prep reminders ("take chicken out of freezer", "marinate at 5pm", "soak beans overnight") scheduled at the right moment.
  - Grocery run event titled with the real store in the user's city.
- **Locale-aware store naming** for the grocery run event. Defaults for UK (Tesco, Sainsbury's, Asda, Morrisons, Waitrose, Lidl, Aldi, M&S Food), US (Trader Joe's, Whole Foods, Kroger, Safeway, Publix, Costco, Walmart, H Mart), Indonesia (Superindo, Hypermart, Ranch Market, Grand Lucky, AEON, Tip Top, pasar / wet market), India (Big Bazaar, Reliance Fresh, DMart, BigBasket, kirana, sabzi mandi), Singapore (FairPrice, Cold Storage, Giant, Sheng Siong, Mustafa), Malaysia (AEON, Tesco / Lotus's, Village Grocer, Jaya Grocer, Mydin), Australia (Woolworths, Coles, Aldi, IGA). Other countries: ask once, remember for the session.
- **Pantry memory file (`pantry.md`)**, opt-in. A project-root file Gordon reads at session start to skip re-asking about staples. Tracks always-stocked staples, usual fridge contents, country, city, preferred store, preferred wet market, budget tier, dietary restrictions, spice tolerance, kitchen equipment, and skill level.
  - Diff-before-write rule: Gordon shows what's changing before saving.
  - Never invents entries; only saves what the user explicitly told him.
  - Doesn't create the file unprompted; offers on the first save-worthy moment.
- Confirm-before-write rule applies to all three integrations. No silent writes to Notion, calendar, or the pantry file.

### Changed
- Intake step now checks for `pantry.md` before asking questions, and skips the staples question if the file already has them.
- "Fresh intake every new session" rule clarified: perishables and what's-in-the-fridge-right-now are still fresh-intake every session. The pantry file is the one exception and only stores staples, preferences, equipment, and store.

## [0.1.0] - 2026-05-23

### Added
- Initial release.
- Full Gordon Ramsay voice (British English, swearing allowed, motivational, theatrically disappointed by laziness, never cruel about circumstance).
- Intake flow with up to 9 inputs (fridge contents, energy, budget + country, restrictions, cooking tolerance, appetite, cleanup tolerance, goal, time available).
- Single-recipe mode with name, serves / time / effort / cleanup, ingredients with local swaps, numbered method, Gordon's verdict.
- Output modes: emergency meals, low-effort one-pan meals, weight gain / weight loss meals (with macro targets, no diet-culture moralising), grocery lists grouped by aisle and priced in local currency, weekly meal plans with leftover chaining, leftovers rescue plans.
- Country-aware realism for UK, US, Indonesia, India, Singapore, and Malaysia (pricing, equipment defaults, staple ingredients, market vs supermarket considerations).
- "Always find a path forward, with warning" rule for conflicts between user requests and stated restrictions.
- Save-to-`.md` behaviour for long outputs with a short voice-in-character chat summary and file link.
- Voice persistence across the whole conversation until the user opts out.
- Safety rules: dietary restrictions and allergies are absolute; no moralising about food, weight, or body; bullying is theatrical and aimed only at laziness, never at circumstance.

[0.2.0]: https://github.com/lazyfoxjumps/Gordon-Ramsay-Meal-Planner/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/lazyfoxjumps/Gordon-Ramsay-Meal-Planner/releases/tag/v0.1.0
