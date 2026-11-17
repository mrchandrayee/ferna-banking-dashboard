# Ferna — Banking Dashboard

[![Live Demo](https://img.shields.io/badge/Live%20Demo-GitHub%20Pages-blue?style=for-the-badge&logo=github)](https://mrchandrayee.github.io/ferna-banking-dashboard/)
[![HTML](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org) [![CSS](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org) [![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](./LICENSE)

A runnable, responsive vanilla HTML/CSS/JavaScript recreation of the supplied 7.57-second screen recording.

## Run it
1. Extract `ferna-banking-dashboard.zip`.
2. Open `index.html` in Chrome, Edge, Firefox or Safari.

No npm, build step, database or external API is required.

Optional local server:
```bash
python3 -m http.server 8000
```
Open `http://localhost:8000`.

## What is recreated from the video

The recording title is **Banking Dashboard 💶**. The product shown is **Ferna — Money for freelancers**. The visible greeting is **Good morning, Inês** and the date shown is Thursday 19 November.

### Overview / Your money
- Total money: €47,602.46
- Safe to spend: €4,409
- Cash flow chart with In / Out / Balance / Forecast legend
- November 2026 in / out / net summary
- Expense categories: Rent & bills, Travel, Camera & gear, Groceries
- Overview shortcuts for Accounts & pots, Cards and Upcoming payments

### My cards
- Everyday physical card ending 4417
- Studio physical card ending 9023
- Card selection, freeze / unfreeze, show details, copy number feedback
- Monthly spending limit slider
- Online payments and cash withdrawal toggles
- Recent transactions paid with the selected card
- Create virtual card demo

### Accounts & pots
- Accounts: Everyday, Studio and Tax reserve, with balances and statement / move actions
- Pots tab with Flat deposit, Rainy-day fund, New 70mm lens and Holiday savings goals
- Circular savings progress and Add / Take out actions

### Other navigation
- Activity transaction list with search and CSV export
- Insights summary
- Scheduled Payments
- Budgets
- Invoices

Also includes sidebar navigation, collapsible sidebar, dark mode, keyboard search shortcut (Ctrl/⌘ + K), transfer/request forms, responsive layout and toast feedback.

## Visible source fragment in the recording
The code panel is labelled `src/card.tsx` and shows a React `useLayoutEffect` that:
- returns early when the frozen state has not changed,
- updates a `wasFrozen` ref,
- skips the animation if a frost ref is absent or reduced motion is enabled,
- uses GSAP `fromTo` to animate `clipPath` from `circle(0% at 88% 12%)` to `circle(150% at 88% 12%)` when freezing,
- reverses opacity / clears the opacity property when unfreezing,
- uses `power3.out` and `power2.in` easing.

The recording only exposes this small code excerpt; the original complete React source is not visible. This project recreates the displayed UI and practical interactions in vanilla HTML/CSS/JS, rather than claiming to reproduce unseen original files.

## Demo limitations
All balances, cards, transactions, accounts, pots, payments and invoices are sample data. Buttons and forms simulate actions in the browser only. There is no bank connection, payment processor, card network, authentication, secure storage, actual transfer, or live financial data. Do not enter real banking credentials or card details.

## 👨‍💻 Author

**mrchandrayee** · [GitHub](https://github.com/mrchandrayee)

## 📄 License

[MIT License](./LICENSE)
