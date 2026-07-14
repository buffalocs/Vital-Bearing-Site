# Vital Bearing and Health OS public pages

This static package contains the Vital Bearing landing page plus Health OS support and privacy pages. Vital Bearing is the website identity while Health OS remains the current app name. The site has no external scripts, analytics, trackers, cookies, forms, or third-party assets.

## Preview locally

From the repository root:

```bash
python3 -m http.server 8080 --directory site
```

Then open `http://localhost:8080`.

Validate before deployment:

```bash
scripts/validate-site.sh
```

The GitHub Pages workflow is manual-only. It will not publish until a repository maintainer deliberately runs **Deploy public pages** and the repository's Pages environment is available.

## Before public App Store submission

1. Replace the private-beta invitation wording with an owner-approved public support email or other direct contact method.
2. Deploy the directory at a stable HTTPS origin.
3. Put the resulting `support.html` and `privacy.html` URLs into App Store Connect.
4. Recheck the policy against the exact shipping build and update its effective date if necessary.

## Domain

The intended production domain is `vitalbearing.com`. DNS and hosting are configured separately from this static package.
