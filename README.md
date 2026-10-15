# ASTERICA 2026 website

Open `index.html` in your browser to view the site. The 45 PreFest tiles each open a dedicated event details page. The pages share one design template, and each event has its own address, such as `prefest-event.html?event=PreFest1`.

## Current details

- Fest: ASTERICA 2026 — The Carnival
- College: College of Medicine and Sagore Dutta Hospital, Kolkata
- Dates: 20–22 December 2026
- Contact: cmsdh.asterica@gmail.com
- Official college website: https://comsdh.org.in/

## Add details for a PreFest event later

1. Open `prefest-event.html` in a text editor.
2. Find `const eventDetails = {};` near the bottom.
3. Add an entry for the matching tile inside the braces. For example:

```js
const eventDetails = {
  PreFest1: {
    title: "Quiz Carnival",
    summary: "A lively team quiz for students across campus.",
    date: "December 12, 2026 · 2:00 PM",
    venue: "College auditorium",
    registration: "Registration opens soon",
    note: "Teams of three. Full rules will be announced shortly.",
    registrationUrl: "https://example.com/registration"
  }
};
```

Replace the example details with the confirmed information. To update another tile, add another entry separated by a comma, using its exact key such as `PreFest2`. Leave out `registrationUrl` until you have a real registration link. Each tile already opens the matching details page.

## Website files

- `index.html` contains the home page, pre-fest listing, main events, and navigation.
- `prefest-event.html` is the reusable event details page. Its `eventDetails` object is where each event's information is added.
- Keep the ASTERICA and college logos and the 3D poster in the `assets` folder. The main hero uses `ASTERICA-2026-3D-poster.png`.

The site is static and can be hosted on GitHub Pages, Netlify, or another static hosting service. It uses Google Fonts when online and falls back to installed fonts when offline.
