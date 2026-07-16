# श्री जगन्नाथ रथयात्रा - Digital Invite (Web Version)

No Python needed for this — it's a small website (HTML/CSS). Free to host on
**GitHub Pages**.

## What's included
- `index.html` — your home page image with 4 invisible clickable buttons
- `location.html`, `agenda.html`, `route.html`, `contact.html` — the 4 pages
  that open when each button is tapped, each with a back arrow (top-left)
- `contact.html` also has a red "आता कॉल करा" (Call Now) button that opens
  the phone dialer automatically — this ONLY works when opened on a mobile
  phone, not a computer
- `images/` — folder holding all 5 images (home.jpg is your real invite;
  location.jpg, agenda.jpg, route.jpg, contact.jpg are placeholders you
  need to replace)

## Step 1 — All 5 real images are already in place ✅
`home.jpg`, `location.jpg`, `agenda.jpg`, `route.jpg`, and `contact.jpg` are
all your real designs, already wired up with working tap zones:
- Home page: all 4 colored buttons open the right page
- Location / Agenda / Route pages: the "मागे जा | BACK" button on each
  image takes you back home
- Contact page: each of the 3 names/numbers is individually tappable and
  dials that specific person —
  - वेणुधर कृष्णदास → +91 9125695157
  - अनादी पुरुष दास → +91 9145188192
  - रोहिणी कीर्ती देवी दासी → +91 8668809299

If you ever add more numbers or change one, open `contact.html` in a text
editor and look for the `<a class="hotspot" ... href="tel:+91...">` lines
— update the number there.

## Step 3 — Put it online with GitHub Pages (free)
1. Go to github.com, sign in (or create a free account)
2. Click **New repository** → name it e.g. `jagannath-invite` → Create
3. On the repository page, click **Add file → Upload files**
4. Drag in all the files and the `images` folder from this project, then
   **Commit changes**
5. Go to **Settings → Pages** (left sidebar)
6. Under "Branch", choose `main` and folder `/ (root)` → **Save**
7. Wait ~1 minute, then refresh — GitHub will show you a live link like:
   `https://yourusername.github.io/jagannath-invite/`

That link is what you share on WhatsApp/social media as the digital invite.
It works exactly like an app page, opens instantly in any phone browser,
and doesn't need anyone to install anything.

## Step 3b — Turn on the WhatsApp preview image
Once your site is live (after Step 3), open `index.html` and find these 5
lines near the top:
```
<meta property="og:image" content="https://YOURUSERNAME.github.io/jagannath-invite/images/home.jpg">
<meta property="og:url" content="https://YOURUSERNAME.github.io/jagannath-invite/">
```
Replace `YOURUSERNAME` with your actual GitHub username in both lines
(match your real Pages link from Step 3). Save, and re-upload just this
file to GitHub (Add file → Upload files → overwrite).

Now when anyone pastes your link into WhatsApp, it will automatically show
a thumbnail of your invite image above the link — no need for them to
click through blindly.

## Step 3c — How to actually send it on WhatsApp
Two options, and it's best to do both:
1. **Send the picture directly**: In WhatsApp, attach `images/home.jpg` as
   a Photo (not Document), then before sending, type your link
   (`https://yourusername.github.io/jagannath-invite/`) in the caption
   box under the image. People see the poster immediately and the link
   is right there to tap.
2. **Just paste the link**: after Step 3b above, pasting the bare link
   will auto-show a preview image + title, so it still looks good even
   without attaching a separate photo.

## Step 4 — Test on an actual phone before sharing widely
- Open the link on your own phone
- Tap all 4 home buttons — confirm each opens the right page
- Tap the back arrow on each page — confirm it returns to home
- Tap "आता कॉल करा" on the contact page — confirm it opens your dialer
  with the correct number pre-filled

## Notes
- The 1080x1920 aspect ratio is preserved on any screen size (the CSS
  handles this with `aspect-ratio`), so your button positions will always
  line up correctly with the image underneath.
- If you ever redesign the home image and move the buttons, you'll need
  to update the `left/top/width/height` percentages in `index.html` to
  match the new positions.
