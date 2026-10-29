# Surplus Food Donation Platform — Front-end Prototype

A clickable prototype for a small idea: shops publish the food they have left over, and people who need it reserve a pickup. It is one HTML file, no build step and no dependencies. Just double click it:

```
second-table-ui-prototype v2.html
```

## What is in the prototype

| Screen | What it does |
|---|---|
| Login / role select | Splits donors and recipients, each side sees a different interface |
| My listings / New listing | Publish surplus food: category, quantity, pickup time, address |
| My requests / Collection history | Recipients follow a request (submitted → approved → collected) and see past ones |
| Report an issue | Tell an admin when a pickup went wrong |
| File upload | Click to choose or drag and drop, preview locally before uploading, and remove |

## How the interactions are built

Plain JavaScript, no framework:

- screen switching: `showScreen` / `navTo`
- sub tabs: `toggleSubtab`
- expandable table rows: `toggleDetailRow`
- modals: `openRequestModal` / `closeRequestModal`
- list filtering: `filterReportList`
- drag and drop upload: `handleFileDrop` (with `readAndPreview` for the local preview)

## The write-up

`A10_Speech_Script_CN_EN.md` is a bilingual speech script that goes with the prototype. It explains the scenario, the user flow and the design trade-offs — not code comments, but the "why it is built this way".

## How to run it

Open `second-table-ui-prototype v2.html` in a browser. No server needed.
