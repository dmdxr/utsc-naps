# Newton's Apples Physics Society

The official website of **Newton's Apples Physics Society (NAPS)**, a student-run physics society at the University of Toronto Scarborough. We're open to every student, in every program, and on every campus!

The site covers our upcoming and past events, the annual undergraduate physics conference, the team, and how to join.

[Instagram](https://www.instagram.com/utsc_naps/) · [Email](mailto:utsc.naps@seds.ca)

---

## Features

- **Deep-space theme** with a graph-paper grid, a starfield, and a slowly rotating orbital diagram in the hero
- **Dark and light mode** with a toggle in the header
- **Fully responsive**, including a collapsing mobile nav
- **Event cards** with date tiles, meta info, difficulty tags, and optional RSVP buttons
- **Google Form embeds** for membership and conference signup
- **Accessible**: keyboard focus styles and `prefers-reduced-motion` support
- **No build step**: plain HTML, CSS, and a little JavaScript

## Project structure

```
.
├── index.html          # Home
├── about.html          # About the club
├── events.html         # Upcoming and past events
├── conference.html     # Undergraduate physics conference
├── team.html           # Executive team
├── join.html           # Membership signup
└── assets/
    ├── css/style.css   # All styling and theme variables
    ├── js/main.js      # Theme toggle, mobile nav, footer year
    └── img/            # Logo and images
```

## Running locally

No dependencies or build tools are needed. Clone the repo and open `index.html` in your browser, or serve it locally:

```bash
git clone https://github.com/<your-username>/<your-repo>.git
cd <your-repo>

# any static server works, for example:
python3 -m http.server 8000
```

Then visit <http://localhost:8000>.

## Making common updates

### Adding an event

In `events.html`, copy an existing card into the **Upcoming** section:

```html
<div class="event">
  <div class="event-date"><div class="mon">Oct</div><div class="day">09</div></div>
  <div class="event-body">
    <h3>Event Title</h3>
    <p>Short description</p>
    <div class="event-meta"><span>🕕 5:00 PM – 7:00 PM</span><span>📍 Room</span></div>
    <div class="tags"><span class="tag">Social</span><span class="tag">Introductory</span></div>
  </div>
</div>
```

Once an event has happened, move it to **Past events** and add the `past` class (`class="event past"`).

Tags describe the physics background an event assumes (for example `Introductory`) and its type (for example `Social`, `Workshop`).

### Add an RSVP button to an event

Put an RSVP link inside the event's heading:

```html
<h3>Event Title <a class="rsvp-tab" href="YOUR_GOOGLE_FORM_LINK" target="_blank" rel="noopener noreferrer">RSVP →</a></h3>
```

### Re-theme the site

All colours, fonts, radii, and widths live in the `:root` block at the top of `assets/css/style.css`. Light mode overrides are in the `[data-theme="light"]` block directly below it.

| Variable | Purpose |
| --- | --- |
| `--accent` | Primary colour (periwinkle) |
| `--accent-2` | Secondary colour (teal) |
| `--gold` | Highlight colour, used sparingly |
| `--bg`, `--surface`, `--border` | Backgrounds and borders |

### Type system

| Role | Font | Used for |
| --- | --- | --- |
| Serif | Newsreader | Headings |
| Sans | Inter | Body copy |
| Mono | IBM Plex Mono | Dates, times, tags, labels |

## Deployment

The site is hosted on **GitHub Pages**. To deploy your own copy:

1. Push the repo to GitHub.
2. Go to **Settings → Pages**.
3. Under **Source**, choose the `main` branch and the `/ (root)` folder.
4. Save. The site will be live at `https://<your-username>.github.io/<your-repo>/` after a minute or so.

## Contributing

Team members and club volunteers are welcome to help keep the site up to date.

1. Create a branch: `git checkout -b update-events`
2. Make your changes and preview them locally
3. Commit with a clear message: `git commit -m "Add November movie night"`
4. Push and open a pull request

For anything else, email us at [utsc.naps@seds.ca](mailto:utsc.naps@seds.ca).

## License

Club name, logo, and photos remain the property of Newton's Apples Physics Society.

---

<sub>Built by Debmita Majumdar, hosted on GitHub Pages.</sub>
