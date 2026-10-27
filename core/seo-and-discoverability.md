# SEO and Public Discoverability Standard

SEO is a product and architecture concern for public content—not a plugin added just before launch. No technical checklist guarantees ranking; the team controls accessibility to crawlers, content structure, metadata, URLs, performance, and quality practices, but not search-engine outcomes.

## 1. Decide applicability and goals
At discovery, classify each route family as public/indexable, public/noindex, authenticated/private, or hybrid. Identify target audiences, search intent, language/region, conversion goals, content owner, and analytics/privacy constraints. Record why SEO is important or not applicable.

## 2. Rendering and crawl strategy
Before implementation, compare SSR, static generation, incremental regeneration, build-time prerendering, and client-side rendering by route family. Consider:
- whether meaningful content and links are present in initial HTML;
- freshness and personalization requirements;
- page count and publishing cadence;
- hosting/runtime constraints and failure modes;
- cache invalidation and deployment complexity;
- performance, accessibility, and JavaScript dependency;
- internal search and crawler behavior.

Do not assume client-side rendering is always unacceptable, or that SSR automatically creates good SEO. Choose based on evidence and test the actual response. Record the decision in an ADR. For SEO-critical content, do not ship a client-only approach without demonstrating crawler-visible content and a documented justification.

## 3. URL and localization design
- Use stable, human-readable, canonical URLs.
- Define a consistent language strategy (for example path prefixes) before publishing content.
- Provide correct `hreflang` alternates only for genuinely equivalent localized pages; include self-references and reciprocal consistency.
- Use canonical URLs for the preferred version of duplicate/near-duplicate content; do not canonicalize unrelated pages together.
- Avoid indexing internal search results, empty/filter combinations, preview pages, admin areas, or low-value parameter variants by default.
- Plan redirects for URL changes; avoid chains and loops; preserve relevant intent and measure 404s.

## 4. Page-level metadata and semantics
Each indexable page should have a unique, accurate title and useful meta description where appropriate, a meaningful main heading and semantic structure, a canonical URL, language declaration, sensible Open Graph/social metadata, and descriptive internal-link text. Metadata must match visible page content and must not be keyword-stuffed.

## 5. Crawl controls and index management
- Return correct HTTP status codes (200, 301/308, 404, 410, 401/403 as appropriate).
- Treat `robots.txt` as crawl guidance, not access control or a reliable way to remove a URL from an index.
- Keep noindex pages accessible to crawlers if they need to see the noindex directive; do not accidentally block them first.
- Include only canonical, indexable, intended URLs in XML sitemaps; update last-modified values only when content meaningfully changes.
- Keep staging/private environments protected; do not rely on obscure URLs.
- Verify robots, sitemap, redirects, canonical, and status codes after deployment.

## 6. Structured data
Use supported, relevant structured data only when page content satisfies the applicable specification. Validate syntax and eligibility, avoid fabricated reviews/offers/organization facts, and do not assume valid markup guarantees a rich result. Treat markup as a representation of visible, accurate content.

## 7. Content and information architecture
Organize content around user intent and clear page purpose. Ensure valuable pages are reachable through meaningful internal links. Avoid mass-generated near-duplicate pages, doorway pages, hidden keyword text, copied content, and unsubstantiated claims. Define content quality, authorship/subject expertise where relevant, freshness, and editorial ownership.

## 8. Performance and user experience
Set a performance budget based on user needs and measurement. Measure real-user Core Web Vitals when available and supplement with lab tests. Prioritize mobile experience, responsive layout, image dimensions/formats, appropriate loading, caching, payload size, server latency, and JavaScript cost. Passing one lab test is not proof of real-user performance.

## 9. Accessibility and media
Use semantic HTML, keyboard access, visible focus, appropriate labels, sufficient contrast, meaningful image alternatives, captions/transcripts where relevant, and accessible interactive components. Accessibility is not only an SEO tactic; it is an independent quality requirement.

## 10. Measurement
Before launch, define ownership for search-performance tools and analytics, if appropriate and privacy-compliant. Monitor indexed/canonical pages, sitemap processing, crawl errors, redirects/404s, search impressions/clicks, conversion, and real-user performance. Distinguish measurement correlation from causation.

## SEO acceptance checklist
For each indexable route family, verify:
1. Expected URL returns the right status.
2. Primary content and important internal links are present and discoverable in the actual rendered response.
3. Title, description, language, canonical, and applicable hreflang are correct.
4. Robots/index directives do what is intended.
5. Sitemap contains the canonical indexable URL and excludes inappropriate pages.
6. Redirects and old URLs behave correctly.
7. Structured data is accurate and validated where used.
8. Mobile usability, accessibility, and performance budgets are tested.
9. Content is useful, unique enough for its purpose, and linked from relevant pages.
10. Monitoring/ownership and post-release validation are assigned.
