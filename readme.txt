# UniPixel

> Server-side conversion tracking for WordPress and WooCommerce. Meta, Google, TikTok, Pinterest, Microsoft. From your own server. No GTM. No external cloud. No per-platform repetition.

[Install from WordPress.org](https://wordpress.org/plugins/unipixel/) ·
[Documentation](https://unipixelhq.com/unipixel-docs/) ·
[Report an issue](https://github.com/unipixelhq/unipixelhq/issues) ·
[Changelog](#changelog)

---

## What it is

UniPixel is a WordPress plugin that sends conversion and event tracking data directly from your WordPress server to ad platforms: Meta, Pinterest, TikTok, Google, and Microsoft. It does server-side tracking without GTM server containers, third-party cloud services, or external hosting.

WooCommerce events are handled automatically. The Centralised Event Manager lets you set up custom conversions across every platform in one shot. The built-in consent layer ships with 18 languages, editable text per language, multiple layout styles, and reads from nine third-party CMPs if you already use one.

---

## Why server-side tracking

Browser-based tracking is failing. Ad blockers, iOS privacy controls and browser restrictions hide a growing share of your real conversions from your ad platforms. iOS 14.5 alone dropped reported Meta conversions by 30 to 40% for many advertisers. Ad blocker adoption sits around 43%.

Your ad platforms make automated decisions about who sees your ads, how much to bid, and where to spend your budget, all based on the conversion data they receive. If that data is incomplete, every decision is wrong. You pay more to reach worse audiences. You kill campaigns that were actually working. You scale campaigns that aren't.

Server-side tracking sends events directly from your server to each platform's official API, bypassing what blocks the browser. The result is more accurate conversion reporting, better algorithm performance, and ad spend that works harder.

---

## Why WordPress changes the picture

Most server-side tracking tools assume you can't run code on your server. WordPress already runs PHP on your server. It can call platform APIs directly.

The whole server-side tracking industry is built around a problem WordPress doesn't have:

- "You need a GTM server container." Not on WordPress. You need a plugin.
- "Server-side tracking requires cloud hosting." Not on WordPress. Your hosting already runs PHP.
- "Budget $100 to $150 a month for infrastructure." Not on WordPress. Your server already does this.
- "You need GTM expertise." Not with UniPixel. The plugin handles it.

UniPixel fires conversion data from the same server that serves your website, directly to the platforms. No middleman, no extra infrastructure, no container.

---

## Supported platforms

| Platform | Pixel | Server-side API | WooCommerce events | Custom events |
|---|---|---|---|---|
| **Meta** (Facebook, Instagram) | Yes | Conversions API | Yes | Yes |
| **Google** (GA4 + Ads) | Yes | Measurement Protocol | Yes | Yes |
| **TikTok** | Yes | Events API | Yes | Yes |
| **Pinterest** | Yes | Conversions API | Yes | Yes |
| **Microsoft** (Bing) | Yes | UET CAPI | Yes | Yes |

All five from one install. Event deduplication runs automatically across every platform.

---

## What's in the box

**Tracking**
- WooCommerce ecommerce events fire automatically: PageView, ViewContent, AddToCart, InitiateCheckout, AddPaymentInfo, Purchase
- Advanced Matching sent through to every platform that supports it
- Automatic event deduplication across all five platforms

**Custom conversions**
- Centralised Event Manager: pick a conversion (Lead, Newsletter Signup, Contact, Registration, or your own) once and UniPixel fires it across every platform you've enabled with the correct standard event name per platform: Meta `Lead`, Google `generate_lead`, TikTok `Contact`, Pinterest `Lead`, Microsoft `lead`
- URL-based event triggers: pick a thank-you page or lead page from a dropdown. No CSS, no GTM
- Custom click events via element targeting

**Consent**
- Built-in consent popup: 18 languages out of the box, editable text per language, five layout styles, optional non-blocking mode, mobile-responsive
- Third-party CMP support: OneTrust, Cookiebot, Osano, Silktide, Orest Bida, Complianz, CookieYes, Moove GDPR, CookieAdmin (Softaculous)

**Operations**
- Event log inside the WordPress admin
- Live event console for debugging
- Server response logging per event

---

## How UniPixel compares

|  | UniPixel | PixelYourSite Pro | Pixel Manager Pro | Conversios Pro | Meta for WooCommerce |
|---|---|---|---|---|---|
| Meta Conversions API | Yes | Yes | Pro | Pro | Yes |
| Google Measurement Protocol | Yes | Pro | Pro | Pro | No |
| TikTok Events API | Yes | Pro | Pro | Pro | No |
| Pinterest Conversions API | Yes | Add-on | Pro | Pro | No |
| Microsoft UET CAPI | Yes | Add-on | Pro | Pro | No |
| Self-hosted server-side | Yes | Yes | No (vendor cloud) | No (GTM container) | Yes (Meta only) |
| GTM required | No | No | No | Yes | No |
| Centralised cross-platform event setup | Yes | No | No | No | No |
| URL-based event triggers (no CSS) | Yes | No | No | No | No |
| Built-in multi-language consent popup | Yes (18 languages) | Separate plugin | Built-in | Built-in | No |
| Works on non-WooCommerce sites | Yes | Yes | No | No | No |

Full case-by-case comparisons:

- [UniPixel vs PixelYourSite](https://unipixelhq.com/blog/unipixel-vs-pixelyoursite/)
- [UniPixel vs Stape](https://unipixelhq.com/blog/stape-alternatives-wordpress/)
- [UniPixel vs Conversios](https://unipixelhq.com/blog/unipixel-vs-conversios/)
- [UniPixel vs Meta for WooCommerce](https://unipixelhq.com/blog/unipixel-vs-meta-for-woocommerce/)

---

## Install

UniPixel ships through the WordPress plugin directory.

→ **[Install from WordPress.org](https://wordpress.org/plugins/unipixel/)**

This GitHub repository is the public home for documentation, release notes, issues, and reference material. The plugin source you install on your site is published from the WordPress.org plugin repository.

---

## Documentation

Full setup guides, platform-specific walkthroughs, troubleshooting and reference material live at [unipixelhq.com/unipixel-docs](https://unipixelhq.com/unipixel-docs/).

---

## Support and issues

For broken behaviour or unexpected results, file an issue here. The templates ask for the platform context we need to reproduce.

For setup questions and "how do I", start with the [documentation](https://unipixelhq.com/unipixel-docs/) and the [WordPress.org support forum](https://wordpress.org/support/plugin/unipixel/).

---

## Changelog

Recent releases. Full history in [Releases](https://github.com/unipixelhq/unipixelhq/releases).

- **v2.6.6**: Centralised Event Manager. Cross-platform conversion creation with auto-filled standard event names per platform. URL-based custom event triggers (pick a page, no CSS). Standard event name dropdowns when defining custom events.
- **v2.6.5**: Consent popup style options (5 layouts), optional Reject all button, CookieAdmin third-party CMP support, mobile-responsive popup, plus admin polish.
- **v2.6.4**: Multi-language consent popup. 18 languages with admin-editable text per language.
- **v2.6.0 to 2.6.3**: Microsoft CAPI full implementation, AddToCart fragment pixel for AJAX add-to-cart, InitiateCheckout session-based deduplication.

---

## License

GPLv2 or later. See [LICENSE](LICENSE).

Built and maintained from Australia.

---

> **Try UniPixel: server-side tracking from the server you already have.**

<!-- release: v2.5.3 -->

<!-- release: v2.6.0 -->

<!-- release: v2.6.4 -->

<!-- release: v2.6.5 -->

<!-- release: v2.6.6 -->
