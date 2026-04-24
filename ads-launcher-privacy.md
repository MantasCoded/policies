# Privacy Policy — Ads Launcher

**Last updated: 24 April 2026**

## 1. About this Policy

Ads Launcher is an internal campaign-launch and smartlink-management tool
operated at **https://smart.trndfy.com** by **Lithuania HQ** (trading as
TRNDFY, "we", "our", "us"). Ads Launcher is a module of the **Advectory**
analytics platform and shares the same data-handling practices described
in this policy.

This policy explains what data we collect, how we use it, and what rights
you have. If anything is unclear, email **mantas@lithuaniahq.com**.

## 2. Who uses Ads Launcher

Ads Launcher is used by authorised members of the TRNDFY team to create
and monitor paid Meta (Facebook / Instagram) advertising campaigns for
music releases. End listeners of the resulting ads are not users of Ads
Launcher — they interact only with smartlinks hosted at
`spoti.trndfy.com`.

## 3. Data we collect

### 3.1 Team members (authenticated users of Ads Launcher)
- Email address and display name (via Supabase authentication)
- Session tokens and authentication metadata
- Activity logs of campaigns and smartlinks you create

### 3.2 Meta advertising data (via the Meta Marketing API)
With explicit authorisation through a Meta System User token we request
the following from ad accounts inside our Business Manager:
- Ad account ID, name, currency, timezone
- Campaign, ad set, ad creative, and ad metadata
- Performance metrics: impressions, clicks, spend, reach, CTR, CPC, CPM,
  conversions
- Page IDs, Instagram user IDs, Pixel IDs, and custom conversion IDs
  linked to those ad accounts

We only access data necessary to create campaigns and report performance.

### 3.3 Smartlink-listener data
When a listener visits a smartlink at `spoti.trndfy.com/<slug>` we process:
- IP address, user agent, referrer, and UTM parameters
- The `_fbp` and `_fbc` cookies set by Meta Pixel
- Click events (e.g. "Smart Link Click") forwarded to Meta's Conversions
  API for attribution

This processing is governed by Meta's own Pixel + Conversions API terms
and our legitimate interest in ad attribution.

### 3.4 Uploaded creatives
- Video files and cover artwork you upload for use in ads
- File names, sizes, MIME types, and storage paths

## 4. How we use your data

- Authenticate team members and authorise access to ad accounts
- Create, update, and monitor Meta campaigns on your behalf
- Generate smartlink landing pages for promoted tracks
- Report campaign performance inside the Ads Launcher dashboard
- Forward conversion events to Meta for ad attribution and optimisation

We do **not** sell, rent, or share your personal data or advertising
data with any third party for their own purposes.

## 5. Where data is stored

- **Supabase** (PostgreSQL + object storage) — hosts user accounts,
  campaign records, and uploaded creatives. Data is encrypted at rest.
- **Cloudflare Workers** — runs the application logic and serves
  smartlinks. No persistent storage.
- **Meta** — campaign and conversion data is transmitted to Meta's
  Marketing and Conversions APIs. Governed by Meta's policies.

All data transmission uses TLS 1.2+ and sensitive tokens
(e.g. Meta System User tokens) are stored as Cloudflare Worker secrets,
never in source code.

## 6. Data retention

- Campaign and smartlink records are retained while the account is
  active and for up to 24 months after account closure for accounting
  and audit purposes.
- Uploaded video creatives are retained while linked to an active
  campaign; orphaned files are purged after 90 days.
- Authentication tokens are rotated or revoked on session end.
- You may request earlier deletion at any time (see section 8).

## 7. Third-party services

Ads Launcher integrates with:

- **Meta (Facebook / Instagram)** — [Meta Privacy Policy](https://www.facebook.com/privacy/policy/)
- **Supabase** — [Supabase Privacy Policy](https://supabase.com/privacy)
- **Cloudflare** — [Cloudflare Privacy Policy](https://www.cloudflare.com/privacypolicy/)
- **Advectory SDK** — first-party analytics for smartlink events; data
  stays inside our infrastructure

We access these platforms only through their official APIs and only
with the permissions you explicitly grant.

## 8. Your rights

You have the right to:

- **Access** — request a copy of the data we hold about you
- **Correct** — request correction of inaccurate data
- **Delete** — request deletion of your account and associated data
- **Revoke** — disconnect any Meta ad account integration at any time
- **Object / restrict** — object to or restrict processing under GDPR

To exercise any of these rights, email **mantas@lithuaniahq.com**. We
will respond within 30 days.

## 9. Data deletion

To delete your account and all associated data:

1. Email **mantas@lithuaniahq.com** with the subject "Account deletion"
   from the email address registered with Ads Launcher.
2. We will verify the request and delete your account, campaign
   records, uploaded creatives, and authentication data within 30 days.
3. Cached ad-performance data on Meta's side can be deleted separately
   via your Meta Business Manager.

## 10. Cookies

Ads Launcher uses only essential cookies for authentication and session
management. Smartlinks hosted at `spoti.trndfy.com` use Meta's `_fbp`
and `_fbc` cookies solely for ad attribution.

## 11. Children

Ads Launcher is not intended for use by anyone under 18. We do not
knowingly collect data from minors.

## 12. International transfers

Data may be transferred to and processed in jurisdictions where our
infrastructure providers operate (EU, US, UK). Transfers rely on
Standard Contractual Clauses or equivalent safeguards.

## 13. Changes to this Policy

We may update this Privacy Policy from time to time. Material changes
will be signalled by updating the "Last updated" date above. Continued
use of Ads Launcher after an update constitutes acceptance.

## 14. Contact

**Email**: mantas@lithuaniahq.com  
**Website**: https://trndfy.com
