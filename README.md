# Alareo Leadership — website

A single-page marketing site for Alareo Leadership, an executive coaching and
leadership-development business based in Bray, Co. Wicklow, Ireland. Founded by
Aideen Cardiff.

This is a plain static site: one `index.html`, no build step, no framework, no
dependencies to install. Open `index.html` in a browser to preview.

## File structure

```
alareo-site/
├── index.html                 # the whole site (HTML + CSS + a little JS, inline)
├── assets/
│   ├── logo.png               # Alareo logo (transparent PNG)
│   └── aideen-cardiff.jpg     # founder headshot
└── README.md
```

## Brand

Palette is drawn from the logo — sage green + deep navy.

| Token        | Hex       | Use                                  |
|--------------|-----------|--------------------------------------|
| ink (navy)   | `#1f2d3b` | body text, dark sections             |
| ink-soft     | `#4a5a69` | secondary text                       |
| green        | `#4f8070` | accents, the three-bar motif         |
| green-deep   | `#2f5145` | buttons, links, headings on light    |
| paper        | `#f5f4ed` | page background                       |
| sage         | `#e7ede8` | alternating section background       |

Type: **Newsreader** (serif, headings) + **Hanken Grotesk** (sans, body),
loaded from Google Fonts. The logo's three ascending bars recur as a small CSS
motif (`.mark`) — keep using that rather than adding new decoration.

Design intent: calm, credible, lots of whitespace ("space to think"). Avoid
busy card grids and heavy effects.

## What's on the page

- Hero (mission statement)
- Approach — the moment leaders are in + what coaching supports
- Three offers — Executive Coaching, LEAF programme, Pause en Provence
- About Aideen (headshot + credentials)
- Testimonials (two, both cleared for publication)
- Team (Aideen, Declan Whittle, Geraldine)
- Contact (details + demo form)

## Still to do / confirm

- [ ] **Declan Whittle** — surname added; still need a short mediation profile.
      Currently a placeholder card marked "profile to follow."
- [ ] **Pause en Provence** — no real content yet. Shown with an "In development"
      badge and placeholder copy. Flesh out when details exist.
- [x] **Contact email** — `aideen.cardiff@alareo.ie`.
- [ ] **Contact form is a stub.** A static file can't send email on its own.
      Either wire it to a form service (e.g. Formspree) or replace with a
      `mailto:` button.
- [ ] **Stuart's testimonial** — deliberately left out; he hasn't confirmed
      permission to publish. Add only once cleared.
- [x] Remove the yellow-ish "Demo preview" bar (`.demobar`) before going live.
- [x] Contact form uses `mailto:aideen.cardiff@alareo.ie` until a form service is wired.

## Deploying to Blacknight

Static hosting — just upload the folder contents.

1. Have a domain **and** a hosting package on Blacknight.
2. Open File Manager (or connect via FTP / FileZilla).
3. Upload `index.html` and the `assets/` folder into the web root:
   `httpdocs` (Plesk plans) or `public_html` (cPanel / WordPress plans).
   Delete the default holding page (`index.php`) if present.
4. **Enable the free SSL certificate** (Let's Encrypt, included) so the site
   loads over HTTPS — otherwise browsers show a "Not secure" warning.

## Contact / business facts (for reference)

- Founder: Aideen Cardiff — Founder & Executive Coach
- Location: Glenard, Meath Road, Bray, Co. Wicklow, A98 XC92
- Email: aideen.cardiff@alareo.ie
- Phone: +353 87 121 9003
- LinkedIn: https://www.linkedin.com/in/aideen-cardiff-b489a86/
- LEAF programme co-delivered with Geraldine Murphy (Evolution Partners)
