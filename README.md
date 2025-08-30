# Elegant Notes (Notes App)

A lightweight, responsive notes app for quickly capturing ideas, work items, and reminders. Notes are stored locally in your browser (localStorage), so they persist across page reloads without any backend.

## Features

- Add notes with title, content, and a tag
  - Tags: Work, Personal, Ideas, Reminders
- Search notes by title or content (instant filter)
- Filter notes by tag
- Delete notes with a confirmation dialog
- Empty state guidance when there are no notes
- Clean, responsive UI built with vanilla HTML/CSS/JS
- Icons via Font Awesome CDN
- footer

## Project Structure

- `index.html` — App markup (controls, modals, grid)
- `style.css` — Styles for layout, cards, modal, and footer
- `app.js` — App logic (render, add, filter, delete, persistence)

## Getting Started

No build step required. Just open `index.html` in a modern browser.

Optional (recommended): Use a simple local server for best results.

- VS Code Live Server extension
- Or any static server

## Usage

1. Add a note
   - Click “Add”
   - Enter Title and Content
   - Pick a Tag
   - Click “Save Note”
2. Search
   - Type in the search box to filter by title/content
3. Filter by tag
   - Choose a tag from the dropdown (All, Work, Personal, Ideas, Reminders)
4. Delete
   - Click the trash icon on a note
   - Confirm in the dialog

Notes are saved in `localStorage` and load automatically next time.

## Troubleshooting

- “Add” button not opening the modal
  - Ensure `index.html` includes `<script src="./app.js"></script>` at the end of the body
  - Confirm the button has `id="addNoteBtn"`
  - Open DevTools (F12) and check the Console for errors
- Icons not showing
  - Requires internet access to the Font Awesome CDN
  - If offline, replace the CDN link with a locally hosted copy
- Notes disappeared
  - Clearing browser storage or using private browsing can remove localStorage data

## Tech Notes

- Data persistence: `localStorage` (key: `notes`)
- Date formatting: uses `toLocaleDateString` for a simple timestamp on each note
- Accessibility: modal uses an overlay and toggles visibility via `.active`

## Credits

- Font: Google Fonts (Montserrat)
- Icons: Font Awesome

---
Made with ❤ by Digar
