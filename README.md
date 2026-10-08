# WhatDate — Privacy Policy

This repository exists for one reason: to serve WhatDate's privacy policy at a public URL, as the
Google Play Store requires.

**Published page:** https://sudowhat.github.io/whatdate-privacy/

It contains no application code. The WhatDate source lives in a separate private repository, and
should stay that way — this repo is what makes the policy public without making anything else
public.

## Editing

Do not edit `index.html` by hand. It is generated from the policy inside the app
(`app/src/main/assets/policies/PRIVACY_POLICY.md` in the app repo) by
`python tools/policy/privacy_page.py publish`, which also checks that the live page matches.
The page carries the source text's SHA-256 in `<meta name="whatdate-policy-sha256">`, and a Play
bundle of the app refuses to build while the live page differs from the app's copy.

The page is deliberately self-contained — no external fonts, scripts, or images. A privacy policy
that reported its readers to a third-party CDN would be a poor privacy policy.
