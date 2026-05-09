# VARY LLC. website

Static two-page corporate and commerce disclosure site for GitHub Pages.

## Local preview

```powershell
python -m http.server 8787
```

Open `http://127.0.0.1:8787/`.

## GitHub Pages

- Publish source: repository root
- Custom domain: `vary-llc.com` via `CNAME`
- Enable HTTPS in the GitHub Pages settings after DNS propagates.
- Configure `www.vary-llc.com` as a DNS alias to the GitHub Pages host if `www` should also resolve.
- Domain/DNS may be managed from Google Workspace or the registrar connected to Google Workspace. Confirm the authoritative DNS host before changing records.

Typical DNS records:

```text
vary-llc.com.      A      185.199.108.153
vary-llc.com.      A      185.199.109.153
vary-llc.com.      A      185.199.110.153
vary-llc.com.      A      185.199.111.153
www.vary-llc.com.  CNAME  <github-user-or-org>.github.io.
```

## Before production

- Confirm whether address, phone number, and responsible person should be published directly on `/commerce/`.
- Align Stripe Dashboard business description with the products and commerce information described on this site.
- Add final Stripe Payment Links or Checkout links only after the product or service terms are finalized.
- Add the final contact form URL to `siteConfig.contactFormUrl` in `script.js`.
