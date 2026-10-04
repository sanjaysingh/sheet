# Offline Spreadsheet

Offline Spreadsheet is a small grid for entering values and formulas, then downloading the sheet as `.xlsx`. It runs entirely in the browser.

**Live app:** https://sheet.sanjaysingh.net

## What it does

- Edits cells in a grid. The formula bar shows the formula or value of the active cell.
- Evaluates formulas that start with `=`. Cell references such as `A1` are substituted, then the expression is calculated.
- Recalculates formula cells when the sheet changes.
- Downloads the current grid as `spreadsheet.xlsx`. A cell that has a formula exports the formula; otherwise it exports the value.

This is a single-sheet editor. It does not load an existing workbook, and formula support is arithmetic rather than a full Excel function set.

## Privacy

The grid stays on the page until you export it. Nothing is uploaded.

## Run locally

Open `index.html` in a browser. Vue, Tailwind, and SheetJS are vendored under `libs/`. Grid and formula-bar components live in `components/`. No install or build step is required.

## Deploy

Commits that land on `main` deploy to GitHub Pages at https://sheet.sanjaysingh.net. Changes reach `main` through a pull request.
