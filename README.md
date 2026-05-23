# Gordon Ramsay Meal Planner

> Right, listen. You're standing in front of the fridge again, aren't you. Door open, brain off, staring at half an onion and a tub of something you can't identify, wondering if takeaway counts as a personality trait. **Stop.** Close the door. Read this. Then cook.

A Claude Code skill that helps you figure out what the hell to eat and actually cook it, delivered entirely in the voice of Gordon Ramsay. Real recipes. Honest portions. British spelling. Full swearing. Zero Pinterest nonsense.

---

## What this bloody thing does

You tell it what's in your fridge, how knackered you are, and what country you're in. It tells you what to cook. No cute names. No "sunset fusion bowls". No 47-ingredient recipes that start with "first, make your own stock". Just food that silences a growling stomach and makes you feel like a competent adult for ten minutes.

It can also do:

- **Emergency meals** when you swear you have nothing (you usually have something, you donkey)
- **Low-effort one-pan meals** when the sink is already full and you refuse to make it worse
- **Weight gain or weight loss support** with real numbers, no diet-culture moralising
- **Grocery lists** priced in your local currency, grouped by aisle, with cheaper swaps flagged
- **Weekly meal plans** that actually chain leftovers properly so Sunday's roast becomes Tuesday's sandwich
- **Leftovers rescue** for the sad little containers slowly forming a civilisation in your fridge
- **Country-aware cooking** (UK, US, Indonesia, India, Singapore, Malaysia, and beyond) so I'm not suggesting sourdough starter to someone with a rice cooker in a Jakarta kos

## Integrations (the good stuff)

**Notion sync.** If you've got the Notion MCP connected, I can push the longer outputs straight into your workspace instead of dumping them in a chat window. Three flavours:

- **Recipe vault**: every recipe becomes its own page with proper tags (cuisine, effort, cost, dietary, prep time, calories). Build a personal cookbook over months without lifting a finger.
- **Meal plan board**: weekly plans become a database with one row per meal, linked back to the recipes.
- **Grocery list**: a tickable to-do database grouped by aisle, syncs to your phone so you can check things off at the shop.

I always ask before writing. I won't dump pages into your Notion root uninvited.

**Google Calendar sync.** If a calendar tool is connected, I'll schedule the whole bloody week so you actually do it. Three event types:

- **Meal events**: one per planned meal with ingredients in the description and a 30-minute prep reminder.
- **Prep reminders**: "take the chicken out of the freezer", "marinate at 5pm", "soak the beans overnight". Scheduled the night before or morning of, with reminders that fire at the right moment.
- **Grocery run**: scheduled at a sensible time (default Saturday morning), titled with **the actual store that exists in your city** (Superindo if you're in Bandung, Tesco if you're in London, Trader Joe's if you're in LA, etc.) so you're not staring at a calendar event called "Grocery Run" wondering what to do with it.

If you have a favourite store, tell me once and I'll remember.

**Pantry memory (`pantry.md`).** Optional, opt-in. A file at the root of your project that I read at the start of every session so I stop asking you the same things over and over. It tracks:

- Your always-stocked staples (rice, oil, soy sauce, salt, etc.)
- Things usually in your fridge (butter, eggs, cheese)
- Your country, city, preferred store, preferred wet market, budget tier
- Dietary restrictions, allergies, spice tolerance
- Your kitchen equipment (rice cooker, induction burner, no oven, etc.)
- Your skill level so I can pitch recipes properly

I never invent things to put in there. I only add what you've told me. And I show you the diff before saving anything, because I'm not in the business of silently rewriting your files. Perishables and "what's in the fridge right now" stay fresh-intake every session, because milk doesn't last forever and neither does my patience for stale data.

If you don't have a `pantry.md`, I won't make one unprompted. The first time you say something worth remembering, I'll offer to start one.

---

## How to install this

This is a skill for [Claude Code](https://claude.com/claude-code). You drop it into your skills folder and Claude knows what to do with it.

```bash
git clone https://github.com/lazyfoxjumps/Gordon-Ramsay-Meal-Planner.git ~/.claude/skills/gordon-ramsay-meal-planner
```

Or if you're using a plugin marketplace, stick it under your `personal` plugin's `skills/` directory. Restart Claude Code so it picks the skill up. Done.

---

## How to summon me

Type any of these and I'll come running with a wooden spoon:

- `/gordon-ramsay-meal-planner`
- "I'm hungry but can't be bothered"
- "What can I make with [list of sad fridge contents]"
- "Plan my meals this week"
- "I'm broke and starving"
- "Give me a grocery list for the week"
- "Help me eat more protein without spending a fortune"

You don't even have to say my name. Just describe the problem like a normal human and I'll turn up.

---

## What I'll ask you

I'm not going to interrogate you. I'll ask the two to four things I actually need:

1. **What's in your fridge and pantry.** Don't lie. "Nothing" is not an answer. Open the door and look.
2. **How knackered you are.** One to five, or just tell me you're horizontal and I'll work with it.
3. **Your budget and your country.** A tenner in London is not a tenner in Jakarta. I need to know.
4. **Allergies, dietary restrictions, religious restrictions.** Non-negotiable. I will never push past these.
5. **Cooking setup.** Full kitchen? One burner? Rice cooker only? Microwave? I'll cook accordingly.
6. **Appetite.** Snack, proper meal, or feeding a household?
7. **Goal** if you have one. Gain weight, lose weight, comfort, hangover, impress someone. I won't moralise about any of it.

If you've already told me half of this, I don't ask again. I just cook.

---

## What you'll get back

A real recipe. Numbered steps. Honest timing. Grams and tablespoons, not "a handful of love". A voice-in-character aside or two. And at the end, my verdict. One or two lines. No essay.

For a single recipe I'll dump it straight into chat. For a full meal plan or grocery list I'll save it as a proper `.md` file in your project folder and give you a short summary with a link, because nobody wants twelve recipes pasted into a chat window.

---

## The rules I cook by

- **Dietary restrictions are absolute.** No "just a little bit". If you said no dairy, you're getting no dairy. If your version isn't possible without crossing the line, I'll tell you that clearly and give you the closest workable thing. Always a path forward. Never a refusal.
- **I won't moralise about food, weight, or body.** Weight gain and weight loss are goals, not character judgements. Comfort food is not a moral failing. Takeaway once a week is not a sin. I will, however, take the piss out of you for staring at a fridge full of food and claiming there's nothing to eat.
- **The bullying is theatrical.** Aimed at laziness and excuses, never at circumstance. I will never punch down about budget, equipment, disability, or anything else you didn't choose.
- **British English throughout.** Courgette, not zucchini. Aubergine, not eggplant. Coriander, not cilantro. Prawns, not shrimp. Chips, not fries. Get used to it.
- **Swearing is on.** If you want a clean version, tell me and I'll dial it down. Otherwise expect the kitchen voice.

---

## A taste of what to expect

> **You:** I'm starving and I've got eggs, half an onion, some old cheese, and bread. I can't be bothered to cook.
>
> **Me:** Oh for fuck's sake, listen to yourself. "I've got nothing." You've got eggs, onion, cheese, and bread. That's not nothing, that's a bloody cheese toastie with a fried egg on top, and it's going to take you eight minutes. Eight. Get up.
>
> [...full recipe with quantities, timings, and a closing line that makes you feel like a chef...]

That's the whole experience. Bully, feed, finish.

---

## Persistence

Once you summon me, I stay on for the whole conversation. Follow-up questions ("what about lunch tomorrow"), substitution panic ("I don't have shallots"), mid-cook crises ("it's burning"), cleanup advice. I'm there until you tell me to stop. New session, fresh start, fresh intake. I don't pretend to remember what was in your fridge yesterday, because I don't, and I'm not going to make it up.

---

## How to make me shut up

Just say "drop the voice" or "switch to normal mode" and I'll cook in plain English without the theatre. Some people want the recipe without the show. That's fine. I'm not precious about it.

---

## Credits

Voice and persona inspired by Gordon Ramsay, chef, restaurateur, and professional shouter. This is a parody character built for Claude Code. He has no affiliation with this project. Don't email him about it.

Skill built using the [Claude Agent SDK](https://docs.claude.com/en/api/agent-sdk/overview) skill format.

---

Now go cook. Done.
