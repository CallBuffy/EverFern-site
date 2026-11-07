EverFern Solutions website - launch notes
=========================================

This folder is the complete site: 4 pages, all images, logos and the
capabilities PDF. It's plain HTML. Nothing to build or install.

Setup (same as buffyhoward.com):
  GitHub   = stores the files AND serves the website for free (GitHub Pages)
  Hostinger = owns the domain name; its DNS points everfernsolutions.com at GitHub

PART A - GITHUB (put the site online)
1. Sign in at github.com (same account used for buffyhoward.com).
2. Top right "+" > New repository.
   Name: everfern-site   Visibility: Public   Click "Create repository".
3. On the empty repo page, click "uploading an existing file".
4. Unzip EverFern-Website.zip on your computer. Open the folder, select ALL
   the files inside (not the folder itself, not the zip) and drag them in.
   Click "Commit changes".
5. Repo > Settings > Pages (left menu).
   Source: Deploy from a branch. Branch: main, folder: / (root). Save.
6. Wait 1-2 minutes. Test the temporary address it shows:
   https://<your-username>.github.io/everfern-site/
7. Same Pages screen > Custom domain: type everfernsolutions.com > Save.

PART B - HOSTINGER (point the domain at GitHub)
8. hPanel > Domains > everfernsolutions.com > DNS / Nameservers > DNS records.
9. DELETE any existing A or AAAA records with Name "@".
   DELETE any existing record with Name "www".
   DO NOT touch MX or TXT records - those run the email.
10. Add 4 A records, Name "@", TTL default, one for each address:
      185.199.108.153
      185.199.109.153
      185.199.110.153
      185.199.111.153
11. Add 1 CNAME record: Name "www"  Target "<your-username>.github.io"

PART C - FINISH
12. Back in GitHub > Settings > Pages. Wait until the domain check shows a
    green check (minutes to a few hours). Then tick "Enforce HTTPS".
13. Open https://everfernsolutions.com on computer and phone.
14. Submit the contact form once. FormSubmit sends a one-time activation
    email to hello@everfernsolutions.com - click the link in it, or later
    messages won't arrive.
15. Paste the site link into a LinkedIn post draft to check the preview image.

SWAPPING A PHOTO LATER
In the GitHub repo: Add file > Upload files > drop in the new image with the
SAME file name (e.g. serve-ltc-preview.jpg for Long-Term Care) > Commit.
The live site updates in about a minute. No code changes needed.
Keep images under ~1400px wide so pages load fast.

FILES
index.html            Home page
services.html         Service detail page
our-name.html         Our Story (Nanna Fern) page
privacy.html          Privacy policy
*.jpg / *.png / *.svg Photos, logos, icons
og-image.png          Image shown when the site is shared on social/text
EverFern-Solutions-Capabilities.pdf  Downloadable one-pager
