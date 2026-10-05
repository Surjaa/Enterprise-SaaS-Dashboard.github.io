# How to explain Tempo in simple language

## The 15-second version

"Tempo is a dashboard that a company uses to watch its sales, customers and orders. I built it with plain HTML, CSS and JavaScript. It has a live heartbeat that speeds up when an order comes in, and you can ask it questions like 'what is my top product?'"

## The 1-minute version

"Companies need one place to see how their business is doing. I built Tempo, a full dashboard with 15 screens: login, charts, customers, orders, products, team, messages, billing and settings.

What makes it different is the **pulse**. Instead of only showing numbers, it gives the business a health score and a live heartbeat line that reacts to new orders. It also has a command palette: press Ctrl+K, type a question in normal words, and it answers from the data.

I made every chart by hand with SVG and used no libraries, so I understand how everything works."

## An everyday comparison

Think of a car dashboard. The speedometer, fuel gauge and warning lights tell the driver what is happening without opening the engine. Tempo is that dashboard for a shop. The pulse score is like the "engine health" light, and the live line is like the sound of the engine.

## What each part does (plain words)

| Part | In simple words |
| --- | --- |
| HTML (`index.html`) | The skeleton. It holds the empty frame: sidebar, top bar, login screen. |
| CSS (`styles.css`) | The clothes. Colours, spacing, light and dark mode, and how it looks on a phone. |
| JavaScript (`app.js`) | The brain. It makes the data, draws the charts, handles clicks, and fills in each page. |
| Fake data | Made-up customers and orders so the app has something to show. A "seeded" generator makes sure it is the same every time. |
| Router | The page switcher. The part of the web address after `#` decides which screen shows, without reloading the page. |
| localStorage | A small notebook in your browser. It remembers your theme, colour and sidebar choice. |

## How some features work

**Search, sort, filter, pagination.** One reusable table function does all four. It takes the full list, removes rows that do not match the search or filter, orders what is left, then shows only one page of it. Every table in the app uses it.

**Charts.** A chart is a list of numbers turned into shapes. The code works out where each point goes on the screen and draws a line or a bar with SVG. When the window changes size, the chart redraws.

**Dark mode.** All colours are stored as named variables, like `--surface` and `--ink`. Dark mode just swaps the values of those variables, so nothing else needs to change.

**The live pulse.** Every 450 milliseconds the app adds a new point to a line. Normally the point is low and calm. When an order arrives, the next points jump up and then fade back down, like a heartbeat.

**Form validation.** Before saving, each field is checked against rules ("required", "must look like an email", "at least 8 characters"). If something is wrong, a clear message appears under that field and the cursor moves there.

**Ask Tempo.** It is not AI. It looks for keywords in your question ("revenue", "stock", "churn") and calculates the answer from the data. It is simple on purpose, and easy to extend.

## Questions an interviewer might ask

**Why no React or chart library?**
"I wanted to show I understand the fundamentals first: the DOM, events, state, and SVG. A framework would be the next step for a bigger app."

**How would you connect it to a real backend?**
"I would replace the fake data arrays with `fetch()` calls to an API, then call the same render functions with the real results."

**How did you make it accessible?**
"Visible keyboard focus, labelled buttons and inputs, `aria-sort` on table headers, dialogs that return focus when closed, Escape to close, and reduced-motion support."

**What was the hardest part?**
"Making one table component flexible enough for four different pages, and making charts that redraw correctly when the window or sidebar size changes."

**What would you improve next?**
"Real data from an API, automated tests, drag-and-drop dashboard cards, and saving the date range in the URL."

## Talking points for a portfolio

- 15 screens, one codebase, zero dependencies.
- A signature idea (the pulse) instead of a copied template.
- Works on desktop and mobile, in light and dark mode.
- Keyboard-first: command palette and shortcuts.
- Every feature in the brief is covered: filters, search, sorting, pagination, modals, dropdowns, tabs, notifications, dynamic charts, form validation, sidebar state and theme switching.
