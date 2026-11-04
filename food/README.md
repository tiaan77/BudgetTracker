# PocketPlate – food & weight-loss tracker

A phone app (installable web app / PWA) for tracking what you eat and drink, built around South African foods.

## Features
- **SA food search** – ~170 built-in local foods, works offline (pap, boerewors, vetkoek, chakalaka, bunny chow, kota, Castle, Savanna, Simba…), plus online search of SA products on Open Food Facts.
- **Barcode scan** – scan packaged products with the camera (looks them up on Open Food Facts). Products that aren't found can be added once with Quick add, and the app remembers the barcode.
- **Photo recognition** – take a photo of your plate, drink or a nutrition label. Claude identifies the items and estimates calories and macros, and you can edit them before saving.
- **Goals** – enter sex, age, height, weight, activity level, goal weight and target date (6 months by default). The app sets a daily calorie target, capped at a safe pace of about 1 kg/week or less and never below 1200 kcal (women) / 1500 kcal (men), plus protein, carb, fat and sugar targets.
- **BMI** with category, healthy weight range for your height, and your BMI at goal weight.
- **Progress** – weight trend compared with your planned line, and calories for the last 14 days compared with your target.
- **Insights** – looks at your last 14 days for patterns: alcohol, sugary drinks, takeaways, fried food, processed meat, sweets, refined starch, late-night eating, weekend overeating, low protein and water. For each it suggests local swaps. The **AI coach** gives personalised advice on what to avoid.
- Data stays **on the phone only** (localStorage). You can export and import a backup.

## Install on your phone
1. Host the `food/` folder over HTTPS. GitHub Pages on this repo works: Settings → Pages → deploy from branch. The app is then at `https://<user>.github.io/BudgetTracker/food/`.
2. Open that URL on your phone:
   - **Android (Chrome):** ⋮ menu → *Install app* / *Add to Home screen*
   - **iPhone (Safari):** Share → *Add to Home Screen*
3. It opens full screen like a normal app. Logging, search and insights work offline. Photo AI, barcode lookup and online search need internet.

## Photo AI setup
Photo recognition and the AI coach use the Claude API. Under **Profile → AI photo recognition**, paste your own Anthropic API key from console.anthropic.com. The key is stored only on your phone and is sent only to Anthropic. Usage is billed to your Anthropic account per photo.

*Nutrition values are estimates. This app is not medical advice.*
