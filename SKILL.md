---
name: site-setup-skill
description: Master autonomous website setup protocol for WordPress and Themixify sites. Automates header, hero slider, category curation, 3-column leveled footer, legal pages, SEO & indexing, media resizing, 404 redirects, and zero-tolerance visual QA.
---

# 🚀 Universal Site Setup Master Skill (v2.0)

## 📌 Mission & Activation Directive
When this skill is provided to any AI Assistant (Antigravity, Claude, ChatGPT, Cursor, Copilot), the AI must:
1. Ingest, memorize, and strictly enforce all 10 setup phases and Zero-Tolerance Rules below.
2. Respond immediately to the Owner:
   > *"I have fully mastered the Site Setup Skill (v2.0). All protocols, zero-tolerance rules, and phase workflows are loaded. Please provide the target website URL to begin full autonomous setup."*
3. Once the URL is provided, autonomously execute the complete setup without stopping, without asking trivial questions, and adhering strictly to the **Audit-First (Non-Destructive)** policy.

---

## ⛔ Strict Zero-Tolerance Rules (Non-Negotiable)

1. **NO DUAL SEARCH BARS (CRITICAL):**
   - Under no circumstances may a page have two search bars (e.g., top header search bar next to a giant homepage hero search bar).
   - Site-wide policy is **ZERO redundant search inputs**. If header search is disabled, ensure homepage and sidebar search inputs are also cleanly disabled unless explicitly specified otherwise.

2. **PERFECT 3-COLUMN LEVELED FOOTER (NATIVE MENUS ONLY):**
   - **Column 1 (`About`):** Editorial brand bio, physical contact address, and real official contact email (`contact@domain.com`).
   - **Column 2 (`Top Categories & Guides`):** Native WordPress Navigation Menu widget (`nav_menu`) linking to top 5–6 niche categories.
   - **Column 3 (`Legal & Transparency`):** Native WordPress Navigation Menu widget (`nav_menu`) linking to all 6 legal pages (`About Us`, `Contact Us`, `Privacy Policy`, `Terms & Conditions`, `Disclaimer`, `Affiliate Disclosure`) + FTC affiliate disclosure text block.
   - ❌ **NEVER** hardcode raw HTML links inside Custom HTML widgets. Always use native WP Navigation Menus for maintainability and theme compliance.

3. **100% TEXTLESS CATEGORY & HERO IMAGES:**
   - All category cards ("Browse by topic") and Hero banner slides must use **100% photographic, textless, WebP images**.
   - Absolutely **NO** typography, post title overlays, watermarks, or text banners inside the background images.
   - Category cards must never fall back to blog post thumbnails that have printed titles on them.

4. **THEMIXIFY MANDATORY CORE SETTINGS:**
   - **General Layout:** Site Width (`container_width`) = `1400px`, Sidebar Width = `320px`.
   - **Trending Bars:** `Sticky trending-posts bar` = **ON**, `Top bar — popular posts` = **ON**, `Posts bar auto-scroll` (marquee) = **ON**.
   - **Bottom Bars:** `Bottom bar — latest posts` = **OFF**.
   - **Single Post:** `Show featured image on single posts` = **OFF** (prevents massive redundant top image above H1).
   - **Share Bar:** `Share row under the title` = **OFF** (clean transition from title into article content).
   - **Media Resizer:** All 4 toggles = **ON** (Images: `600 × 400 px`, shrink to fit, centered, don't enlarge small images, apply to pages; Videos: `600 × 338 px` 16:9, centered).
   - **Redirects & 404:** `Send all 404s to the homepage` = **ON** (`301 — permanent`).

5. **UNIQUE EEAT AUTHOR PROFILES (STRICT WEBP < 40 KB):**
   - ❌ **NEVER REUSE AVATARS:** Every site must have a 100% unique persona, unique name, and completely distinct face. No two sites may ever share an author headshot.
   - **Niche-Specific Persona:** Author appearance and biography must naturally fit the site niche (e.g., veteran mechanical pitmaster for gas grills, tactical hobby technician for gel blasters).
   - **Format & Size:** Strictly `.webp`, `400x400` to `500x500 px`, compressed under **40 KB** for instant load time.

6. **AUDIT-FIRST (NON-DESTRUCTIVE) INTEGRATION POLICY:**
   - Before connecting or creating Google Analytics 4 (GA4), Search Console (GSC), or Bing Webmaster Tools, **ALWAYS audit first**.
   - 🛑 **IF** a valid Measurement ID (`G-XXXXXXXXXX`) or verified GSC property is already active: **DO NOT TOUCH OR OVERWRITE IT**.
   - ✅ **ONLY IF** it is completely empty or missing, proceed with configuration. Never overwrite working tracking IDs or destroy historical traffic data.

---

## 🛠️ Step-by-Step 10-Phase Autonomous Workflow

### Phase 1: Pre-Flight Audit & Credentials Inspection
- Inspect WordPress theme version, active plugins (Themixify, LiteSpeed Cache), and database options.
- Perform an initial audit of `Themixify -> Analytics` and external services before taking action.
- Trash the default `Sample Page` and default placeholder "Hello world!" post if present.

### Phase 2: Theme Layout & General Settings
- Navigate to **Themixify -> General** (`admin.php?page=themixify-general`):
  - Set `Site width (px)` to `1400`.
  - Enable `Sticky trending-posts bar`, `Top bar — popular posts`, and `Posts bar auto-scroll`.
  - Disable `Bottom bar — latest posts` and `Show featured image on single posts`.
  - Save changes.

### Phase 3: Media Resizer & Single Post Polish
- Navigate to **Themixify -> Media Resizer** (`admin.php?page=themixify-media-resizer`):
  - Image Resizer: Enable `Resize in-article images` (`600 × 400 px`, `Shrink to fit`, `Center`, `Don't enlarge small images` ON, `Also apply to pages` ON).
  - Video Resizer: Enable `Resize in-article videos` (`600 × 338 px`, `Center`).
  - Save changes.
- Navigate to **Themixify -> Share Bar** (`admin.php?page=themixify-share-bar`):
  - Turn **OFF** `Share row under the title`.
  - Save changes.

### Phase 4: Header & Primary Navigation
- Upload high-resolution Logo (`.png` / `.svg`) and 512×512 Favicon.
- Navigate to **Appearance -> Menus** (`nav-menus.php`):
  - Create **"Primary Header Menu"**: Include `Home` + top 4–6 core niche categories.
  - Assign to `primary` theme location.
- Remove redundant search bars from header or hero section.

### Phase 5: Hero Banner & Visual Identity
- Navigate to **Themixify -> Homepage** (`admin.php?page=themixify-homepage`):
  - Upload 2–3 cinematic, 100% text-free, landscape (`1600x900 px`) WebP/JPG banner slides.
  - Set strong niche headline, sub-headline, and high-contrast CTA buttons.
  - Style secondary CTA buttons with clean contrast (`#ffffff` solid background with dark text) via Custom CSS if needed.

### Phase 6: Category Curation ("Browse by topic")
- Navigate to **Posts -> Categories** (`edit-tags.php?taxonomy=category`):
  - Ensure all posts are categorized into 4–6 clean niche categories with zero uncategorized posts.
  - For each category, upload and assign a dedicated, **100% TEXTLESS** WebP image (`800x533 px`, < 100 KB) into the `themixify_cat_image` field.
  - Never allow category cards to fall back to blog post thumbnails with printed titles.

### Phase 7: Legal Pages & EEAT Compliance
- Create or update the 6 mandatory legal pages:
  1. `/about-us/` (Comprehensive editorial mission, testing methodology, author bio).
  2. `/contact-us/` (Interactive form, official email, phone, physical address).
  3. `/privacy-policy/` (GDPR/CCPA compliant).
  4. `/terms-conditions/` (Standard terms of service).
  5. `/disclaimer/` (Educational & informational disclaimer).
  6. `/affiliate-disclosure/` (FTC compliant disclosure + 301 redirect from `/disclosure/`).
- Ensure no duplicate H1/H2 headers repeating the page title and no dummy `#` links.

### Phase 8: Leveled 3-Column Footer with Native Menus
- Navigate to **Appearance -> Menus** (`nav-menus.php`):
  - Create **"Footer Categories"** menu (all top niche categories).
  - Create **"Footer Legal"** menu (all 6 legal pages).
- Navigate to **Appearance -> Widgets** (`widgets.php`):
  - **Footer Column 1:** Text widget with Brand About bio, physical address, and contact email.
  - **Footer Column 2:** Navigation Menu widget with Title `Top Categories & Guides` and Menu `Footer Categories`.
  - **Footer Column 3:** Navigation Menu widget with Title `Legal & Transparency` and Menu `Footer Legal`, plus FTC Affiliate Disclosure text.
  - **Blog Sidebar (`sidebar-blog`):** Purge 100% empty to prevent misplaced cards in category archives.

### Phase 9: Redirection & SEO Health
- Navigate to **Themixify -> Redirects** (`admin.php?page=themixify-redirects`):
  - Enable `Send all 404s to the homepage` (`301 — permanent`).
  - Add redirect from `/disclosure/` to `/affiliate-disclosure/`.
- If GA4 / Search Console are not yet connected, set up Measurement ID, submit `sitemap.xml`, and configure IndexNow / Bing API.

### Phase 10: Final Quality Audit & Proof Verification
- Purge LiteSpeed Cache (`purge_all`) and Themixify Speed Cache.
- Perform live verification:
  - Homepage: 1400px container, top sliding trending bar active, zero duplicate search bars.
  - "Browse by topic": All category cards display crisp textless photos and clear titles.
  - Footer: Symmetrical 3-column leveled layout with working native links.
  - Single Post: No featured image banner above title, no share row under title, unique WebP author box in sidebar.
  - 404 Check: Request non-existent URL (e.g., `/random-test-404-check/`) and verify 301 redirect to homepage.
- Capture full-viewport proof screenshots and present the final report.

---

## 🔄 Continuous Self-Evolution Protocol
Whenever the Owner introduces a new requirement, setting, or design fix:
1. Immediately apply the change to the target website.
2. Update this `SKILL.md` file under the appropriate phase or zero-tolerance section.
3. Commit and push the update directly to GitHub: `https://github.com/tntayyab/site-setup-skill`.
4. Ensure all future setups benefit from the newly evolved protocol.
