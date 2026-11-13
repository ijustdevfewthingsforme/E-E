# Elliot Air · EA0312 to Phuket

Drop the `phuket` folder into your existing GitHub Pages repo, next to the date-night `index.html`.
The page will then live at `https://elliotair.com/phuket/`.

## Before sending the link

Open `phuket/index.html` and edit the `TRIP` block at the top of the `<script>`:

```js
const TRIP = {
  ...
  departTime: "",   // e.g. "09:40" (Kuala Lumpur time). Empty = TBD, countdown aims at 09:00
  returnTime: "",   // e.g. "18:15"
  pdf: ""           // link to the e-ticket PDF
};
```

**The PDF link**, either:
- put the PDF in the `phuket` folder (e.g. `ticket.pdf`) and write `pdf: "ticket.pdf"`, or
- paste a share link (Google Drive set to "Anyone with the link", Dropbox…).

Note: on GitHub Pages a PDF in a public repo can be found by anyone who has the address. If the ticket shows booking references or passport details, a private Drive link is safer.

Then replace `https://elliotair.com/phuket/og-image.png` (the `og:image` line) with your real domain.

## Optional: new voice announcement

Record a new captain message, put it in `phuket/` (MP3), and set `const CAPTAIN_AUDIO = "captain-phuket.mp3";`.
While it's empty, the speaker button stays hidden.

## After the trip

In the next trip's page, add Phuket to the `PREVIOUS_FLIGHTS` list:

```js
{code:"EA0312", date:"3–6 Dec 2026", dest:"Phuket"},
```
