# Alareo Leadership website
 
Single-page website for **Alareo Leadership**: executive coaching, leadership team
development and mediation, based in Bray, Co. Wicklow. Founded by Aideen Cardiff.
Tagline: *Human, on Purpose.*
 
This is a plain static site: one `index.html` (HTML, CSS and a little JavaScript, all
inline) plus an `assets/` folder. There is no build step, no framework and nothing to
install. Open `index.html` in a browser to preview it.
 
This README is the standing brief for anyone editing the site, including AI tools such as
Cursor or Claude. **Read "Rules for editing" before changing anything.**
 
## Rules for editing
 
1. **Aideen's wording is final.** Use her copy exactly as supplied. Don't rewrite,
   shorten, "improve" or add marketing language unless asked. Only fix obvious typos,
   and list every fix you make.
2. **No dashes in the copy.** Never use em dashes (—) or en dashes (–) in visible text,
   including the page title and alt text. Use a comma, colon or full stop instead.
   Hyphens are fine inside words and ranges (decision-making, 2025-26).
3. **Irish/UK spelling:** organisation, programme, judgement, wellbeing, centre.
4. **Keep the design consistent.** Don't add new fonts, colours, icon libraries,
   animations, frameworks or build tools. Reuse the existing classes and CSS variables.
   The three-bar motif (`.mark`) and the growing-leaf drawing (`bg-leaf-art.svg`) are the
   only decoration.
5. **Inline only.** Keep CSS and JS inline in `index.html`. The only outside services are
   Google Fonts (until the fonts are self-hosted) and the Formspree form endpoint.
6. **This repo is public.** Never commit private information: a home address, client
   names, a client's employer, passwords, API keys or private notes. The Formspree form
   ID is designed to be public, so that one is fine.
7. **Testimonials:**
   - **Every testimonial is important to Aideen.** Never drop, shorten or reword one.
   - **No personal names for now.** Each quote shows only its role line (see
     "Testimonials" below). Names are added only when Aideen confirms each person is
     happy to be named.
   - Never add an employer or organisation the person didn't write themselves.
8. **Partners:** describe Geraldine Murphy only as a former bio-pharma CEO and company
   founder. **Never name her companies, past or present.**
9. **Names and places:**
   - The retreat is always *Pause en Provence*, in italics (no "Une").
   - The location is only ever "Bray, Co. Wicklow".
10. **Images:**
    - When you replace an image, give the new one a new filename (browsers cache old
      ones).
    - Strip location data from phone photos. iPhone photos include GPS by default.
    - Keep files within the sizes under "Images".
11. **Check before you commit:**
    - view the page at phone width (390px), small laptop (1024px) and laptop (1366px)
    - no sideways scrolling
    - the mobile menu opens and closes, and isn't hidden behind the header
    - every image loads
    - no `—` or `–` anywhere in the visible text
## File structure
 
```
alareo-site/
├── index.html
├── assets/
│   ├── logo-full.png           # full logo incl. tagline (transparent PNG)
│   ├── favicon.svg             # browser tab icon (three bars)
│   ├── og-image.jpg            # preview image when the link is shared (1200x630)
│   ├── aideen-hero-square-v2.jpg  # top of page: square photo of Aideen (outdoors)
│   ├── aideen-desk-v3.jpg         # About section (rectangle)
│   ├── aideen-team-circle.jpg     # Team section (circle, pre-cropped square)
│   ├── declan-team-circle.jpg     # Team section (circle, pre-cropped square)
│   ├── geraldine-murphy.jpg       # Team section (circle). From the first version of the site: keep it
│   ├── bg-leaf-art.svg            # growing-leaf drawing (behind the top photo, and on the LEAF card)
│   ├── bg-bray-sunset.jpg         # Bray photo band
│   ├── card-coaching-sea.jpg   # Executive Coaching card
│   ├── photo-mediation.jpg     # Mediation card (to source; placeholder until then)
│   └── photo-provence.jpg      # Pause en Provence card (to source; placeholder until then)
├── .htaccess                   # Blacknight server settings (not used by GitHub Pages)
└── README.md
```
 
Working files that are not part of the site, such as the Cursor prompt file, stay out of
git. They're listed in `.gitignore`.
 
## Brand
 
The palette is drawn from the logo: sage green and deep navy.
 
| Token        | Hex       | Use                                  |
|--------------|-----------|--------------------------------------|
| ink (navy)   | `#1f2d3b` | body text, dark sections             |
| ink-soft     | `#4a5a69` | secondary text                       |
| green        | `#4f8070` | accents, the three-bar motif         |
| green-deep   | `#2f5145` | buttons, links, headings on light    |
| paper        | `#f5f4ed` | page background                      |
| sage         | `#e7ede8` | alternating section background       |
 
- **Type:** Newsreader (serif, headings) and Hanken Grotesk (sans, body).
- **Tagline:** written "Human, on Purpose." in text, to match the logo.
- **Photo shapes:**
  - top-of-page photo of Aideen: square, 6px corners
  - About photo: rectangle (4:5)
  - team photos: circles (176px, thin sage ring), using pre-cropped square images
- **Design intent:** credible and warm, with plenty of space ("space to think"). The
  page uses photos generously, but every section still has a clear heading and room to
  breathe.
## Page structure (top to bottom)
 
| # | Section | id | Background |
|---|---------|----|------------|
| 1 | Header: logo, nav, "Book a chemistry call" button | | white |
| 2 | Hero: eyebrow, headline, intro, buttons; square photo of Aideen with the growing leaf behind its top-left corner and a quote card over its bottom-right corner | | paper |
| 3 | Key facts strip (three facts) | | white |
| 4 | Bray photo band: "The human qualities..." + button | | photo |
| 5 | The moment leaders are in | `moment` | paper |
| 6 | Human, on Purpose (philosophy and three levels) | `philosophy` | sage |
| 7 | Four ways to work together (white cards with a picture on top and "Read more") | `offers` | paper |
| 8 | For organisations | `organisations` | ink |
| 9 | About Aideen: photo, full bio, credentials | `about` | paper |
| 10 | Testimonials: one featured, the rest in a grid | `voices` | sage |
| 11 | Team: Aideen (short bio), Declan, Geraldine, all in circles, with "Read full bio" | `people` | ink |
| 12 | Contact: booking card, contact details, form | `contact` | paper |
| 13 | Footer: wordmark, tagline, location | | ink |
 
Aideen appears twice: the full bio and credentials in **About**, and the shorter
coaching bio in **Team**.
 
## Testimonials
 
The order is fixed. People who gave their name come first; anonymous quotes come last.
 
| # | Where | Role line shown on the site |
|---|-------|-----------------------------|
| 1 | Featured (and its first sentence in the top-of-page quote card) | Partner at Law |
| 2 | Grid | Coaching client, Health & Safety Authority |
| 3 | Grid | Senior Manager, Consulting sector |
| 4 | Grid | *(second new testimonial, to come; goes here when it arrives)* |
| 5 | Grid | Executive coaching client |
| 6 | Grid | Executive coaching client |
 
- **Grid:** two columns on laptops and one on phones. If the grid has an odd number of
  quotes, the last one spans the full width.
- **Names** are kept privately by Fionn and added only when Aideen confirms.
## Contact and booking
 
- **Chemistry call:** a 15-minute intro call. The "Book a chemistry call" buttons
  (header, hero, contact section) all use one setting, `BOOKING_URL`, at the top of the
  script. Paste Aideen's Microsoft Bookings page link there. While it's empty, the
  buttons scroll to the contact form instead, and the booking card is hidden.
- **The contact form** sends messages straight to Aideen's inbox through Formspree, so
  visitors don't need an email app. To set it up:
  1. Create a Formspree form for aideen.cardiff@alareo.ie.
  2. Put the form ID in the form's `action` (replace `FORM_ID`).
  3. Send a test message and check it arrives.
  When Aideen clicks Reply, it goes to the visitor. A hidden `_gotcha` field catches
  spam bots.
- **If the site is hosted on Blacknight with `.htaccess`:** add `https://formspree.io` to
  `form-action` and `connect-src` in the Content-Security-Policy line, or the form will
  be blocked.
The band uses bg-bray-sunset.jpg, chosen by Aideen.
## Images
 
| Image | Recommended size | Budget |
|-------|------------------|--------|
| Band photo | landscape, 2400px wide | about 300 KB |
| Card photos | landscape 16:9, 1600px wide | about 200 KB |
| Portraits | 700 to 1000px wide | about 200 KB |
| Logo | as supplied (PNG, transparent) | about 50 KB |
 
Phone photos: export as JPEG (not HEIC), resize, and strip location data before adding
them. Stock photos must be free for commercial use (Unsplash and Pexels are).
 
## Updating the site
 
1. Edit on your laptop, never in the hosting file manager. The GitHub copy is the master.
2. Preview locally, then commit and push to GitHub.
3. The push deploys automatically. Today that's GitHub Pages. On Blacknight it will be
   Plesk's Git deployment, set to automatic, with GitHub's webhook pointing at Plesk.
## Going live on Blacknight
 
1. Upload `index.html`, `assets/` and `.htaccess` into the web root (`httpdocs`, or
   `public_html` on cPanel plans). Delete the default holding page. Don't upload
   `README.md`.
2. Turn on the free SSL certificate and the HTTP to HTTPS redirect. Check the site loads
   with and without `www`.
3. **Email check:** the website and Aideen's Microsoft 365 email share the same domain
   settings. After setting up hosting, confirm the MX (mail) records still point at
   Microsoft and that Blacknight's own mail service is off for the domain.
4. Once the Blacknight site is live, make this repo private. It has to be in that order,
   because GitHub Pages stops serving a private repo on a free plan. For automatic
   deploys from a private repo, add Plesk's SSH key to the repo as a deploy key.
## Open items
 
- [x] Aideen to choose the Bray band photo (`?band=` previews)
- [ ] Testimonial 4: waiting on the second new testimonial
- [ ] Names on testimonials: waiting on Aideen
- [ ] Source the Mediation and Pause en Provence card photos (Aideen's own Provence photos preferred)
- [ ] Set up Microsoft Bookings (15-minute chemistry call) and paste the link into `BOOKING_URL`
- [ ] Create the Formspree form, add its ID and send a test message
- [ ] Self-host the two Google Fonts (privacy) before launch
- [ ] Optional: client logos, only with each organisation's permission
## Business details (all public on the site)
 
- Email: aideen.cardiff@alareo.ie
- Phone: +353 87 121 9003
- LinkedIn: https://www.linkedin.com/in/aideen-cardiff-b489a86/
- Location: Bray, Co. Wicklow
- LEAF programme co-delivered with Geraldine Murphy (former bio-pharma CEO and company founder)
- Mediation with Declan Whittle, Barrister-at-Law
 