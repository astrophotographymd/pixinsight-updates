# AstroMD Social Export update repository

This folder is the static site that PixInsight reads as an update repository.

Production URL:

    https://updates.astrophotographymd.com/

PixInsight looks for `updates.xri` at that exact URL, with no redirect.

## Host on GitHub Pages

1. Create a dedicated GitHub repository (keep it separate from the main
   website). Do not put `private/` or `tools/keygen.js` in this repository.
2. Copy the contents of this folder to the repository root, including
   `updates.xri`, the dated package archive, `CNAME`, `.nojekyll`, and
   this README.
3. In the GitHub repo: Settings > Pages > Source: Deploy from a branch,
   branch `main` (or `gh-pages`), folder `/ (root)`.
4. Point a DNS CNAME record for `updates.astrophotographymd.com` at
   `<user>.github.io`. The included `CNAME` file tells GitHub Pages the
   host name. GitHub Pages will serve HTTPS once the certificate is ready.
5. Confirm in a browser that these two URLs load, and that neither
   redirects:

   - https://updates.astrophotographymd.com/updates.xri
   - https://updates.astrophotographymd.com/<package-file>.tar.gz

6. In PixInsight, add `https://updates.astrophotographymd.com/` under
   Resources > Updates > Manage Repositories, then Check for Updates.

`.nojekyll` tells GitHub Pages not to process the files with Jekyll, which
can otherwise ignore folders whose names start with an underscore, or
mishandle some static files.

## Rebuild

From the AstroMD-SocialExport tree:

    python3 tools/build-repo.py

Then replace the published files with the new `repo/` output. Keep older
package archives on the site if you want them still downloadable; PixInsight
uses the sha1 in `updates.xri` to decide whether a package is new.

## Package downloads

`updates.xri` sets `serverURL` on the package element to:

    https://astromd-keygen-sandbox.astrophotographymd.workers.dev/dl/

PixInsight still loads `updates.xri` from this site. It downloads the
archive from the address above, using the same relative file name.
That server streams the file from this site and counts the download, so
the archive must stay here under the same name. PixInsight does not
follow redirects, and this download server does not redirect.

To build a repository that omits `serverURL`, so PixInsight downloads
the archive directly from this site, run:

    python3 tools/build-repo.py --no-download-server

or set `ASMD_OMIT_DOWNLOAD_SERVER=1` (also `true`, `yes`, or `on`).

## Signing

Official PixInsight documentation says a repository should be signed with a
Certified PixInsight Developer (CPD) identity. This local build does not
include a Signature element. Signing is a launch step, not part of this
script.

## What is not in this folder

Developer tools, the license key generator, and the HMAC secret never belong
in the public repository.
