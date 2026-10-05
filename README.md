# Enterprise SaaS Dashboard: a commerce dashboard with a heartbeat

Tempo is a B2B SaaS dashboard built with plain HTML, CSS and JavaScript. No frameworks, no chart libraries, no build step. Open `index.html` and it runs.

Most dashboards show numbers. Tempo also shows how the business *feels*: a live pulse line speeds up whenever an order arrives, and one score summarises the health of the business.

## What makes it different

| Feature | What it does |
| --- | --- |
| **Business pulse** | A 5 to 99 score built from revenue growth, conversion change, churned customers and unpaid orders. |
| **Live heartbeat** | A line in the top bar and on the dashboard that spikes when a new order arrives. Bigger orders make bigger spikes. |
| **Live orders** | A new order lands every 7 to 13 seconds. It appears in the live list, the activity timeline, the orders table and the notification bell. |
| **Command palette** | Press `Ctrl+K` (or `Cmd+K`) to jump to any page or run any action. |
| **Ask Tempo** | Type a plain-English question in the palette ("top product", "revenue", "low stock") and get an answer from the data. |
| **Hand-made charts** | Line, bar, donut, heatmap, funnel and a tile-map are all drawn with SVG by about 100 lines of code. |
| **Accent colours** | Four brand colours that restyle the whole app, in both light and dark mode. |
| **Keyboard shortcuts** | `g` then `d`, `a`, `c`, `o`, `p`, `t`, `s` to navigate. `[` collapses the sidebar. `?` lists everything. |

## Pages (15 views)

Login, Dashboard, Analytics (3 tabs), Customers, Orders, Products, Team, Notifications, Messages, Settings (5 tabs), Your profile, Billing, Subscription, Help center. A customer or order detail opens in a modal.

## JavaScript features

Filters, search, sorting, pagination, modal windows, dropdowns, tabs, notifications, dynamic charts, form validation, remembered sidebar state, and light / dark / system theme switching. Date-range filtering (7, 30, 90 days or custom dates) changes every chart, KPI and the pulse score.

## Project structure

```
tempo-dashboard/
  index.html            page shell: login screen, sidebar, top bar
  css/
    styles.css          design tokens, layout, components, responsive rules
  js/
    app.js              data, charts, tables, router, pages, interactions
  docs/
    HOW-TO-USE.md       a guided tour
    EXPLAIN-SIMPLY.md   how to describe the project to anyone
  README.md             this file
```

## Run it

1. Unzip the folder and keep the structure as it is.
2. Double-click `index.html`. That is all.

Optional: for a local server, run `npx serve .` or `python -m http.server` in the folder.

Login: use any valid email and a password of 6+ characters, or click **Use the demo account**.

## Deploy for free (GitHub Pages)

1. Create a repository and upload these files.
2. Go to Settings, then Pages, and choose the main branch.
3. Your site is live at `https://YOUR-NAME.github.io/REPO-NAME/`.

## How the code is organised (app.js)

1. Helpers and storage
2. Fake data (seeded random, so it looks the same every time)
3. Icons
4. State, theme, toasts, modals, dropdowns, form validation
5. Charts
6. Reusable data table
7. Live pulse engine
8. Command palette and Ask Tempo
9. Pages (each page is an object with `render()` and `init()`)
10. Router, login, start-up

## Accessibility

Visible keyboard focus, labelled controls, `aria-sort` on tables, dialogs with focus return, `Esc` to close, and `prefers-reduced-motion` respected.

## Ideas to extend it

- Replace the fake data in `app.js` with a real API using `fetch()`.
- Add drag-to-reorder dashboard cards.
- Add a "compare two products" view.
- Save the date range in the URL.

## Notes

This is a front-end demo. Login is simulated, the card form stores nothing, and preferences live in your browser's `localStorage`. Fonts load from Google Fonts; without internet the app falls back to system fonts.
