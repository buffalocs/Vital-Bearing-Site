# Vital Bearing and Health OS public pages

This static package contains the Vital Bearing landing page plus Health OS support, privacy, FAQ, accessibility, and error pages. Vital Bearing is the website identity while Health OS remains the current app name. The site has no external scripts, analytics, trackers, cookies, forms, or third-party assets.

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

The editable source remains here. Public files are deliberately copied into the separate public repository `buffalocs/Vital-Bearing-Site`, which GitHub Pages deploys to `vitalbearing.com`. See `docs/PUBLIC_SITE_OPERATIONS.md` for the controlled publishing and rollback process.

## Before public App Store submission

1. Replace the private-beta invitation wording with an owner-approved public support email or other direct contact method.
2. Enforce HTTPS after GitHub finishes issuing the custom-domain certificate.
3. Verify all production URLs with `REQUIRE_HTTPS=1 scripts/check-public-site.sh`.
4. Put the Support, Privacy, and Marketing URLs into App Store Connect.
5. Recheck the policy against the exact shipping build and update its effective date if necessary.

## Domain

The production domain is `vitalbearing.com`. DNS and hosting are configured separately from this static package.
