# anilbholla.com — GitHub Pages

Static one-page website for Anil Bholla, Leadership Coach.

## Files
- `index.html` — the whole site
- `hero-kurta.jpg`, `anil-suit.jpg`, `anil-polo.jpg`, `anil-full-length.jpg`, `logo.svg` — photos and logo
- `CNAME` — tells GitHub Pages to serve the site at anilbholla.com

## 1. Put the site on GitHub
1. Sign in at github.com and create a new **public** repository (e.g. `anilbholla-website`).
2. Click **Add file → Upload files**, drag in all 8 files (no folders), then **Commit changes**.
3. Go to **Settings → Pages**. Under *Build and deployment* choose **Deploy from a branch**, branch **main**, folder **/ (root)**, and **Save**.
4. After a minute the site is live at `https://<your-username>.github.io/anilbholla-website/`. Check it on a phone.

## 2. Connect anilbholla.com (DNS at GoDaddy)
In GoDaddy → **My Products → anilbholla.com → DNS**:

| Type  | Name | Value                        |
|-------|------|------------------------------|
| A     | @    | 185.199.108.153              |
| A     | @    | 185.199.109.153              |
| A     | @    | 185.199.110.153              |
| A     | @    | 185.199.111.153              |
| CNAME | www  | `<your-username>.github.io`  |

Delete any other A record for `@` (such as GoDaddy's "Parked" record) and any GoDaddy forwarding.

Then in GitHub **Settings → Pages**, type `anilbholla.com` under *Custom domain*, save, and tick **Enforce HTTPS** once it becomes available (DNS can take a few hours).

## 3. Turn on the contact form
GitHub Pages cannot send email, so the form sends through FormSubmit (formsubmit.co, free, no account).

1. Once the site is live, submit the form once yourself.
2. FormSubmit emails **anilbholla@gmail.com** an activation link. Anil clicks it. (The first test shows an error message until this is done.)
3. Submit again. The message should arrive in Anil's inbox.
4. Optional, to hide his email from the page source: FormSubmit's activation email gives a random code. In `index.html`, find
   `const FORM_ENDPOINT='https://formsubmit.co/ajax/anilbholla@gmail.com';`
   and replace `anilbholla@gmail.com` with that code.

## Making changes later
Edit `index.html` on GitHub (pencil icon) and commit; the site updates in about a minute.
