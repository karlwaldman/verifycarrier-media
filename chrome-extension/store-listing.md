# Chrome Web Store listing draft

**Name:** VerifyCarrier — Quick Carrier Lookup

**Summary:** Look up USDOT, MC or carrier names. Review public carrier facts and
open the full VerifyCarrier profile before your next load.

**Category:** Tools

**Website:** https://verifycarrier.com

**Support:** https://verifycarrier.com/support

**Privacy policy:** https://github.com/karlwaldman/verifycarrier-media/blob/main/chrome-extension/PRIVACY.md

**Promotional image:** [440 × 280 PNG](assets/promo-440x280.png). Supply genuine screenshots from the installed build before submission.

## Description

Check the carrier. Before the load.

VerifyCarrier puts public carrier research a click away. Search a USDOT, MC number
or company name from your toolbar. Found a carrier number in an email, load board
or website? Select the text, right-click and choose VerifyCarrier.

Review company identity, location, registration, reported operating status, fleet
size and available FMCSA safety rating. Open the full carrier profile on
https://verifycarrier.com to keep researching.

Start with anonymous lookups: 10 API calls per IP per day. Create a free VerifyCarrier
account and add your own API key for 100 API calls per month. Search and profile
lookups count separately. Paid plans use their existing API allowance. Monitoring
and saved research have their own availability and access requirements.

Missing or partial source data stays unknown. VerifyCarrier provides research
evidence, not a safety certification or carrier-selection recommendation.

Your personal API key stays in local Chrome storage and is sent only to
verifycarrier.com when you request a lookup. There are no content scripts,
automatic page scans, remote scripts or extension analytics trackers.

Create your free account: https://verifycarrier.com/signup

## Owner submission checklist

- Upload release ZIP and 128px icon; attach genuine screenshots from the installed
  extension, plus optional branded promotional art.
- Single purpose: user-requested carrier lookup with optional website handoff.
- Host permission: `https://verifycarrier.com/*` for carrier API requests only.
- Storage: optional personal API key on this device; no sync storage.
- Context menus: explicitly selected text lookup only.
- No remote code, broad website access, browsing-history permission or content scripts.
- Declare user-provided API credentials and user-submitted lookup terms consistently
  with PRIVACY.md. Do not claim credentials are never transmitted: they go to the API.
- Verify website CTA links and installed-extension checks before submitting.
- Store homepage link creates a public website reference only after publication;
  no store backlink, install or demand is claimed before then.
