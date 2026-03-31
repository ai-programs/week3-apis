# 🗂️ Week 3 — Build a Catalogue

This week you're building something new from scratch. No more TypeRacer — it's time to create a **catalogue app** powered by real data from the internet.

You'll connect to an **API** — a service that gives your app access to thousands of entries about Pokémon, superheroes, One Piece characters, countries, or Rick and Morty characters. Your app will fetch this data, display it as beautiful cards, and let users click through to see details.

By the end of today, you'll have something that looks and feels like a real app.

---

## 🧠 The Big Idea

Last week you learned about databases — places that store YOUR data. This week is different. You're going to use **someone else's data**.

An **API** (Application Programming Interface) is like a menu at a restaurant. You don't go into the kitchen — you look at the menu, pick what you want, and the waiter brings it to you. APIs work the same way: your app asks for specific data, and the API sends it back in a format called **JSON**.

The key idea: **there's an enormous amount of data out there on the internet, created by others, that you can use in your apps for free.**

---

## 🚀 Getting Started

### Step 1: Choose your API

Pick one of these APIs. Each one has different data — choose the one that interests you most.

| API                | What it has                                    | Explore it                                                                 |
| ------------------ | ---------------------------------------------- | -------------------------------------------------------------------------- |
| **PokéAPI**        | 1000+ Pokémon with stats, types, images        | [Open in browser →](https://pokeapi.co/api/v2/pokemon/pikachu)             |
| **Superhero API**  | 700+ Marvel & DC heroes with powerstats        | [Open in browser →](https://akabab.github.io/superhero-api/api/id/70.json) |
| **One Piece API**  | Characters, devil fruits, crews, sagas         | [Open in browser →](https://api.api-onepiece.com/v2/characters/en/1)       |
| **Rick and Morty** | 800+ characters with species, status, origin   | [Open in browser →](https://rickandmortyapi.com/api/character/1)           |
| **REST Countries** | 250 countries with flags, population, capitals | [Open in browser →](https://restcountries.com/v3.1/name/portugal)          |

### Step 2: Explore the data

**This is the most important step.** Click the link above for your chosen API. You'll see raw data in your browser — this is JSON.

Take a few minutes to look at it. Ask yourself:

- What fields are available? (name, image, stats, description?)
- What would look cool on a card?
- What extra information could go on a detail page?
- Where are the images?

You'll need to know this to tell Gemini what to build.

### Step 3: Open the Gemini chat

Look for the **✨ Gemini icon** on the right side of your screen. Tell it what you want to build — the catalogue, the cards, the detail view. Be specific about which API you're using and what data you want to show.

### Step 4: Build, test, iterate

Start simple — get data showing on the page first, even if it's ugly. Then make it better, step by step.

---

## 🔄 Make It Yours

Once you have the basics working, push it further. Some ideas:

- Cards with hover effects — zoom, glow, shadow, flip
- A search bar to find entries by name
- A detail view when you click a card
- Sort or filter by different attributes
- A "random" button that shows a surprise entry
- Dark/light mode toggle
- Animated loading states while data is fetching
- A compare mode — pick two entries and see their stats side by side
- Connect to Firebase from last week to save favourites

**CSS challenge:** This is the week to make something that looks professional. The more specific you are about the design you want, the better the result. "Make it look cool" is okay. "Cards with rounded corners, a dark background, a subtle purple glow on hover, and the image zooms slightly when I mouse over" is much better.

---

## 🧠 What You're Learning

| Concept                | What it means                         | Why it matters                                             |
| ---------------------- | ------------------------------------- | ---------------------------------------------------------- |
| **API**                | A service that gives your app data    | Access to millions of data points created by others        |
| **JSON**               | The format APIs use to send data      | Understanding it lets you pick exactly what to display     |
| **fetch**              | JavaScript's way of requesting data   | How your app talks to the internet                         |
| **Request → Response** | Your app asks, the API answers        | Same model as HTTP from Week 2, but now with external data |
| **CSS effects**        | Hover states, transitions, animations | What makes an app feel polished and professional           |

---

## 📁 Your Files

| File         | What's inside                   |
| ------------ | ------------------------------- |
| `index.html` | The structure of your catalogue |
| `style.css`  | The visual design               |
| `main.js`    | Fetching data + app logic       |

---

## 🔗 API Quick Reference

Need the base URLs? Here they are:

**PokéAPI**

- One Pokémon: `https://pokeapi.co/api/v2/pokemon/{name or id}`
- List: `https://pokeapi.co/api/v2/pokemon?limit=20`
- Docs: [pokeapi.co/docs/v2](https://pokeapi.co/docs/v2)

**Superhero API**

- One hero: `https://akabab.github.io/superhero-api/api/id/{id}.json`
- All heroes: `https://akabab.github.io/superhero-api/api/all.json`
- Docs: [akabab.github.io/superhero-api](https://akabab.github.io/superhero-api/)

**One Piece API**

- One character: `https://api.api-onepiece.com/v2/characters/en/{id}`
- All characters: `https://api.api-onepiece.com/v2/characters/en`
- Devil fruits: `https://api.api-onepiece.com/v2/fruits/en`
- Docs: [api-onepiece.com/en/documentation](https://api-onepiece.com/en/documentation)

**Rick and Morty API**

- One character: `https://rickandmortyapi.com/api/character/{id}`
- All characters: `https://rickandmortyapi.com/api/character`
- Docs: [rickandmortyapi.com/documentation](https://rickandmortyapi.com/documentation)

**REST Countries**

- By name: `https://restcountries.com/v3.1/name/{country}`
- All countries: `https://restcountries.com/v3.1/all?fields=name,flags,capital,population,region`
- Docs: [restcountries.com](https://restcountries.com/)

---

## 💡 Tips

- **Explore the API in your browser first.** Seriously — open the link, read the JSON, understand the structure. This is the single most important thing you can do before building.
- **Start ugly, make it pretty.** Get data on the page first, even as plain text. Design comes after.
- **Be specific about design.** Describe exactly what you want — colors, effects, layout. The AI is great at CSS, but it needs you to describe the vision.
- **Check the browser console (F12)** if something isn't working. API errors usually show up there.
- **Ask Arjun or Sérgio** if you're stuck on anything — they're here to help.

Have fun! 🗂️
