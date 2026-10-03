# VerifyCarrier Chrome Extension Privacy

The extension sends the carrier number or company name you enter, or the text you
explicitly select and ask it to look up, to https://verifycarrier.com. It does not
automatically read web pages or collect your browsing history. Selected text is
limited to 120 characters. Lookup terms are not retained by the extension.

If you save your personal VerifyCarrier API key, it is stored in Chrome local
extension storage on this device, not Chrome sync. The key is sent to
verifycarrier.com as an authorization header for your requested API calls. It is
never added to website URLs. You can remove it in the popup or by uninstalling
the extension. No shared production key is included in the download.

The extension does not run advertising, analytics or session replay SDKs. API
requests are subject to VerifyCarrier's server-side usage, security, quota and
carrier-source processing described in the [website privacy policy](https://verifycarrier.com/privacy).
The service receives normal network request information, including your IP address.

Website links include fixed marketing campaign tags identifying this extension.
After opening the website, its own privacy and analytics consent choices apply.
Campaign tags contain no API key or personal identifier. Carrier profile links
include the public USDOT of the profile you choose to open.

For questions, contact [VerifyCarrier support](https://verifycarrier.com/support).
