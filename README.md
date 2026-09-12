# Affiniti

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Affiniti is the channel-marketing software company founded in Sydney, Australia by Joel Montgomery
and listed under that name on the EquityZen secondary market, which is the lead this profile was
harvested from. It traded for most of its life as **OneAffiniti**; Capstreet-backed Incentive
Solutions acquired it in April 2021, and in September 2023 the combined business rebranded to
**Extu**, the brand every live web property and the product carry today. `oneaffiniti.com` 301s to
`extu.com`.

**Not the same company as affiniti.com.** There is an unrelated New York fintech called Affiniti
Finance, Inc. (`affiniti.com`, YC / SignalFire-backed, co-branded SMB commercial cards). It is a
different company with a different EquityZen/Crunchbase record and is not profiled here. The
EquityZen listing this repo was harvested from —
[equityzen.com/company/affiniti](https://equityzen.com/company/affiniti) — names "digital marketing
campaigns ... to markets and channels that are otherwise difficult to access" and "Founder & CEO
Joel Montgomery", which is unambiguously the OneAffiniti/Extu company.

## What was found

| Surface | Result |
|---|---|
| OpenAPI / Swagger / GraphQL / gRPC / WSDL / AsyncAPI | **None.** No spec at any probed path on `extu.com`, `cms-api.extu.com`, `app.extu.com` or `oneaffiniti.com`. |
| Developer portal / API reference / SDKs / CLI | **None.** The site's own `llms.txt` (661 indexed pages) and full XML sitemap name no developer page; no packages on npm, PyPI or RubyGems. |
| `llms.txt` | **Served** — `https://extu.com/llms.txt`, 274,992 bytes, saved verbatim to `llms/affiniti-llms.txt`. |
| `/.well-known/` | **Two hits** — OIDC discovery + RFC 8414 metadata on `cms-login.extu.com` and `pexp-login.extu.com` (Auth0 custom domains). Everything else 404s on every host. |
| A2A agent card / MCP server | **None** on any host. |
| Compliance | SOC 2 Type 2 (provider-announced) and a GDPR trust center. |
| Private backend | `cms-api.extu.com` is the Laravel service the Extu CMS app calls (`middlewareBaseUrl` in the `app.extu.com` bundle). Every anonymous route 404s; there is no public contract. |

`extu.com` answers our crawler with a Cloudflare managed challenge (HTTP 403, `cf-mitigated:
challenge`) on every HTML URL, so page bodies were not read. Its `robots.txt`, `sitemap.xml`,
`llms.txt` and `/.well-known/` paths all answer normally, and those are the sources every finding
above rests on.

- https://extu.com/
- https://equityzen.com/company/affiniti
