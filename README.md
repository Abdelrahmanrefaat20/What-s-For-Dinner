# What's For Dinner

**Your daily meal inspiration** — a recipe discovery app that shows a random meal each time you visit, complete with ingredients, step-by-step instructions, nutrition facts, and chef's tips.

![App preview](./image/utensils-solid-full.jpg)

## Features

- **Random meal generator** — click "Try Another Recipe" to get a new randomly selected dish
- **Recipe card** with photo, star rating, review count, prep time, cook time, and servings
- **Allergen/warning box** highlighting important dietary notes for the current recipe
- **Tabbed recipe details** (Bootstrap tabs):
  - **Ingredients** — full ingredient list
  - **Instructions** — step-by-step cooking directions
  - **Nutrition** — calories, protein, carbs, fat, fiber, and sodium
  - **Chef's Tips** — extra tips for getting the best result
- **Bookmark and share** buttons on each recipe
- Built-in recipe dataset (in `js/main.js`) — no external API or backend required

## Tech Stack

- **HTML5** — page markup (`index.html`)
- **CSS3** — custom styling and layout (`css/style.css`, `css/media.css`)
- **[Bootstrap 5](https://getbootstrap.com/)** — grid, tabs, and responsive navbar (`css/bootstrap.min.css`, `js/bootstrap.bundle.min.js`)
- **Vanilla JavaScript** — recipe data and randomizer/rendering logic (`js/main.js`)
- **Font Awesome** — icon set (`css/all.min.css`, `webfonts/`)

No build tools, frameworks, or package manager are required — this is a static site.

## Project Structure

```
What-s-For-Dinner/
├── index.html              # Main page markup
├── css/
│   ├── bootstrap.min.css     # Bootstrap framework
│   ├── all.min.css            # Font Awesome
│   ├── style.css              # Custom styles
│   └── media.css              # Responsive/media-query styles
├── js/
│   ├── bootstrap.bundle.min.js  # Bootstrap JS (tabs, navbar)
│   └── main.js                   # Recipe dataset + randomizer/render logic
├── webfonts/                 # Font Awesome web fonts
└── image/                    # Logo and avatar images
```

## How It Works

`js/main.js` holds an array of recipe objects (name, description, image, timing, servings, difficulty, ingredients, instructions, nutrition, and tips). On load — and each time the "Try Another Recipe" button is clicked — `getRandomMeal()` picks a random entry from the array and `displayMeal()` renders its details into the page.

## Getting Started

Since this is a static site, no installation or build step is needed.

1. Clone the repository
   ```bash
   git clone https://github.com/Abdelrahmanrefaat20/What-s-For-Dinner.git
   cd What-s-For-Dinner
   ```
2. Open `index.html` directly in your browser, or serve it locally:
   ```bash
   npx serve .
   ```
   (or use any static server / the VS Code "Live Server" extension)

## Customization

- **Add recipes**: append a new object to the `data` array in `js/main.js`, following the existing recipe structure.
- **Colors & theme**: custom overrides live in `css/style.css`.
- **Images**: recipe photos are currently pulled from Unsplash URLs in `js/main.js` (`imgCover` field) — replace with your own image URLs or local paths as needed.


