# Care Dental UI – website and admin panel

Public site: `index.html` (one page: Home, Services, About Us, Our Team, Book & Contact).
Admin panel: `/admin` (sign in), then the dashboard. Open it from the **Admin Panel** button in the footer.

## Put it on GitHub
1. Sign in at https://github.com. Click **+ → New repository**, name it `care-dental-ui`, click **Create repository**.
2. Click **uploading an existing file**. Unzip the ZIP first, then select everything inside the folder and drag it onto the page.
   Make sure `netlify`, `admin`, `assets`, `src`, `tests`, `_redirects`, `_headers` and `netlify.toml` are included.
3. Click **Commit changes**.

## Put it on Netlify
1. Sign in at https://app.netlify.com with GitHub. Click **Add new project → Import an existing project**.
2. Choose **Deploy with GitHub** and select `care-dental-ui`. Leave the settings empty and click **Deploy**.
   Do not drag the folder onto Netlify, because the admin functions will not start.

## First sign-in
1. Open `https://YOUR-SITE.netlify.app/admin`.
2. Username: **alihussain**. Password: the one given to you with this project.
3. Open **Account** and change the password. Use at least 12 characters.

## What you can edit
- **Business details:** name, phone, WhatsApp number and email. These update the header, footer, contact area and every link.
- **Homepage text:** the heading and the line under it.
- **Services:** add, edit, reorder and delete. Deleted services stay deleted.
- **Images and logo:** upload PNG, JPG, WEBP, GIF or SVG up to 2 MB, then choose **Use as logo**.
- **Restore original text:** brings back the original text. Images are kept.

## Security
Passwords are stored as scrypt hashes, never in plain text. Sessions are signed cookies (8 hours).
Five wrong passwords lock sign-in for five minutes. Changing the password signs out other sessions.
Uploads are checked by file signature, and SVGs with scripts are refused.

## Tests (optional, needs Node.js)
    npm install
    ADMIN_TEST_PASSWORD='your-current-password' npm test
