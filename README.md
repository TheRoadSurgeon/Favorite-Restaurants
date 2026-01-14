# Favorite Restaurants (Flutter)

A Flutter app that displays a scrollable list of favorite restaurants and supports quick access to each restaurant’s menu, website, and contact information. The UI is designed to be clean and mobile-friendly, with card-based list items and a context menu that appears next to the user’s long-press position.

This project was built for CS378: Framework-Based Software Development for Hand-Held Devices, Project 3.

---

## Features

- Scrollable restaurant list with card-style items showing the restaurant name, address, and a thumbnail image
- Tap on a restaurant to open its Menu screen
- Long press to open a context popup menu positioned at the press location with actions to:
  - Show menu
  - Open website
  - Open contact info
- Contact screen with actionable rows:
  - Address opens Maps
  - Phone initiates a call when available
  - Website opens the browser
- Menu screen with a hero image and menu items grouped by category

---

## Screens

The app has three screens, each managed by its own class in a separate file:

1. Restaurant List (`RestaurantListScreen`)
   - Card-based list with thumbnail, name, and address
   - Tap opens Menu, long press opens popup actions

2. Menu (`MenuScreen`)
   - Hero image
   - Menu items grouped by category with prices right-aligned

3. Contact (`ContactScreen`)
   - Address, phone (optional), website actions

---

## Tech Stack

- Flutter / Dart
- Packages
  - `url_launcher` for opening websites, maps, and phone calls
  - `collection` for grouping menu items by category

---

## Project Structure

```text
lib/
  models/restaurant.dart
  data/
    sample_restaurants.dart
    menus/                 # one file per restaurant menu
  screens/
    restaurant_list_screen.dart
    menu_screen.dart
    contact_screen.dart
assets/
  images/
    restaurants/           # thumbnails + hero images
```

---

## Run Locally

1. Fetch dependencies
   ```bash
   flutter pub get
   ```

2. Run
   ```bash
   flutter run
   ```

If you add images as assets, ensure they are declared under `assets:` in `pubspec.yaml`.

---

## Usage

- Open the app to view the restaurant list.
- Tap an item to open the menu.
- Long press an item to open the popup menu near your press point and choose an action.

---

## Data and Assets

Restaurant data is defined as local constants and composed into a master list.
Images may be local assets or network URLs. Recommended sizes:
- Thumbnails: square 1:1
- Hero images: wide 2:1

---

## LLM Usage

This project used an LLM as required by the course. The refined spec and project scaffolding were supported by OpenAI ChatGPT, with iterative fixes and validation via building and running the app.

---

## Notes

- All content is for educational use.
- This app uses local data only and does not include a backend.