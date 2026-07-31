# Grist Task Board

A single-file [Grist](https://www.getgrist.com/) Custom Widget that turns any table into a drag-and-drop Kanban-style task board, grouped by a Status (Choice) column.

## Features

- **Kanban board** — one column per Status choice, in the same order and colors configured on the Status column itself.
- **Drag and drop** — drag cards between status columns to update the Status field (desktop/mouse only).
- **Task popup editor** — click a card to open a side panel with every mapped field, editable in place. Supports Text, Choice, ChoiceList, Reference, ReferenceList, Date, DateTime, Checkbox and Attachments columns.
- **Card badges** — Priority and Team show as colored badges on the card; Location shows as card metadata.
- **Bins** — configurable toolbar pills (e.g. Completed, Cancelled, Duplicate) for statuses you'd rather keep off the board. Drag a card onto a bin to set its status, or click a bin to open a configured link. Desktop only.
- **Board settings panel** — add, edit, or remove bins (label, matching status value, optional link URL) from the gear icon in the toolbar.
- **Attachments** — upload files, paste an image directly (Ctrl+V) into an attachment field, view images in a lightbox, and remove attachments.
- **Create / delete tasks** — add a task directly into a status column with the `+` button, or delete the open task from its popup.
- **Undo** — Ctrl+Z / Cmd+Z steps back through the last 20 field or status edits made in this widget.
- **Read-only fields** — map extra columns (e.g. Modified date, Created by) to show as reference info in the popup without being editable.
- **Responsive** — on phones/touch devices the toolbar, bins, and drag-and-drop are hidden in favor of a full-screen popup with a Status dropdown.
- **Light/dark theme** — follows the system color scheme automatically.

## How to use

1. In Grist, open the page you want the board on, add a **Custom Widget Builder**, and paste the contents of **widget.html** into it, press preview, followed by save.
3. Grant the widget **Full document access** when prompted (it needs this to read/write records and manage attachments).
4. In the widget's column mapping panel, map:
   - **Title** — the task name column.
   - **Status** — a Choice column defining the board's columns.
   - **Location**, **Team**, **Priority** — optional columns shown on the card.
   - **Additional fields** — any other columns you want editable in the task popup.
   - **Read-only fields** — any columns you want shown in the popup but not editable (e.g. Modified date).
5. Click the gear icon in the toolbar to configure bins for statuses you want to keep off the main board.

No build step or dependencies to install — it's a single HTML file that loads the Grist Plugin API and SortableJS from a CDN at runtime.
