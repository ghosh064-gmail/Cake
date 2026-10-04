# Cake Shop Manager (Android, Kotlin, SQLite)

Offline inventory + billing + dashboard app for a cake shop. Pre-loaded with the 159 items from `price_list.pdf`
(selling price only) and shelf life from `monginis_self_life.xlsx`.

## Get the APK (no Android Studio needed)
1. Create a free GitHub repo and upload everything in this folder (keep `.github/workflows/build-apk.yml`).
2. Open the repo > Actions > "Build APK" > Run workflow (it also runs on every push).
3. When it finishes (about 5 minutes) download the artifact `CakeShopManager-apk` > unzip > `app-debug.apk`.
4. Copy the APK to the phone, open it, allow "Install unknown apps" when asked.

## Or with Android Studio
Open this folder > let Gradle sync > Build > Build APK(s). Output: `app/build/outputs/apk/debug/app-debug.apk`.

## Using the app
- Dashboard: units & value in stock, today's sales and margin, returns, vendor payable (due today / overdue / outstanding), 7-day table.
- Inventory: search, add/edit items, shelf life beside price, add or remove stock. All stock starts at 0.
- Billing: add items, customer details, Cash/UPI/Card, saves bill, reduces stock, share bill as text.
- Returns: record expired/damaged/returned food; reduces stock; counted in dashboard.
- Vendors: add vendor bills with due date, record payments.
- Menu (top right): Download everything (.xlsx), Export database (CSV), Update stock from image, Settings (margin %).
- Files are saved to Downloads/business data/.
- Update stock from image: pick a photo of a stock list (name or code + quantity on each line); on-device OCR matches lines to items, you review/edit, then Add or Set stock.

## Notes
- Margin = 20% of selling price (change under Settings). Reports show Margin % / Margin per unit / Margin on sales.
- Shelf life values marked "Category default" in `preloaded_inventory_preview.xlsx` were not in the shelf-life file; edit them in the app.
