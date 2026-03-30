# Week 3 — Planning Document

## Overview

**Title:** Build a Beautiful Catalogue
**Duration:** 2 hours
**New project:** Yes (separate from TypeRacer)
**Key technology:** APIs (fetch, JSON), CSS animations and transitions
**Deploy:** GitHub Pages (public APIs, no keys to hide)

---

## Core Concepts to Teach

### 1. What is an API?

An API is like a menu at a restaurant. You don't go into the kitchen — you look at the menu, pick what you want, and the waiter brings it to you. APIs work the same way: your app asks for specific data, and the API sends it back.

The key idea: **there's an enormous amount of data out there on the internet, created by others, that you can use in your apps for free.**

Use a live demo in the browser to make it tangible. Open `https://pokeapi.co/api/v2/pokemon/pikachu` directly in the browser and show the raw JSON. "This is what your app receives when it asks for data about Pikachu."

### 2. JSON — Reading Data

Before building anything, spend 10-15 minutes showing what JSON looks like. Students don't need to write it — they need to **read** it.

```json
{
  "name": "Pikachu",
  "id": 25,
  "height": 4,
  "weight": 60,
  "types": [
    { "type": { "name": "electric" } }
  ],
  "stats": [
    { "base_stat": 35, "stat": { "name": "hp" } },
    { "base_stat": 55, "stat": { "name": "attack" } },
    { "base_stat": 90, "stat": { "name": "speed" } }
  ]
}
```

Explain it as: "It's like a profile card. Each field has a name and a value. Some values are simple (a name, a number), some contain lists (types, stats), and some contain other profile cards inside them (nested objects)."

Understanding JSON at a reading level is the prerequisite for being able to ask Gemini for meaningful changes: "show the speed stat instead of the attack" only makes sense if they understand the structure.

### 3. The Request Cycle

Build on Week 2's HTTP knowledge:

1. User types "pikachu" in the search bar
2. JavaScript sends a request to the PokéAPI server
3. The API server responds with JSON data
4. JavaScript reads the JSON and updates the page

This is the same request/response model from Week 2, but now they're requesting data from someone else's server instead of reading/writing their own Firebase data.

### 4. CSS — Making It Beautiful

This is the week where CSS gets serious. Previous weeks were "make it look decent." This week is "make it look **professional**."

Key CSS concepts to explore through prompting:
- **Cards with hover effects** — scale, shadow, glow
- **Smooth transitions** — `transition: all 0.3s ease`
- **Grid/Flexbox layouts** — responsive card grids
- **Gradients and backgrounds** — modern visual effects
- **Typography** — font pairing, sizing hierarchy
- **Loading states** — skeleton screens or spinners while data loads

Students should be encouraged to be very specific in their prompts about visual design. "Make the cards have rounded corners, a subtle shadow that gets bigger on hover, the image zooms slightly when I hover, and add a gradient background" is a great prompt.

---

## The Project: A Searchable Catalogue

### Core Features
1. **Search bar** — type a name or term, results appear
2. **Card grid** — results displayed as beautiful cards with images
3. **Detail view** — click a card to see full information
4. **Responsive layout** — looks good on different screen sizes

### Bonus Features (if time permits)
- **Compare mode** — select two items, see them side by side with stats
- **Favourites** — save liked items (localStorage or Firebase from Week 2!)
- **Filters** — filter by type, category, etc.
- **Animations** — cards animate in when results load
- **Theme toggle** — dark/light mode

### The "Compare" Feature

If students finish the basic catalogue early, the compare feature is a great stretch goal. Pick two items and see their stats side by side — "Who Would Win?" built into the catalogue. This works naturally with APIs that have numerical stats (Pokémon, superheroes, Dragon Ball).

---

## API Choice

### Recommended: Everyone uses the same API (PokéAPI)

**Why PokéAPI:**
- Universal appeal across the 12-16 age range
- No API key needed
- Clean, well-structured JSON
- Great images (official artwork, sprites)
- Numerical stats perfect for comparison features
- Extremely well-documented
- Very reliable (high uptime)

### Alternative: Let students choose

If you prefer variety, the project structure works identically with any of these. You teach the concept using PokéAPI as the demo, and students can choose:

| API | Theme | Has Stats? | Key? | Images? | Best For |
|---|---|---|---|---|---|
| **PokéAPI** | Pokémon | ✅ 6 base stats | No | ✅ | Universal appeal |
| **Superhero API** | Marvel/DC heroes | ✅ 6 powerstats | No | ✅ | Comic fans |
| **Dragon Ball API** | Dragon Ball | ✅ Ki levels | No | ✅ | Anime fans |
| **Rick and Morty API** | R&M characters | ❌ | No | ✅ | Older teens |
| **Studio Ghibli API** | Ghibli films | ❌ | No | ❌ (poster links) | Anime/film fans |
| **The Dog API** | Dog breeds | ⚠️ Some stats | Free key | ✅ | Animal lovers |
| **The Cat API** | Cat breeds | ⚠️ Some stats | Free key | ✅ | Animal lovers |
| **REST Countries** | Countries | ✅ Population, area | No | ✅ Flags | Geography fans |
| **NASA APOD** | Space images | ❌ | Free key | ✅ Stunning | Space fans |
| **Open Library** | Books | ❌ | No | ✅ Covers | Readers |
| **Pokémon TCG API** | Pokémon cards | ✅ HP, attacks | No | ✅ HD cards | Card game fans |
| **Digimon API** | Digimon | ✅ Some stats | No | ✅ | Digimon fans |

**Note:** APIs without numerical stats still work for the catalogue. They just won't support the "Who Would Win?" compare feature as naturally. The catalogue + search + detail view works with all of them.

**Recommendation:** Use PokéAPI as the default for teaching. If a student really wants to use a different API, let them — the Gemini instructions in airules.md should handle it. The concept is the same regardless of the data source.

---

## Teaching Approach

### The Session Arc

1. **Show what an API is** (10 min) — Open a URL in the browser, show raw JSON, explain the concept
2. **Show JSON structure** (10 min) — Walk through a real API response, explain objects, arrays, nesting
3. **Demo a prompt** (10 min) — Show how to ask Gemini to build a catalogue that fetches from the API
4. **Students build** (60 min) — They prompt Gemini to create their catalogue, search, cards
5. **CSS challenge** (20 min) — "Now make it beautiful" — encourage specific, detailed design prompts
6. **Show and tell** (10 min) — Students share their screens, see each other's designs

### The CSS Challenge

This could be framed as a mini-competition: "Who can make the most beautiful catalogue?" Encourage them to be ambitious with their design prompts. Show examples of what's possible:

- Cards that flip on hover to reveal stats on the back
- Parallax scrolling effects
- Glassmorphism (frosted glass) card design
- Neon glow effects on dark backgrounds
- Animated gradient backgrounds
- Cards that tilt based on mouse position (3D effect)

The point is: the AI can implement any visual effect they can describe. **The limit is their imagination, not their coding ability.** This is the purest expression of vibe coding.

---

## Continuity with Previous Weeks

### From Week 2 (Firebase)
- Students could save favourites to Firebase instead of localStorage
- The class could share a "favourite Pokémon" leaderboard
- This reinforces Firebase concepts while learning new ones

### CSS Skills
- Week 1: "make it look fun" (basic)
- Week 2: functional UI for leaderboard
- **Week 3: "make it look professional"** (hover effects, transitions, grid layouts)
- This progression should be highlighted: "look how much better your design skills have gotten in 3 weeks"

---

## Open Questions

- [ ] **One API for everyone or student choice?** Teaching is simpler with one API. Variety is more fun. Could compromise: teach with PokéAPI, allow alternatives.
- [ ] **How much CSS theory?** Students don't need to understand CSS syntax, but knowing terms like "hover effect", "transition", "grid layout" helps them write better prompts.
- [ ] **Compare feature: core or bonus?** If core, it defines the project more strongly as "Who Would Win?" with a catalogue wrapper. If bonus, the focus stays on catalogue + search + beautiful design.
- [ ] **Multi-page or single page?** A catalogue with a detail view could be two separate HTML pages, or a single page that swaps content. Single page is simpler. Multi-page teaches routing concepts.
- [ ] **Persist favourites where?** localStorage is simpler. Firebase connects to Week 2. Both are valid.

---

## Week 3 Template — What It Should Contain

```
week3-catalogue/
├── .idx/
│   ├── dev.nix          ← Same as Week 1 (Python HTTP server, no Node)
│   └── airules.md       ← API context, CSS encouragement, Week 3 objectives
├── README.md            ← Instructions + API reference + CSS challenge ideas
├── index.html           ← Placeholder with project title
├── style.css            ← Minimal reset + CSS variables
└── main.js              ← Empty placeholder
```

The `airules.md` should:
- Explain the API being used (endpoints, JSON structure)
- Encourage beautiful CSS and detailed design prompts
- Maintain vanilla JS constraint (fetch API, no axios/libraries)
- Include examples of CSS effects students can ask for
- Reference Week 3 learning objectives

---

## Success Criteria

By the end of Week 3, students should:

- ✅ Understand what an API is and why it's useful
- ✅ Be able to read a JSON response and identify the data they want
- ✅ Have a working catalogue that searches and displays results from an API
- ✅ Have a detail view for individual items
- ✅ Have invested time in making it visually impressive (hover effects, transitions, layout)
- ✅ Understand the request cycle: user input → API request → JSON response → page update
- ✅ Feel proud of building something that looks and feels like a "real" app
