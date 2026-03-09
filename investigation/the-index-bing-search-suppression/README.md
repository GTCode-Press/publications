# The Index: How Bing Blocked an Entire Domain to Bury One Judge's Name

> Domain-Level Search Suppression of an Independent Journalism Site

**Author:** Ekewaka Lono
**Published:** February 13, 2026
**Last Modified:** March 1, 2026
**Canonical URL:** https://gtcode.com/investigation/the-index-bing-search-suppression/
**Section:** Investigations
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

The investigation you're reading almost didn't exist — not because it wasn't written, but because the platform it's published on has been made invisible.

On February 12, 2026, a routine check of Bing Webmaster Tools revealed that `gtcode.com` — this site — returns zero results on Microsoft's search engine. Not low-ranked. Not deprioritized. *Zero.*

The evidence comes from Microsoft's own tools.

---

## Exhibit A: The Disappearance

A `site:gtcode.com` search on Bing returns nothing.

![Bing search for site:gtcode.com returning zero results](https://gtcode.com/img/bing-block-site-search.webp)

*"There are no results for site:gtcode.com."*

This is not a new domain. This site has been publishing investigative journalism and open-source software documentation since 2025. It has a valid sitemap, a robots.txt that explicitly welcomes all crawlers, valid structured data, and no technical barriers to indexing.

---

## Exhibit B: The Investigation Page

URL Inspection of the most recent investigation — "[The Nod: Wilson Loo and the Silent Felony](https://gtcode.com/investigation/the-nod-wilson-loo-silent-felony/)" — returns **"Not discovered."**

![Bing URL Inspection showing "Not discovered" for Wilson Loo investigation](https://gtcode.com/img/bing-block-wilson-loo-not-discovered.webp)

*"URL cannot appear on Bing. The inspected URL is not known to Bing."*

This could be explained away. New page, hasn't been crawled yet. But it wasn't crawled because the domain itself is suppressed. The "Request indexing" button exists, but the question is why a site with a valid sitemap and no crawl barriers requires manual page-by-page submission.

---

## Exhibit C: The Control Case

This is the exhibit that demonstrates domain-level suppression.

URL Inspection of `gtcode.com/repos/agent_session_manager/` — an open-source Elixir software package page — returns **"Blocked."**

![Bing URL Inspection showing "Blocked" for open-source Elixir package](https://gtcode.com/img/bing-block-agent-session-manager.webp)

*"The inspected URL is known to Bing but has some issues which are preventing us from serving it to our users. We recommend you to follow Bing Webmaster Guidelines."*

This is not an investigation page. This is documentation for an open-source Elixir library — `agent_session_manager` — a technical package for managing AI agent sessions. It contains:

- API documentation
- Installation instructions
- Code examples
- A link to the Hex.pm package registry

There is no investigative content. No controversial claims. No names, no allegations, no journalism of any kind. It is a software documentation page, indistinguishable from thousands of other open-source project pages indexed on Bing every day.

And yet: **"Blocked."**

Note the distinction. Exhibit B says "Not discovered" — Bing claims it hasn't seen the page. Exhibit C says the URL **"is known to Bing"** — they crawled it, they evaluated it, and they actively decided to suppress it. An open-source software page was crawled, reviewed, and blocked.

The only thing connecting this Elixir package page to the Wilson Loo investigations is the domain name.

---

## The Pattern

This is the same pattern documented in [The Zone of Politeness](https://gtcode.com/investigation/zone-of-politeness-hawaii-media-blackout/), applied to a different institution:

| System | Mechanism | Result |
|--------|-----------|--------|
| **Civil Beat** | Donor relationships, board overlaps | Editorial silence on Luke-Loo network |
| **Judicial Conduct Commission** | 90-day jurisdictional loophole | Investigation evaded via resignation |
| **HPD** | Selective non-investigation | Reports filed, never acted upon |
| **Bing** | Domain-level content suppression | Entire site — including software repos — invisible |

The methodology is always the same: structural mechanisms that produce suppression without requiring explicit coordination. No one needs to pick up a phone. The system works because each actor follows their own institutional incentives, and the aggregate effect is silence.

---

## What This Isn't

This is not a claim that Microsoft CEO Satya Nadella personally ordered `gtcode.com` blocked. That's not how modern content suppression works.

Search engines accept third-party content complaints. Reputation management firms file these complaints professionally and at scale. A single domain-level complaint — filed by an attorney, a PR firm, or a "concerned party" — can trigger automated review processes that result in suppression. The entity that files the complaint is rarely disclosed.

The question is not whether someone at Microsoft made a deliberate decision. The question is: **who filed the complaint?**

---

## The Open Questions

1. **Has a third-party content removal request been filed against gtcode.com?** Bing's Webmaster Tools does not expose this information to site owners.

2. **Does the Lumen Database contain any takedown requests targeting this domain?** *(Under investigation.)*

3. **Are the same pages indexed on Google, DuckDuckGo, and other search engines?** If the same Elixir package page indexes everywhere except Bing, the suppression vector is Bing-specific.

4. **What is the specific "issue" preventing the agent_session_manager page from being served?** Bing's error message is deliberately vague. A software documentation page cannot plausibly violate content guidelines.

5. **When did the suppression begin relative to the publication dates of the Wilson Loo investigations?** Timeline correlation would establish whether the suppression is responsive to specific publications.

---

## The Evidence Standard

This investigation applies the same standard as every other piece published on this site: **show the receipts.**

The three exhibits above are screenshots from Microsoft's own Bing Webmaster Tools, taken on February 12, 2026, by the verified site owner. They are not interpretations. They are not allegations. They are Microsoft's own diagnostic output, showing that:

1. The entire domain is invisible on Bing
2. Investigation pages are "Not discovered"
3. An open-source software page was crawled, evaluated, and actively blocked

The screenshots are the primary sources. The analysis follows from what they show.

---

## What Happens Next

This page will be updated as additional evidence is gathered. Specifically:

- Cross-engine comparison (Google, DuckDuckGo, Brave, Yandex)
- Lumen Database search for takedown requests
- Bing reconsideration request and its outcome
- Timeline correlation between publication dates and suppression events
- Any response from Microsoft

The record is now public.

---

## Update: February 15, 2026

### Exhibit D: "Not Discovered" Becomes "Blocked"

Three days after this article was published, the same investigation page from Exhibit B — "[The Nod: Wilson Loo and the Silent Felony](https://gtcode.com/investigation/the-nod-wilson-loo-silent-felony/)" — was re-inspected using Bing Webmaster Tools.

The status has changed.

![Bing URL Inspection showing "Blocked" for The Nod investigation page, February 15, 2026](https://gtcode.com/img/bing-block-nod-blocked-20260215.webp)

On February 12, this page was **"Not discovered"** — Bing claimed it had never seen it. On February 15, the status reads **"Blocked"**:

> *"URL cannot appear on Bing. The inspected URL is known to Bing but has some issues which are preventing us from serving it to our users. We recommend you to follow Bing Webmaster Guidelines."*

This is the same message, word for word, that appeared on the open-source Elixir software page in Exhibit C. The distinction between the two exhibits has collapsed. Both pages — an investigation into judicial corruption and an open-source software library — are now identically blocked.

What this confirms: Bing discovered the investigation page sometime in the three-day window between February 12 and February 15. It crawled the page. It evaluated the content. And it applied the same domain-level block that had already caught the software repository. The page was not ignored — it was reviewed and suppressed.

The filter is not passive. It is active, and it is catching new pages as they appear.

---

## Update: February 18, 2026

### Exhibit E: The Phantom Error

Six days after the initial documentation, and three days after Exhibit D confirmed active suppression of new pages, a standard diagnostic step was taken: a Site Scan was initiated through Bing Webmaster Tools. This is Microsoft's own tool for webmasters — designed to identify technical problems that might prevent a site from appearing in search results. The purpose is to help site owners fix their sites.

The scan completed. An email confirmation arrived from Bing Webmaster Tools (`bingwb@microsoft.com`):

![Bing Webmaster Tools email confirming site scan completion for gtcode.com, February 18, 2026](https://gtcode.com/img/bing-block-scan-email-20260218.webp)

*"Scan initiated in Bing Webmaster with name test is now available."*

The scan report contained a single finding: **"ERROR: Http 400-499 errors"** — on the homepage.

![Bing Site Scan showing HTTP 400-499 errors for gtcode.com root URL, February 18, 2026](https://gtcode.com/img/bing-block-scan-4xx-20260218.webp)

The scan reached **page depth 0**. It could not get past the front door. According to Bing's own diagnostic infrastructure, `https://gtcode.com/` is returning an HTTP client error — a 4xx status code — which means the server is supposedly rejecting the request.

There is one problem with this finding: **the error does not exist.**

The homepage returns HTTP 200 — the standard success response — to every user agent tested, including Bing's own crawler signature (`Mozilla/5.0 (compatible; bingbot/2.0; +http://www.bing.com/bingbot.htm)`). It returns 200 over HTTP/1.1 and HTTP/2. It returns 200 with no user agent at all. The page loads. The content renders. The server is not rejecting anything.

This was tested independently on February 18, 2026, using multiple user agents and protocol versions against the live site. Every request succeeded. The 4xx error Bing reports is not reproducible from outside Bing's own infrastructure.

A URL Inspection was then run on the homepage itself — the same URL the Site Scan claimed was returning 4xx errors:

![Bing URL Inspection showing "Discovered but not crawled" and "URL cannot appear on Bing" for gtcode.com homepage, February 18, 2026](https://gtcode.com/img/bing-block-homepage-not-crawled-20260218.webp)

The result: **"Discovered but not crawled. URL cannot appear on Bing."** The crawl section states: *"The inspected URL is known to Bing but has some issues which are preventing indexation."* No specifics. No actionable explanation. Just a vague advisory to "follow Bing Webmaster Guidelines."

But the most revealing detail is the discovery date: **14 November 2017**. Bing has known about this URL for over eight years. It was discovered, and then — according to Bing's own tools — never crawled. Not once in eight years. For a homepage. On a domain with a valid sitemap, a permissive robots.txt, and content that loads for every other crawler on the internet.

The Site Scan says the homepage returns a 4xx error. The URL Inspection says it was never crawled. Both cannot be true. If the page was never crawled, there is no request to generate a 4xx response. If there was a 4xx response, the page was crawled. Bing's own diagnostic tools are contradicting each other on the same URL, on the same day.

### The Contradiction Within the Contradiction

On the same day, a URL Inspection was run on a different page: `https://gtcode.com/consulting/` — a simple services page with no investigative content.

![Bing URL Inspection showing "Indexed successfully" for gtcode.com/consulting, February 18, 2026](https://gtcode.com/img/bing-block-consulting-indexed-20260218.webp)

The result: **"Indexed successfully. URL can appear on Bing."** Green checkmarks. No SEO issues. No problems found.

Compare this to the other URL Inspections documented in this investigation:

| Page | Content | Bing Status |
|------|---------|-------------|
| `/` | Homepage | **Discovered but not crawled** |
| `/investigation/the-nod-wilson-loo-silent-felony/` | Judicial corruption investigation | **Blocked** |
| `/repos/agent_session_manager/` | Open-source Elixir software docs | **Blocked** |
| `/consulting/` | Services page | **Indexed successfully** |

Bing's own URL Inspection tool reports that a consulting page on `gtcode.com` is indexed and can appear in search results. But recall Exhibit A: a `site:gtcode.com` search on Bing returns **zero results**. Not reduced results. Not filtered results. Zero.

So Bing's tools simultaneously claim:
- The homepage was "Discovered but not crawled" — yet the Site Scan reports a 4xx error on the same URL, which requires a crawl attempt
- The homepage has been known to Bing since 2017 but was supposedly never crawled in eight years
- The consulting page is indexed and can appear — but the domain returns nothing in search
- The investigation and software pages are "Blocked" and cannot appear
- The homepage generates a phantom 4xx error that doesn't exist

Four different URL statuses from the same toolset, on the same domain, on the same day — plus a Site Scan that contradicts the URL Inspection of the same page. The one page Bing claims is fine still doesn't appear in search. The suppression operates above the page-level status — it is applied at a layer that overrides Bing's own inspection results.

### The Control Domain

There is a second domain on the identical infrastructure stack: `nshkr.com`. Same static site generator (Hugo). Same hosting platform (GitHub Pages). Same CDN and DNS provider (Cloudflare). Same domain registrar. Same deployment pipeline.

`nshkr.com` contains no investigative journalism. No judicial corruption reporting. No mentions of any judge, any court, any institution. It is a personal site.

`nshkr.com` is not blocked on Bing. It does not generate phantom 4xx errors. It is not suppressed.

The only material difference between the two domains is that `gtcode.com` publishes investigations into Judge Wilson M.N. Loo and the institutional networks surrounding him.

### What This Exhibit Eliminates

Exhibits A through D established *what* Bing is doing: domain-level suppression that catches both investigative journalism and unrelated open-source software pages. Exhibit E addresses the *how* — and eliminates the most charitable technical explanations:

- **"The site has a technical problem"** — It doesn't. HTTP 200 across all tests. One page is even marked "Indexed successfully."
- **"Cloudflare is blocking Bing's crawler"** — The control domain on the same Cloudflare configuration is not blocked.
- **"It's a hosting platform issue"** — Both domains use GitHub Pages. One is blocked. One is not.
- **"It's a CDN or DNS misconfiguration"** — Both domains use Cloudflare. One is blocked. One is not.
- **"The site is too new to be indexed"** — The site has been publishing since 2025, has a valid sitemap, and explicitly welcomes all crawlers in its robots.txt. Bing itself confirms at least one page is indexed.
- **"Individual pages have content problems"** — An open-source software documentation page with zero controversial content is blocked. A consulting page with no investigative content is "Indexed successfully" but still invisible in search. The blocking pattern is not explained by page content.

What remains after elimination: Bing's infrastructure is generating phantom errors, selectively blocking pages, and overriding its own "Indexed successfully" status — all on a single domain, while an identical-stack domain operates normally. The diagnostic tools designed to help webmasters understand and fix problems are instead producing contradictory outputs that obscure what is actually happening.

The tools that are supposed to provide transparency are participating in the opacity.

---

*— Ekewaka Lono, 13 February 2026 (updated 18 February 2026)*

---

## How to Cite

**BibTeX:**

    @article{lono2026indexbingsearch,
      author  = {Lono, Ekewaka},
      title   = {The Index: How Bing Blocked an Entire Domain to Bury One Judge's Name},
      journal = {GTCode.com Investigations},
      year    = {2026},
      month   = feb,
      url     = {https://gtcode.com/investigation/the-index-bing-search-suppression/},
      note    = {Last modified 2026-03-01; Archived at \url{https://github.com/GTCode-Press/publications/tree/pub-20260309T180822/investigation/the-index-bing-search-suppression}}
    }

**APA:**
Lono, E. (2026, February 13). The Index: How Bing Blocked an Entire Domain to Bury One Judge's Name. *GTCode.com Investigations*. https://gtcode.com/investigation/the-index-bing-search-suppression/ (Archived at https://github.com/GTCode-Press/publications/tree/pub-20260309T180822/investigation/the-index-bing-search-suppression)

**Chicago:**
Ekewaka Lono. "The Index: How Bing Blocked an Entire Domain to Bury One Judge's Name." *GTCode.com Investigations*, February 13, 2026. https://gtcode.com/investigation/the-index-bing-search-suppression/. Archived at https://github.com/GTCode-Press/publications/tree/pub-20260309T180822/investigation/the-index-bing-search-suppression.
