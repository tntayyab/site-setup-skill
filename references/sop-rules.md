# 📖 Themixify & WordPress Technical SOP Reference

This reference documents the exact technical keys, database options, form field names, and standard CSS overrides used across all autonomous site setups.

---

## 1. Themixify Settings Field Mapping

| Setting Page | Option Name / Field Name | Recommended Value | Notes |
| :--- | :--- | :--- | :--- |
| **General** (`themixify-general`) | `container_width` | `1400` | Site width in pixels |
| | `sidebar_width` | `320` | Sidebar width in pixels |
| | `sticky_postbar_enabled` | `1` (checked) | Sticky trending bar |
| | `postbar_top_enabled` | `1` (checked) | Top bar popular posts |
| | `postbar_marquee` | `1` (checked) | Marquee auto-scroll |
| | `postbar_bottom_enabled` | `0` (unchecked) | Disable bottom latest posts |
| | `single_featured_image` | `0` (unchecked) | Disable giant top image on posts |
| **Media Resizer** (`themixify-media-resizer`) | `resize_images` | `1` (checked) | In-article image resizing |
| | `image_width` × `image_height` | `600` × `400` | Centered, shrink to fit |
| | `dont_enlarge_small` | `1` (checked) | Prevent pixelation |
| | `apply_to_pages` | `1` (checked) | Apply to WP pages |
| | `resize_videos` | `1` (checked) | In-article video resizing |
| | `video_width` × `video_height` | `600` × `338` | Centered 16:9 ratio |
| **Share Bar** (`themixify-share-bar`) | `article_share_top` | `0` (unchecked) | Disable share row under title |
| **Redirects** (`themixify-redirects`) | `r404_enable` | `1` (checked) | Send all 404s to homepage |
| | `r404_type` | `301` | Permanent 301 redirect |
| | `r404_skip_admins` | `0` (unchecked) | Apply to all requests |
| **Homepage** (`themixify-homepage`) | `home_search_enabled` | `0` (unchecked) | Disable homepage search |
| | `themixify_hero[banners][]` | Array of image URLs | 16:9 textless WebP/JPG slides |
| | `cta_enabled` | `1` (checked) | CTA band above footer |
| | `cta_bg_image` | Image URL | Dark contrast background |
| **Category Term** (`edit-tags.php`) | `themixify_cat_image` | Image URL | Dedicated textless WebP image |

---

## 2. Standard High-Contrast Custom CSS

When hero slider secondary buttons or footers require contrast enhancement, inject the following snippet into **Themixify -> Custom CSS** (`themixify-custom-css`):

```css
/* High-Contrast Hero CTA Secondary Button */
.tf-btn.tf-btn--ghost,
.tmx-hero-btn--secondary,
.hero-slider__btn--secondary {
  background: #ffffff !important;
  color: #0f172a !important;
  border: 1px solid #ffffff !important;
  font-weight: 700 !important;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.25) !important;
}

.tf-btn.tf-btn--ghost:hover,
.tmx-hero-btn--secondary:hover {
  background: #f8fafc !important;
  color: #0284c7 !important;
}

/* Symmetrical Leveled Footer Styling */
.site-footer {
  background-color: #0f172a !important;
  color: #cbd5e1 !important;
}

.site-footer .widget-title,
.site-footer h3,
.site-footer h4 {
  color: #38bdf8 !important;
  font-weight: 700 !important;
}

.site-footer a {
  color: #94a3b8 !important;
  text-decoration: none;
}

.site-footer a:hover {
  color: #ffffff !important;
  text-decoration: underline;
}

.site-footer p {
  color: #94a3b8 !important;
  line-height: 1.6;
}
```

---

## 3. Mandatory Cache Purge Endpoints

Always purge both LiteSpeed Cache and Themixify Speed Cache after updating options:

```bash
# 1. Themixify Speed Cache:
POST /wp-admin/admin-post.php
Body: action=themixify_purge_speed_cache

# 2. LiteSpeed Cache (if active):
GET /wp-admin/admin.php?page=themixify-speed-cache&LSCWP_CTRL=purge&litespeed_type=purge_all_lscache
```
