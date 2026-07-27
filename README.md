# MBMCA Landing Page — On Your Mark Transportation

A landing page built from the two MBMCA ad graphics. Event: Midwest Bus &
Motorcoach Association Conference, South Bend, IN (Hilton Garden Inn),
July 28–29.

## Which file do I use?

| File | Use it for |
|------|-----------|
| `wordpress-custom-html.html` | **Simple route:** one Custom HTML block, built-in form emails Mark via FormSubmit. All CSS namespaced under `.oym`. |
| `avada/` (3 files) | **Avada form route:** the page split so your own Avada form drops into the middle. See below. |
| `index.html` | Standalone full-page version for previewing in a browser. |

## Two ways to build it — pick one

- **Simple / fastest:** paste `wordpress-custom-html.html` into ONE Custom HTML
  block. Uses the built-in form (emails Mark via FormSubmit after a one-time
  activation click). Lead data passes through a third party.
- **Avada form (recommended for keeping data in your stack):** use the three
  files in `avada/`. Lead data stays in WordPress.

### Avada route (3 blocks stacked on the page)

1. **Custom HTML block** = paste `avada/BLOCK-1-top.html`
2. **Shortcode block** = your Avada form shortcode (see `avada/BLOCK-2-form.txt`
   for how to find your form ID and set the notification email to
   mark@onyourmarktransportation.com)
3. **Custom HTML block** = paste `avada/BLOCK-3-bottom.html`

A shortcode will NOT run inside a Custom HTML block, which is why the form gets
its own Shortcode block in the middle.

## Add it to WordPress (3rd-grade steps)

1. Log in to WordPress and go to **Pages → Add New**.
2. Click the **+** to add a block and search for **"Custom HTML"**. Pick it.
   - *What you'll see:* an empty box that accepts code.
3. Open `wordpress-custom-html.html`, **select all**, copy, and **paste** it
   into that box.
4. Click **Preview** (top right) to check it, then **Publish**.
   - *Tip:* pick a **full-width / no-sidebar** page template so the design
     spans edge to edge.

## The form → emails Mark

The form is wired to **FormSubmit.co**, which emails every submission to
**mark@onyourmarktransportation.com** — no plugin or backend required.

**One-time setup:** the FIRST time someone submits the form, FormSubmit sends
Mark a single "Activate" email. He clicks the link once, and from then on every
submission lands in his inbox automatically.

- Change the destination: edit the email in the `<form action="...">` line.
- After-submit redirect: edit the `_next` hidden field (currently points to a
  `/thank-you/` page — create that page or change the URL).
- **Prefer to keep leads in your own stack?** Delete the `<form>` and drop in a
  WordPress form plugin shortcode (WPForms / Fluent Forms) — the surrounding
  styling still applies. This is the more robust, spam-protected option.

## Things to swap in (placeholders)

- **Logo** — search `<!-- LOGO -->`; replace the text logo with your logo image.
- **Mark's photo** — search `<!-- MARK PHOTO -->`; replace the placeholder with
  the cut-out headshot from the ad.
- **MBMCA logo** — search `<!-- MBMCA -->`; swap in the real association logo.

## Buttons

- **Get in Touch with Mark** → jumps to the contact form.
- **Explore Our Services / Learn More** → https://onyourmarktransportation.com/services/

## Brand colors (for rebuilding)

- Navy `#0e2340` · Deep navy `#0a1a30`
- Lime green `#8dc63f` · Dark green `#6fa82f`
- Red (logo accent) `#e4322b`
- Fonts: **Montserrat** (headings/body) + **Kaushan Script** (signature)
