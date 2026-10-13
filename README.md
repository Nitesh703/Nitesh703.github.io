# Portfolio

Personal site, served by GitHub Pages from the `main` branch (root folder) of a
repo named `Nitesh703.github.io`, at `https://Nitesh703.github.io`.

Plain static files, no build step:

- `index.html`: all content
- `style.css`: all styling
- `resume.pdf`: linked from the header (add this file yourself)

## Editing

1. Open `index.html` and edit the text. Search for `TODO` to find placeholders.
2. To add a project or publication, copy the commented-out `<ul>` example in
   that section, uncomment it, and fill it in.
3. Preview by opening `index.html` in a browser.
4. Publish:

   ```sh
   git add -A
   git commit -m "Update site"
   git push
   ```

   The live site updates a minute or two after the push.

## Adding a custom domain later

Not set up. If you want one, per
[GitHub's docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site):

1. In the repo, go to Settings → Pages → Custom domain, enter the domain, and
   save. This commits a `CNAME` file containing the domain to the repo root.
   (You can also add that file by hand.)
2. At your DNS provider, add records:
   - **Apex domain** (`example.com`): four `A` records pointing to
     `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`.
     Optionally, for IPv6, four `AAAA` records pointing to
     `2606:50c0:8000::153`, `2606:50c0:8001::153`, `2606:50c0:8002::153`,
     `2606:50c0:8003::153`.
   - **Subdomain** (`www.example.com`): a `CNAME` record pointing to
     `Nitesh703.github.io` (no repo name).
3. Wait for DNS to propagate, then tick Enforce HTTPS in Settings → Pages. It
   can take up to 24 hours for that option to become available.

GitHub also recommends verifying the domain in your account settings before
adding it, to guard against domain takeovers. The IP addresses above can
change, so check the linked docs before setting records.
