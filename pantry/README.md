# PocketPantry – weekly shopping & usage tracker

A phone app (installable web app, same setup as PocketPlate) that starts from your weekly shopping list and learns what you actually use.

## How a week works
1. **List** – this week's shopping list, by category. Tick items as they go in the trolley (tap the amount or ⋯ to change how much, or skip an item this week). Leftovers from last week are subtracted, so you only buy the difference. Long-life pantry and drinks items only appear when you mark them as running low. Add one-off extras at the bottom.
2. **Stocktake** – at the end of the week, say how much of each item is left (None, ¼, ½, ¾, All or an exact amount) or tap **Ran out** if it finished early. Mark pantry items that are running low.
3. **Finish week** – the app records what you used, carries leftovers forward and builds next week's list. It also adjusts the weekly amounts:
   - **Ran out early** → amount goes up a step (about +20%).
   - **Half or more left over**, or **leftovers two weeks running** → amount moves towards what you really use, plus 10%. After only one week it moves halfway, so one odd week doesn't throw it off.
   - You see every change on the List, and can change any amount under **Amounts**. Turn off automatic changes there to get suggestions you apply yourself.

## Sharing with Claude
Under **Share → Copy for Claude**, the app copies your amounts, leftovers, usage history and current list, with instructions for replying. Paste it into the Claude app and ask for help (meal plans around leftovers, less waste, budget). Claude ends its reply with a `{"pocketpantry": …}` block. Paste the reply back into the app and tap **Apply**. It can change weekly amounts, change only this week's list, add or remove items, mark pantry items low and add extras. **Undo** reverses it.

**Share list** sends the list as plain text to WhatsApp, email or notes.

## Install
Host the repo on GitHub Pages (Settings → Pages → deploy from branch). The app is then at `https://<user>.github.io/BudgetTracker/pantry/`. On Android use ⋮ → *Install app*; on iPhone use Share → *Add to Home Screen*. It works offline.

Data stays on the phone (localStorage). Use **Share → Save backup** to keep a copy or move phones. The starting list is in `starter-list.js`.
