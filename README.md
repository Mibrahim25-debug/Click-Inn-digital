# Click Inn Digital website

Source code for **https://clickinndigital.com**, the Click Inn Digital company website.

It is a plain static website: HTML, CSS and JavaScript only. There is no WordPress, no database, no build step and nothing to install.

## What each file does

### Pages

| File | Page | What it contains |
|---|---|---|
| `index.html` | Home | Main landing page: headline, key numbers, client logo strip, ways to start, footer |
| `about.html` | About | Company story, team approach, company facts, clients |
| `services.html` | Capabilities | Data platforms, dashboards, process automation, AI agents, predictive models, assessments |
| `work.html` | Work | Delivered solutions running in production |
| `approach.html` | Approach | How we deliver: weekly rhythm and engagement phases |
| `assurance.html` | Assurance | Security, data residency, AI controls, common questions |
| `contact.html` | Contact | Book a demo form, contact email and company address |

### Styling and behaviour

| File | Purpose |
|---|---|
| `site.css` | All styling for every page (colours, layout, dark mode, animations) |
| `site.js` | All interactivity: menus, scrolling logo strip, number count-up, animations, pause button, demo request form |

### Images

| File or folder | Purpose |
|---|---|
| `logos/` | Client logos shown in the scrolling "Our clients" strip: `tess-payments.png`, `twyla-tech.png`, `qalco-energy.png`, `premier-solutions.png` |
| `favicon.svg`, `favicon-32.png`, `favicon.ico` | Click Inn icon shown on the browser tab |
| `apple-touch-icon.png` | Icon used when the site is saved to a phone home screen |

## How the pieces connect

- Every page loads `site.css` and `site.js`, so a change to either affects the whole site.
- The header menu and the footer are repeated inside each HTML file. If you change a menu item, footer text, email or address, change it in **all** pages that show it.
- The client logo strip appears in `index.html` and `about.html`. A logo must be added in both places and its image saved in `logos/`.
- The browser tab icon is linked in the `<head>` of every page.

## Common edits

| To change... | Edit |
|---|---|
| Company address or contact email | `contact.html` (address is in the "Email us directly" box). The email also appears in every page footer. |
| Colours, fonts, spacing | `site.css` (colours are defined at the top) |
| A client logo | Replace the image in `logos/`, keeping the same file name |
| Page wording | The matching `.html` file from the table above |

## Deploying to Bluehost

The live site is hosted on Bluehost (Starter Hosting). The website files must sit directly in `public_html`.

1. Open Bluehost, then **Hosting**, then **File Manager**, then `public_html`.
2. Click **Upload** and upload only the files you changed. Click **Overwrite** if asked.
3. Check the **Permissions** column. Every file should be **0644** and every folder **0755**. A file left at 0600 shows visitors a **403 Forbidden** error or a missing image.
4. Open the site in a private browser window to check. Press **Ctrl+Shift+R** if you still see the old version, because Bluehost makes browsers keep pages for 2 hours.

Do not delete the `.htaccess` file or the `.well-known` folder on the server. They are not part of this repository.

## Notes

- DNS is managed at GoDaddy and points to the Bluehost server. Email runs on Google Workspace. Do not change DNS or email records without checking with the team first.
- Do not upload zip files or log files to `public_html`. Anyone can download them.
