# Bing Indexing Diagnostics

> Contradictory webmaster diagnostics, partial visibility, and technical transparency for an independent publisher

**Author:** Ekewaka Lono
**Published:** February 13, 2026
**Last Modified:** May 13, 2026
**Canonical URL:** https://gtcode.com/diagnostics/bing-search-indexing-anomaly/
**Section:** Investigations
**License:** [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

---

Bing's own tools reported inconsistent states for gtcode.com depending on the page inspected: blocked, not discovered, invisible in public search, or indexed successfully. Public search behavior later shifted while remaining incomplete: a subsequent `site:gtcode.com` search displayed "About 50 results" while visibly surfacing only one gtcode.com URL on the captured first page, a non-investigative technical article. The investigation corpus remained absent from the visible first-page result set reviewed from the screenshot.

This article documents Bing Webmaster diagnostic contradictions. Ordinary technical explanations are considered first: crawler scheduling, stale diagnostics, site-scan bugs, CDN/crawler mismatch, canonicalization, transient HTTP behavior, quality classifiers, policy systems, duplicate handling, index freshness, and public-result rendering differences. The exhibits narrow some of those explanations. The current evidence does not identify any human actor inside or outside Microsoft.

Record posture: the current evidence shows contradictory diagnostics and selective public-search behavior. Actor identity, complaint source, policy trigger, intent, and content causation require Bing records, crawler logs, policy notices, support responses, or other technical evidence.

On February 12, 2026, a routine check of Bing Webmaster Tools and public search showed that `gtcode.com` — this site — returned zero visible public results on Microsoft's search engine. Not low-ranked. Not deprioritized. *Zero.*

The evidence comes from Microsoft's own tools.

---

## Exhibit A: The February 12 Disappearance

On February 12, 2026, a `site:gtcode.com` search on Bing returned no visible results.

![Bing search for site:gtcode.com returning zero visible results on February 12, 2026](https://gtcode.com/img/bing-block-site-search.webp)

*"There are no results for site:gtcode.com."*

The domain has published investigative journalism and open-source software documentation since 2025. It has a valid sitemap, a robots.txt that explicitly welcomes all crawlers, valid structured data, and no technical barriers to indexing.

---

## Exhibit B: The Investigation Page

URL Inspection of the most recent investigation — "[The Nod: Visual Allegation, Audio Sequence, and Review Gap](https://gtcode.com/hawaii-courts/the-nod-visual-allegation/)" — returns **"Not discovered."**

![Bing URL Inspection showing "Not discovered" for The Nod investigation page](https://gtcode.com/img/bing-block-wilson-loo-not-discovered.webp)

*"URL cannot appear on Bing. The inspected URL is not known to Bing."*

The narrow explanation is straightforward: a new page awaiting crawl. Later exhibits show a broader site-level diagnostic anomaly. The "Request indexing" button exists, but the question is why a site with a valid sitemap and no crawl barriers requires manual page-by-page submission while other URLs on the same domain show blocked or contradictory statuses.

---

## Exhibit C: The Control Case

This is the exhibit that first indicated the diagnostic pattern was not limited to one article.

URL Inspection of `gtcode.com/repos/agent_session_manager/` — an open-source Elixir software package page — returns **"Blocked."**

![Bing URL Inspection showing "Blocked" for open-source Elixir package](https://gtcode.com/img/bing-block-agent-session-manager.webp)

*"The inspected URL is known to Bing but has some issues which are preventing us from serving it to our users. We recommend you to follow Bing Webmaster Guidelines."*

The inspected URL points to documentation for an open-source Elixir library — `agent_session_manager` — a technical package for managing AI agent sessions. It contains:

- API documentation
- Installation instructions
- Code examples
- A link to the Hex.pm package registry

The page contains ordinary software material. It names no judge, court, institution, party, allegation, or journalism subject. It resembles thousands of other open-source project pages indexed on Bing every day.

And yet: **"Blocked."**

Note the distinction. Exhibit B says "Not discovered" — Bing claims it hasn't seen the page. Exhibit C says the URL **"is known to Bing"**. Bing's tools reported it as blocked after discovery. An open-source software page was crawled, reviewed, and blocked.

The shared attribute is the domain name. No Hawaii accountability claim depends on this Bing article.

---

## Technical Pattern

The process question here is technical: what mechanism reduced public visibility, what ordinary explanation applies, and what record would test the cause?

The exhibits document site-level and page-level diagnostic contradictions inside Bing's own webmaster tools. Any explanation involving a policy system, third-party report, technical bug, or intent would require Bing support responses, policy notices, crawl logs, server logs, Lumen entries, reproducible crawler audits, or subsequent public-search behavior.

---

## What The Evidence Leaves Open

The current evidence does not identify any human actor inside or outside Microsoft.

Search engines use automated policy and quality systems, crawler queues, site diagnostics, and complaint-review channels. Any of those mechanisms could explain reduced or uneven visibility. So could benign or internal explanations: stale diagnostic state, policy classifiers, quality systems, false-positive malware or spam filters, unsupported status propagation, and public-search rendering differences. These exhibits establish the anomaly while leaving complaint history, policy trigger, technical bug, and actor identity unresolved.

The open questions are complaint history, policy trigger, technical explanation, or another site-level diagnostic or policy state.

---

## The Open Questions

1. **Has a third-party content removal request been filed against gtcode.com?** Bing Webmaster Tools withholds this information from site owners.

2. **Does the Lumen Database contain any takedown requests affecting this domain?** *(Under investigation.)*

3. **Are the same pages indexed on Google, DuckDuckGo, and other search engines?** If the same Elixir package page indexes everywhere except Bing, the visibility anomaly is Bing-specific.

4. **What is the specific "issue" preventing the agent_session_manager page from being served?** Bing's error message is vague. A software documentation page with no investigative content is a strong control case.

5. **When did the visibility problem begin relative to publication dates and site changes?** Timeline comparison can screen ordinary technical explanations against the observed public-search change. Any actor-specific explanation would require actor-specific evidence.

---

## The Evidence Standard

This investigation applies the same standard as every other piece published on this site: **show the receipts.**

The initial exhibits are screenshots from Microsoft's own Bing Webmaster Tools and public search results, taken on February 12, 2026, by the verified site owner. They are primary-source outputs showing that:

1. The entire domain was publicly invisible on Bing on February 12, 2026
2. Investigation pages are "Not discovered"
3. Bing's tools reported an open-source software page as known to Bing and unable to be served to users

The screenshots are the primary sources. The later May 12 screenshot materially updates the public-search condition from total public invisibility to partial visibility.

This article documents Bing's treatment of gtcode.com as reflected in Bing Webmaster Tools and search results. Cause remains unresolved. The current record establishes a visibility anomaly and unresolved diagnostic contradictions. Causation by any specific article, person, complaint, or policy trigger requires additional technical or platform records.

---

## Update: February 15, 2026

### Exhibit D: "Not Discovered" Becomes "Blocked"

Three days after this article was published, the same investigation page from Exhibit B — "[The Nod: Visual Allegation, Audio Sequence, and Review Gap](https://gtcode.com/hawaii-courts/the-nod-visual-allegation/)" — was re-inspected using Bing Webmaster Tools.

The status has changed.

![Bing URL Inspection showing "Blocked" for The Nod investigation page, February 15, 2026](https://gtcode.com/img/bing-block-nod-blocked-20260215.webp)

On February 12, this page was **"Not discovered"** — Bing claimed it had never seen it. On February 15, the status reads **"Blocked"**:

> *"URL cannot appear on Bing. The inspected URL is known to Bing but has some issues which are preventing us from serving it to our users. We recommend you to follow Bing Webmaster Guidelines."*

This is the same message, word for word, that appeared on the open-source Elixir software page in Exhibit C. The distinction between the two exhibits has collapsed. Both pages — a judicial-accountability investigation and an open-source software library — are now identically blocked.

What this confirms: Bing discovered the investigation page sometime in the three-day window between February 12 and February 15. Its tools then reported the same "Blocked" status that had already caught the software repository. Bing's tools represented the page as known and unable to appear.

Bing's tools reported a blocking status after discovery.

---

## Update: February 18, 2026

### Exhibit E: The Phantom Error

Six days after the initial documentation, and three days after Exhibit D showed Bing's tools reporting blocked status on a newly discovered page, a standard diagnostic step was taken: a Site Scan was initiated through Bing Webmaster Tools. This is Microsoft's own tool for webmasters — designed to identify technical problems that might prevent a site from appearing in search results. The purpose is to help site owners fix their sites.

The scan completed. An email confirmation arrived from Bing Webmaster Tools (`bingwb@microsoft.com`):

![Bing Webmaster Tools email confirming site scan completion for gtcode.com, February 18, 2026](https://gtcode.com/img/bing-block-scan-email-20260218.webp)

*"Scan initiated in Bing Webmaster with name test is now available."*

The scan report contained a single finding: **"ERROR: Http 400-499 errors"** — on the homepage.

![Bing Site Scan showing HTTP 400-499 errors for gtcode.com root URL, February 18, 2026](https://gtcode.com/img/bing-block-scan-4xx-20260218.webp)

The scan reached **page depth 0**. It could not get past the front door. According to Bing's own diagnostic infrastructure, `https://gtcode.com/` is returning an HTTP client error — a 4xx status code — which means the server is supposedly rejecting the request.

There is one problem with this finding: **the reported error fails external reproduction.**

The homepage returns HTTP 200 — the standard success response — to every user agent tested, including Bing's own crawler signature (`Mozilla/5.0 (compatible; bingbot/2.0; +http://www.bing.com/bingbot.htm)`). It returns 200 over HTTP/1.1 and HTTP/2. It returns 200 with no user agent at all. The page loads. The content renders. The tests showed no server-side rejection.

This was tested independently on February 18, 2026, using multiple user agents and protocol versions against the live site. Every request succeeded. Outside Bing's own infrastructure, the reported 4xx error could not be reproduced.

A URL Inspection was then run on the homepage itself — the same URL the Site Scan claimed was returning 4xx errors:

![Bing URL Inspection showing "Discovered but not crawled" and "URL cannot appear on Bing" for gtcode.com homepage, February 18, 2026](https://gtcode.com/img/bing-block-homepage-not-crawled-20260218.webp)

The result: **"Discovered but not crawled. URL cannot appear on Bing."** The crawl section states: *"The inspected URL is known to Bing but has some issues which are preventing indexation."* The tool supplied a vague advisory to "follow Bing Webmaster Guidelines" without a specific actionable explanation.

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
| `/hawaii-courts/the-nod-visual-allegation/` | Judicial-accountability investigation | **Blocked** |
| `/repos/agent_session_manager/` | Open-source Elixir software docs | **Blocked** |
| `/consulting/` | Services page | **Indexed successfully** |

Bing's own URL Inspection tool reported that a consulting page on `gtcode.com` was indexed and could appear in search results. But Exhibit A showed that, on February 12, 2026, a `site:gtcode.com` search on Bing returned **zero visible results**. Not reduced results. Not filtered results. Zero.

So Bing's tools simultaneously claim:
- The homepage was "Discovered but not crawled" — yet the Site Scan reports a 4xx error on the same URL, which requires a crawl attempt
- The homepage has been known to Bing since 2017 but was supposedly never crawled in eight years
- The consulting page is indexed and can appear — but the domain returned nothing in public search on February 12
- The investigation and software pages carry "Blocked" statuses
- The homepage generates a phantom 4xx error that fails external reproduction

Four different URL statuses from the same toolset, on the same domain, on the same day — plus a Site Scan that contradicts the URL Inspection of the same page. As of February 18, the one page Bing claimed was fine still failed to surface in public `site:` search. The anomaly operated above the page-level status — at a layer that overrode Bing's own inspection results.

### The Control Domain

There is a second domain on the identical infrastructure stack: `nshkr.com`. Same static site generator (Hugo). Same hosting platform (GitHub Pages). Same CDN and DNS provider (Cloudflare). Same domain registrar. Same deployment pipeline.

`nshkr.com` is a personal site with no investigative journalism, judicial-accountability reporting, or mentions of any judge, court, or institution.

`nshkr.com` loads normally in Bing, generates no phantom 4xx errors, and shows no comparable visibility anomaly.

One reason this anomaly was reviewed is that `gtcode.com` publishes public-interest investigation pages. That context explains the review priority. Content causation remains unresolved.

### What This Exhibit Eliminates

Exhibits A through D established what Bing's tools were reporting in February: a site-level diagnostic pattern that caught both investigative journalism and unrelated open-source software pages. Exhibit E addresses the *how* — and eliminates several ordinary technical explanations:

- **"The site has a technical problem"** — HTTP 200 across all tests. One page is even marked "Indexed successfully."
- **"Cloudflare is blocking Bing's crawler"** — The control domain on the same Cloudflare configuration loads normally.
- **"It's a hosting platform issue"** — Both domains use GitHub Pages. Bing reports blocking on gtcode.com while the control domain behaves normally.
- **"It's a CDN or DNS misconfiguration"** — Both domains use Cloudflare. Bing reports blocking on gtcode.com while the control domain behaves normally.
- **"The site is too new to be indexed"** — The site has been publishing since 2025, has a valid sitemap, and explicitly welcomes all crawlers in its robots.txt. Bing itself confirms at least one page is indexed.
- **"Individual pages have content problems"** — An open-source software documentation page with zero controversial content is blocked. A consulting page with no investigative content is "Indexed successfully" while remaining absent from public site-search on February 18. Page content fails as a complete explanation for the blocking pattern.

What remains after elimination: Bing's infrastructure generated phantom errors, reported blocked statuses on selected pages, and overrode its own "Indexed successfully" status — all on a single domain, while an identical-stack domain operated normally. The diagnostic tools designed to help webmasters understand and fix problems produced contradictory outputs that created practical opacity.

The practical effect was opacity from tools designed to provide transparency.

That sentence describes the practical effect of the diagnostic contradictions while leaving intent by Microsoft, Bing personnel, or any outside complainant unresolved.

---

## Update: May 12, 2026 — One Non-Investigative Result Appears

A later public Bing search for `site:gtcode.com` shifted away from the clean zero-result page documented in Exhibit A. Bing displayed "About 50 results" while visibly showing only one result from gtcode.com:

> Harness Engineering: The Discipline of Building Systems
>
> `https://gtcode.com/articles/harness-engineering`

The visible URL points to a technical article about harness engineering, outside the Oahu Underground investigation corpus. The screenshot captures the visible first-page result set, which excluded Oahu Underground investigation pages.

![Bing search for site:gtcode.com showing about 50 results but only one visible gtcode.com result, a non-investigative Harness Engineering article](https://gtcode.com/img/bing-site-gtcode-one-visible-result-20260512.png)

*Exhibit F: Bing public search for `site:gtcode.com`, showing "About 50 results" but visibly surfacing only one gtcode.com result on the captured first page, the non-investigative technical article `/articles/harness-engineering/`.*

This materially updates the evidence. The original February 12 result documented total public invisibility at that time. The later result shows partial visibility: at least one non-investigative page surfaced, while the captured visible first-page results still centered on a single technical article and excluded the investigation corpus. That pattern requires a technical explanation.

The updated pattern shifts from simple disappearance to partial visibility:

1. Bing previously returned zero visible results for `site:gtcode.com`.
2. Bing Webmaster Tools reported contradictory states across the same domain: "Not discovered," "Blocked," "Discovered but not crawled," and "Indexed successfully."
3. A later public `site:` search reported "About 50 results."
4. The visible result set surfaced only one gtcode.com page.
5. The visible page was a non-investigative technical article.
6. The captured public first-page result set excluded the investigation pages.

This leaves a narrowed diagnostics issue: a technical article can appear while the investigation corpus remains non-visible, and Bing can report a larger result count than the visible result set reflects. The records needed to evaluate that gap are crawler logs, index-status histories, policy notices, support responses, and reproducible control queries.

---

## What The Evidence Leaves Open

The evidence establishes a search-index diagnostics problem while leaving cause unresolved. The current record identifies no human actor. It leaves unresolved whether the cause was a third-party complaint, a policy system, a technical bug, a stale diagnostic state, or some combination of those factors. The May 12 update narrows the domain-wide claim: at least one non-investigative technical article surfaced. The unresolved issue is why the public result set remains selectively visible and why the captured first-page `site:` results exclude the investigation corpus despite Bing's reported result count and prior Webmaster Tools diagnostics.

## What Would Resolve This

The fastest way to resolve the diagnostics issue would be one of the following:

- a Bing support response identifying the diagnostic or policy basis;
- crawl logs showing whether Bingbot received a reproducible server-side error;
- a policy notice, URL-removal notice, or webmaster action message;
- a Lumen record or other public removal-request record;
- a reproducible third-party crawl audit showing the same problem outside Bing;
- a subsequent ordinary `site:gtcode.com` result set showing navigable coverage of the domain, including investigation pages.

## What Would Falsify This

The anomaly thesis would be materially narrowed or falsified if Bing begins returning ordinary, navigable `site:gtcode.com` results across the domain, including investigation pages; if Bing provides a documented technical explanation that reproduces externally; if a robots, CDN, sitemap, hosting, canonicalization, or structured-data error is identified and corrected; if a reconsideration response explains a neutral policy basis; or if server logs show Bingbot was blocked by site infrastructure.

The May 12 result narrows the thesis without resolving it: the captured first-page result set shows only one visible non-investigative URL, leaving partial visibility through a still-unresolved indexing anomaly as the current claim.

---

## What Happens Next

This page will be updated as additional evidence is gathered. Specifically:

- Cross-engine comparison (Google, DuckDuckGo, Brave, Yandex)
- Lumen Database search for takedown requests
- Bing reconsideration request and its outcome
- Timeline comparison between publication dates, site changes, and visibility changes
- Search `site:gtcode.com/diagnostics/` and the relevant silo path
- Search exact URLs for major investigation pages
- Compare Bing visibility of `/articles/`, `/repos/`, `/hawaii-courts/`, and `/diagnostics/`
- Search exact title strings for investigation pages
- Search exact URL strings
- Re-run URL Inspection in Bing Webmaster Tools for the homepage, `/articles/harness-engineering/`, `/hawaii-courts/the-nod-visual-allegation/`, `/hawaii-courts/open-letter-bosko-petricevic/`, and `/diagnostics/bing-search-indexing-anomaly/`
- Capture whether Webmaster Tools reports "Indexed successfully," "Blocked," "Discovered but not crawled," or other statuses for the investigation pages after the public search change
- Any response from Microsoft

The record is now public.

---

*— Ekewaka Lono, 13 February 2026 (updated 12 May 2026)*

---

## How to Cite

**BibTeX:**

    @article{lono2026bingsearchindexing,
      author  = {Lono, Ekewaka},
      title   = {Bing Indexing Diagnostics},
      journal = {GTCode.com Investigations},
      year    = {2026},
      month   = feb,
      url     = {https://gtcode.com/diagnostics/bing-search-indexing-anomaly/},
      note    = {Last modified 2026-05-13; Archived at \url{https://github.com/GTCode-Press/publications/tree/main/diagnostics/bing-search-indexing-anomaly}}
    }

**APA:**
Lono, E. (2026, February 13). Bing Indexing Diagnostics. *GTCode.com Investigations*. https://gtcode.com/diagnostics/bing-search-indexing-anomaly/ (Archived at https://github.com/GTCode-Press/publications/tree/main/diagnostics/bing-search-indexing-anomaly)

**Chicago:**
Ekewaka Lono. "Bing Indexing Diagnostics." *GTCode.com Investigations*, February 13, 2026. https://gtcode.com/diagnostics/bing-search-indexing-anomaly/. Archived at https://github.com/GTCode-Press/publications/tree/main/diagnostics/bing-search-indexing-anomaly.
