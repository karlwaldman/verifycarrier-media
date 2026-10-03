# VerifyCarrier — Quick Carrier Lookup

Look up a USDOT, MC number or company name from the Chrome toolbar, or select a
carrier name/number on any page and use the right-click menu. Public identity,
registration and safety fields come from [VerifyCarrier](https://verifycarrier.com).
Missing source fields stay unknown. This extension does not approve carriers.

## Free allowance

Use your own VerifyCarrier API key for your existing plan: Free includes 100 API
calls per month. Without a key, the API allows 10 calls per IP per UTC day. Search
and opening a search result each use a call. All enforcement happens on the server.
No shared service key, paid entitlement or plugin credential is bundled.

## Install the test build

1. Unzip the release ZIP into a permanent folder.
2. Open `chrome://extensions` and enable Developer mode.
3. Choose **Load unpacked** and select the folder containing `manifest.json`.
4. Pin VerifyCarrier. Open it and search for `DOT 2930366` or `MC 989359`.
5. Optionally create a [free account](https://verifycarrier.com/signup?utm_source=chrome_extension&utm_medium=referral&utm_campaign=quick_lookup&utm_content=readme)
   and add your personal key under **Use your free account's API key**.

This is an unpacked test build, not a Chrome Web Store installation. Store
publication needs the owner's developer account and policy declarations.

## Verify and package

From the repository root, run `npm run test:extension` and
`npm test -- tests/chrome-attribution.test.ts tests/measurement-context.test.ts`.
Create the upload ZIP from this directory with only `manifest.json`, `popup.html`,
`popup.css`, `popup.js`, `lookup.mjs`, `background.js` and `icons/*` at its root.
Do not include tests, dependencies, credentials, environment files or private code.

Manual installed-extension checks: toolbar DOT/MC/name lookup, right-click selected
text, no match, malformed input, 429 recovery, save/remove personal key, invalid key
fallback warning, profile/signup links, and quota headers. A local HTML preview
exercises live lookups and layout, but Chrome permission handling and storage need
the installed build. Browser previews cannot read unexposed cross-origin quota
headers; the extension's host permission allows those reads.

## Acquisition experiment

Homepage, signup, carrier profile and monitoring links carry fixed
`utm_source=chrome_extension` plus `quick_lookup` campaign tags. The website
recognizes this bounded acquisition channel through its existing consent-based
first-touch attribution and server outcome receipts. No analytics SDK runs in the
extension. Links are marketing attribution, not identity or entitlement proof.

After website deployment, verify a consenting extension visitor's page view and
matching persisted signup receipt arrive in PostHog before claiming ingestion.
Report external candidate visitors, receipt-backed signups and monitoring handoffs
at 14 and 28 days, grouped by `acquisition_channel='chrome_extension'`. Distinguish
unavailable ingestion from zero demand; exclude internal/test users. Store installs
and impressions come from the owner's Chrome Web Store dashboard. Backlinks and
clicks are acquisition inputs, not proof of adoption or a ranking guarantee.

See [store-listing.md](store-listing.md) and [PRIVACY.md](PRIVACY.md) for publication.
