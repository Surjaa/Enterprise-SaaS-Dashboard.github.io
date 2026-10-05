# How to use Tempo

A five-minute tour. Follow it in order and you will see every feature.

## 1. Sign in

Click **Use the demo account**. Or type any email (for example `you@company.com`) and a password with 6+ characters. Try leaving the fields empty first to see form validation.

## 2. Meet the pulse (Dashboard)

- The big coloured card shows the **business pulse score**. The chips under it show what moved it.
- Watch the line at the bottom of that card. Within about 10 seconds a **live order** arrives, the line spikes, and the order slides into the Live orders list.
- The bell in the top bar gets a red number. Click it to see the new notification.

## 3. Change the date range

Use **7 days / 30 days / 90 days / Custom** at the top. Every card, chart and the pulse score update. In Custom, pick two dates.

## 4. Use the command palette

Press **Ctrl+K** (Mac: **Cmd+K**), or click the search bar.

- Type `orders` and press Enter to jump to Orders.
- Type `dark` and press Enter to switch theme.
- Ask a question: `top product`, `revenue`, `pending orders`, `low stock`, `churn`. The answer appears at the top.
- Type `accent` to change the colour.

## 5. Work with tables (Customers, Orders, Products, Team)

- **Search** by typing in the box.
- **Filter** with the dropdown (for example Status).
- **Sort** by clicking a column title. Click again to reverse.
- **Page** with the numbered buttons at the bottom.
- **Click a row** (Customers, Orders) to open its details.
- **Add** things with the buttons at the top right. Try submitting an empty form to see errors.
- On Team, change someone's role from the dropdown or remove a member.
- On Orders, **Export CSV** downloads the data.

## 6. Explore Analytics

Three tabs: **Overview** (traffic, channels, categories), **Audience** (sign-ups and a busiest-hours heatmap), **Funnel** (how visitors become buyers). Hover any chart for a tooltip.

## 7. Messages

Pick a conversation, send a message and wait a second for a reply.

## 8. Settings

- **General:** rename the workspace (validated).
- **Appearance:** light, dark or system theme; four accent colours; comfortable or compact spacing.
- **Notifications:** switches that save instantly.
- **Security:** the password form checks length, a number, and that both entries match.
- **API:** copy or roll a demo key.

## 9. Billing, Subscription, Help

- Billing: invoices (searchable, with download) and a card form with validation.
- Subscription: toggle monthly / yearly, switch plans, cancel.
- Help: search the FAQ, filter by topic, open and close answers.

## 10. Layout controls

- The **menu button** at the top left collapses the sidebar (on a phone it opens it). The choice is remembered.
- The **sun / moon button** switches theme.
- The **avatar menu** opens Profile, Settings, Billing and Sign out.

## Keyboard shortcuts

| Keys | Action |
| --- | --- |
| `Ctrl/Cmd + K` | Command palette |
| `g` then `d` | Dashboard |
| `g` then `a` | Analytics |
| `g` then `c` | Customers |
| `g` then `o` | Orders |
| `g` then `p` | Products |
| `g` then `t` | Team |
| `g` then `s` | Settings |
| `[` | Collapse / expand sidebar |
| `?` | Show shortcuts |
| `Esc` | Close dialogs and menus |

## Troubleshooting

- **Page looks unstyled:** make sure the `css/` and `js/` folders sit next to `index.html`.
- **Want to start fresh:** open the browser console and run `localStorage.clear()`, then refresh.
- **Fonts look different:** they load from Google Fonts and need internet. Offline, system fonts are used.
