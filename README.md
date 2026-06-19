# Myas-Meal-Planner-and-Nutrition-Tracker-
# 🐾 Mya's Meal Planner

A complete nutrition and feeding tracker for Mya's homemade raw/whole-food diet — built as a single self-contained HTML file. No installs, no build tools, no npm. Just open it in a browser.

**Mya:** American Pit Bull Terrier · 60 lb · 3 years, spayed · Moderate activity
**Daily target:** 16 oz per meal · 2 meals/day · ~1,350 kcal/day

---

## 🚀 How to Use It

This app is hosted on **GitHub Pages**, so it works permanently from a single link — no downloading, no Safari file-opening issues.

1. Open your GitHub Pages URL (e.g. `https://yourusername.github.io/mya-meal-planner`) in Safari on your iPad
2. Tap the **Share** button → **Add to Home Screen**
3. It now behaves like a normal app icon — tap it any time to log meals

All your data (fed status, add-ins, notes) is saved automatically in the browser and will still be there next time you open it, as long as you don't clear Safari's site data.

---

## 📱 The Five Tabs

### 📋 Plan
Reference info that doesn't change day-to-day:
- Full **AAFCO daily nutrient targets** (27 nutrients — macros, minerals, fatty acids, vitamins) for Mya's size and activity level
- Visual **4-week rotation calendar** showing which protein is fed each day, with fish days (Thursday & Sunday) highlighted

### 📅 Calendar
Day-by-day meal logging:
- Navigate forward/backward by date with ‹ ›
- See that day's AM/PM meal (protein, starch, veg, organ) auto-pulled from the 4-week rotation
- Tap **Mark Fed** to log a meal
- Tap **+ Add-ins** to log extras (blueberries, fish oil, bone broth, hard boiled egg, etc.) with exact ounces — these feed into the nutrition totals

### 📜 History
A feeding history log you can review three ways:
- **Week** — a 7-day list with fed status for AM/PM and a notes field per day
- **Month** — full calendar grid; small dots show which meals were fed, a gold dot marks days with a note
- **Year** — 12 mini-calendars at a glance, color-coded by how complete each day's feeding was

Tap any day in Month or Year view (or the note line in Week view) to open full meal details and add or edit a note for that day — vet visits, reactions, anything worth remembering.

### 📊 Nutrition
A rolling 30-day average across all 27 AAFCO nutrients:
- Status summary: how many nutrients are Optimal / Low / High
- Per-nutrient bars showing current value vs. the AAFCO min–max range
- Red = below minimum, amber = above maximum, green = on target

### 📖 Guide
Reference material for meal prep:
- **Protein options** — current rotation list with fat level (lamb removed; Beef 85/15, Turkey, Chicken, Pork Loin, plus Sardines/Salmon on fish days)
- **Vegetable guide** — green light (rotate freely), use sparingly, and avoid lists
- **Starch options** — quinoa, oats, sweet potato, white rice, with prep notes
- **Organ meat guide** — liver, heart, kidney frequency and limits
- **Daily constants** — the fixed supplements added to every meal (eggshell powder, iodized salt, psyllium husk, vitamin E, etc.)

---

## 🔄 The 4-Week Rotation

| Week | AM/PM Proteins | Fish Day Swap |
|------|-----------------|----------------|
| 1 | Beef (85/15) + Turkey | Sardines (Thu & Sun) |
| 2 | Pork Loin + Chicken | Salmon (Thu & Sun) |
| 3 | Turkey + Beef (85/15) | Sardines (Thu & Sun) |
| 4 | Chicken + Pork Loin | Salmon (Thu & Sun) |

Rotation repeats every 4 weeks, calculated automatically from the date — it never needs to be reset and works for any past or future day.

---

## 🥩 Daily Meal Structure (16 oz total)

- **Protein:** 7–8 oz
- **Starch:** 2–3 oz
- **Vegetables:** 2–3 oz
- **Organ meat:** 0.5 oz (liver 2–3x/week, heart 1–2x/week)

**Every meal also gets:**
- ½ tsp eggshell powder (calcium)
- 1 pinch iodized salt
- ¼ tsp psyllium husk powder
- ¼ tsp mixed tocopherols (or 200 IU vitamin E oil on fish days)
- Ginger or herb cube (non-fish) / spearmint (fish)
- 1–2 tbsp reserved cooking liquid or bone broth

---

## 🛠 Customizing

Everything lives in one file: `index.html`. No build step — just edit and re-upload to GitHub.

**Add a new ingredient or add-in:**
Find the `FOODS` or `ADDINS` object near the top of the `<script>` section and add a new line using the `mkN(...)` helper (26 nutrient values per oz).

**Change AAFCO targets:**
Edit the `AAFCO` array — each entry has `min` and `max` values.

**Change the rotation:**
Edit the `WEEKS` object — each day has an `am` and `pm` meal built with `meal(protein, starch, veg, organ)`.

---

## ☁️ Deploying Updates

1. Go to your repo on **github.com**
2. Open `index.html` → click the pencil (✏️) to edit
3. Paste in the updated code
4. Click **Commit changes**
5. Wait ~30–60 seconds — your live URL updates automatically

No separate "deploy" step needed once GitHub Pages is turned on (Settings → Pages → Branch: main).

---

## 💾 Data & Storage

- All meal logs, add-ins, and notes save to **browser localStorage** — fully offline, no backend, no account needed
- Data is tied to the browser + URL it was saved from, so always access the app from the same GitHub Pages link
- Nothing is sent over the network — everything stays on your device

---

Built for Mya. 🐾
