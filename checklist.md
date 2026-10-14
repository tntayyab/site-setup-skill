# ✅ Universal Site Setup Master Checklist

Use this checklist to verify 100% compliance before delivering any completed website.

---

### Phase 1: Pre-Flight Audit & Cleanup
- [ ] Inspect existing Google Analytics 4 (GA4) status — keep intact if active.
- [ ] Inspect existing Google Search Console (GSC) status — keep intact if active.
- [ ] Inspect existing Bing Webmaster Tools & IndexNow — keep intact if active.
- [ ] Move default `Sample Page` to Trash (`post_status = trash`).
- [ ] Move default `Hello world!` post to Trash if present.
- [ ] Verify site title and tagline match niche editorial standards.

---

### Phase 2: Theme Layout & General Settings
- [ ] Navigate to `Themixify -> General` (`admin.php?page=themixify-general`).
- [ ] `Site width (px)` set to `1400`.
- [ ] `Sidebar width (px)` set to `320`.
- [ ] `Sticky trending-posts bar` = **ON**.
- [ ] `Top bar — popular posts` = **ON**.
- [ ] `Posts bar auto-scroll` (marquee) = **ON**.
- [ ] `Bottom bar — latest posts` = **OFF**.
- [ ] `Show featured image on single posts` = **OFF**.
- [ ] Changes saved and verified with HTTP 200.

---

### Phase 3: Media Resizer & Share Bar
- [ ] Navigate to `Themixify -> Media Resizer` (`admin.php?page=themixify-media-resizer`).
- [ ] `Resize in-article images` = **ON**.
- [ ] In-article image dimensions: `600 × 400 px`.
- [ ] Image fit: `Shrink to fit — whole picture, proportional never cropped`.
- [ ] Image alignment: `Center`.
- [ ] `Don't enlarge small images` = **ON**.
- [ ] `Also apply to pages` = **ON**.
- [ ] `Resize in-article videos` = **ON**.
- [ ] Video dimensions: `600 × 338 px` (16:9), `Center`.
- [ ] Navigate to `Themixify -> Share Bar` (`admin.php?page=themixify-share-bar`).
- [ ] `Share row under the title` = **OFF**.
- [ ] Changes saved and verified with HTTP 200.

---

### Phase 4: Header & Navigation
- [ ] High-resolution logo uploaded in Site Identity.
- [ ] 512×512 Favicon uploaded in Site Identity.
- [ ] Primary Menu created with `Home` + top 4–6 niche categories.
- [ ] Primary Menu assigned to `primary` theme location.
- [ ] Zero duplicate search bars: Header search disabled or verified clean.
- [ ] DOM audit verifies total search input count = 0 (or strictly 1 if requested).

---

### Phase 5: Hero Slider & Visuals
- [ ] 2–3 high-resolution 16:9 (`1600x900 px`) textless WebP/JPG slides uploaded.
- [ ] Hero headline and sub-headline tailored to niche authority.
- [ ] Primary CTA button linked to top troubleshooting category.
- [ ] Secondary CTA button linked to reviews/buying guides category.
- [ ] Secondary CTA button contrast verified (crisp `#ffffff` background with dark text).
- [ ] Homepage search section disabled below hero slider.

---

### Phase 6: Category Curation ("Browse by topic")
- [ ] All site posts categorized into 4–6 niche categories.
- [ ] Zero posts in `Uncategorized` (`count = 0`).
- [ ] Empty unused placeholder categories deleted.
- [ ] Every category term has a dedicated, 100% photographic, textless WebP image (~800x533 px, < 100 KB) in `themixify_cat_image`.
- [ ] Verified that category cards do NOT fall back to blog post thumbnails with printed titles.

---

### Phase 7: Core Legal Pages & EEAT Persona
- [ ] `/about-us/` created with editorial mission, testing lab, and author credentials.
- [ ] `/contact-us/` created with interactive form, official email, phone, and address.
- [ ] `/privacy-policy/` created and published.
- [ ] `/terms-conditions/` created and published.
- [ ] `/disclaimer/` created and published.
- [ ] `/affiliate-disclosure/` created and published.
- [ ] 301 redirect from `/disclosure/` to `/affiliate-disclosure/`.
- [ ] Zero duplicate H1/H2 headings repeating the page title.
- [ ] Zero unreplaced placeholders or dummy `#` links.
- [ ] Author persona configured with 100% unique niche-specific WebP avatar (< 40 KB).
- [ ] Author bio and social links populated in `profile.php`.

---

### Phase 8: Leveled 3-Column Footer
- [ ] "Footer Categories" menu created with top niche categories.
- [ ] "Footer Legal" menu created with all 6 legal pages.
- [ ] Footer Column 1: About Brand bio + official contact email + physical address.
- [ ] Footer Column 2: Navigation Menu widget (`nav_menu`) -> "Top Categories & Guides".
- [ ] Footer Column 3: Navigation Menu widget (`nav_menu`) -> "Legal & Transparency" + FTC Affiliate Disclosure text.
- [ ] Zero raw unmaintainable Custom HTML widgets used for menus.
- [ ] Symmetrical visual leveling across all 3 columns verified.
- [ ] `Blog Sidebar` (`sidebar-blog`) in `widgets.php` purged 100% empty (`[]`).

---

### Phase 9: Redirection & SEO Protection
- [ ] Navigate to `Themixify -> Redirects` (`admin.php?page=themixify-redirects`).
- [ ] `Send all 404s to the homepage` = **ON** (`301 — permanent`).
- [ ] Test `/random-test-404-check/` and verify 301 redirect to homepage.
- [ ] Submit XML sitemap (`/sitemap.xml` or `/sitemap_index.xml`) in Google Search Console if configuring fresh.
- [ ] Verify Bing Webmaster Tools & IndexNow API key if configuring fresh.

---

### Phase 10: Final Quality Audit & Proof Delivery
- [ ] Purge LiteSpeed Cache (`purge_all_lscache`).
- [ ] Purge Themixify Speed Cache (`themixify_purge_speed_cache`).
- [ ] Capture full-viewport proof screenshot of Homepage (1400px width + top trending bar + hero).
- [ ] Capture full-viewport proof screenshot of "Browse by topic" category grid.
- [ ] Capture full-viewport proof screenshot of Leveled 3-Column Footer.
- [ ] Capture full-viewport proof screenshot of Single Post (no top image, no share row under title, unique WebP author box).
- [ ] Capture full-viewport proof screenshot of Category Archive (clean, zero misplaced sidebar widgets).
- [ ] Present comprehensive final delivery report with clickable artifact links to Owner.
