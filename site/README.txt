nathanielcorey.com  —  site files
=================================

WHAT'S HERE
  index.html      the whole site (complete HTML document)
  images/         every photo, screenshot and logo the page uses
  CNAME           tells GitHub Pages the custom domain. Harmless on other hosts.

BEFORE YOU DEPLOY
  Drop your resume PDF in this folder and name it exactly:  resume.pdf
  The "Résumé" button in the header links to it. Without the file that button 404s.

OPTION A — GITHUB PAGES (recommended: free, versioned, no nameserver change)
  1. Create a new PUBLIC repo named exactly:  nathCode45.github.io
  2. Upload the CONTENTS of this folder to the repo root
     (index.html and CNAME at the top level, images/ as a folder).
     Web upload works fine: repo -> Add file -> Upload files -> drag them in.
  3. Repo -> Settings -> Pages. Source: "Deploy from a branch", branch main, folder / (root).
  4. Same page, Custom domain: nathanielcorey.com -> Save.
  5. Do the GoDaddy DNS step below.
  6. Come back after DNS resolves and tick "Enforce HTTPS".

  GoDaddy DNS (My Products -> Domain -> DNS -> Manage Zones):
    Delete the parked "A @" record GoDaddy created, then add:
      A      @     185.199.108.153
      A      @     185.199.109.153
      A      @     185.199.110.153
      A      @     185.199.111.153
      CNAME  www   nathCode45.github.io
    Confirm these values against GitHub's current docs page
    ("Managing a custom domain for your GitHub Pages site") before trusting them.

OPTION B — NETLIFY (fastest, no git)
  1. netlify.com -> sign up -> Add new site -> Deploy manually.
  2. Drag this whole folder onto the drop zone. Site is live in seconds.
  3. Domain settings -> Add a domain -> nathanielcorey.com.
  4. Netlify shows you the exact DNS records. Enter those at GoDaddy.
     HTTPS is automatic once DNS resolves.

AFTER DNS
  Changes take anywhere from 10 minutes to a few hours to propagate.
  Check progress:  dnschecker.org  (enter nathanielcorey.com, type A)
  Don't skip HTTPS. A portfolio on plain http:// shows a "Not secure" warning.

UPDATING LATER
  GitHub Pages: edit the file in the repo (or push a commit); the site rebuilds itself.
  Netlify: drag the folder onto the site again to redeploy.
