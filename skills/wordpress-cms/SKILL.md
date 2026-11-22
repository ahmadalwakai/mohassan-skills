---
name: مواقع WordPress وأنظمة إدارة المحتوى
description: مواقع ووردبريس وأنظمة إدارة المحتوى: القوالب، الإضافات، Elementor، WooCommerce، الحماية، السرعة، النسخ الاحتياطي، أعطال التحديثات، نقل الموقع. wordpress wp woocommerce elementor plugin plugins theme themes cms gutenberg wix squarespace ووردبريس وورد بريس الووردبريس إضافة إضافات اضافات قالب قوالب
version: 1.0.0
category: coding
---
Use this for WordPress and similar site builders.
1. Before any change: a full backup of files and database, and a staging copy for anything risky. Most hosts and backup plugins provide both.
2. Site broken after an update: enable WP_DEBUG_LOG to read the real error. If the dashboard is unreachable, rename the plugins folder (or one plugin's folder) through SFTP or the host file manager to disable plugins, then re-enable them one at a time; switch to a default theme the same way. Restore the backup if needed and repeat the update on staging.
3. Plugins: fewer is better. Choose maintained ones (recent updates, many installs, good support), delete unused ones, and never install pirated premium plugins.
4. Hardening: current core, themes and plugins; unique strong admin passwords with two-factor sign-in; no "admin" username; limited login attempts; least-privilege roles; a web application firewall; HTTPS everywhere; file editing disabled in the dashboard.
5. Speed: decent hosting on PHP 8.x with object caching, a page cache plugin, a CDN, compressed WebP images, lazy loading, few fonts and sliders, page builders used sparingly.
6. WooCommerce: test checkout end to end after every update, try payment gateways in test mode first, document stock and tax settings.
7. SEO basics: clean permalinks, an SEO plugin for titles and sitemaps, one H1 per page, alt text.
8. Migration: copy files and database, run a serialization-aware search and replace for URLs, then check links, forms and outgoing email.
Answer shape: the likely cause, then numbered steps the owner can follow, with risky steps marked.
