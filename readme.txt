AWNINGS & SIGNS UNLIMITED — SOURCE PACKAGE (.dc.html)
=====================================================
Built 2026-07-26. Current version only.

WHAT IS HERE
------------
Awnings and Signs Unlimited.dc.html   Landing page — EDITABLE SOURCE
Custom Patio Covers.dc.html           Service page template — EDITABLE SOURCE
support.js                            Runtime. Required. Do not edit.
image-slot.js                         Photo component. Required.
uploads/                              All 18 project photographs
robots.txt                            Crawler rules incl. AI bots — DOMAIN ROOT
sitemap.xml                           XML sitemap — DOMAIN ROOT
llms.txt                              AI-readable business brief — DOMAIN ROOT

This is the SOURCE package. The .dc.html files stay editable: open either one
in the editor and the design, copy and Tweaks panel all work.

OPENING THEM
------------
Keep every file in this folder together — the pages load support.js,
image-slot.js and uploads/ by relative path. Double-clicking works; a local
static server (e.g. "npx serve .") is more reliable in Safari.

DEPLOYING FROM THIS PACKAGE
---------------------------
A .dc.html file IS a working web page. To publish:

  1. Rename "Awnings and Signs Unlimited.dc.html" to "index.html"
  2. Rename "Custom Patio Covers.dc.html" to "custom-patio-covers.html"
  3. Upload everything into public_html, keeping uploads/ as a folder

  public_html/
  ├── index.html
  ├── custom-patio-covers.html
  ├── support.js
  ├── image-slot.js
  ├── robots.txt
  ├── sitemap.xml
  ├── llms.txt
  └── uploads/

  4. After renaming, update the cross-page links: in Custom Patio Covers the
     nav/footer point to "index.html", and the homepage footer link
     "Custom patio covers" should point to "custom-patio-covers.html".
     (The separate DEPLOY package already has this wiring done — use that one
     if you do not intend to edit further.)

robots.txt, sitemap.xml and llms.txt must sit at the web root, not in a
subfolder, or crawlers will not find them.

BEFORE YOU GO LIVE
------------------
1. FORM ENDPOINT — in each .dc.html, find "const FORM_ENDPOINT = ''" near the
   bottom and paste your form URL (Zoho Forms, serverless function, Formspree,
   Basin, or an email relay). Until then the form validates and shows the
   success state but transmits nothing.

2. CANONICAL URL — both pages declare awningsandsignsunlimited.com as
   canonical. Deploying elsewhere without updating <link rel="canonical">
   and og:url will stop the pages ranking.

3. PHONE NUMBER — pages lead with (310) 438-6544 (from your contact page).
   Yelp, ZoomInfo, YellowPages and BBB list (310) 644-9090 as primary.
   Make it consistent everywhere; mismatched NAP hurts local SEO.

4. MORE SERVICE PAGES — duplicate Custom Patio Covers.dc.html per service
   (instructions are commented at the top of its script block), then add each
   URL to sitemap.xml.

TWEAKS PANEL
------------
Three live controls on the landing page:
  headlineOption   a / b / c — three outcome-led hero headlines
  accentColor      brand red default, plus blue / green / bronze
  animationsEnabled  turn scroll reveals off

AI CRAWLERS
-----------
robots.txt explicitly allows: GPTBot, OAI-SearchBot, ChatGPT-User (OpenAI);
Googlebot, Google-Extended, GoogleOther (AI Overviews + Gemini); ClaudeBot,
Claude-User, Claude-SearchBot, anthropic-ai (Anthropic); xAI-Bot / GrokBot;
PerplexityBot, Perplexity-User; plus Bingbot, Applebot-Extended, Meta,
DuckAssistBot, Amazonbot, CCBot and cohere-ai.

Two notes:
- "GoogleAIOverviewBot" and "GoogleAISearchBot" are not real user-agent tokens.
  Google controls AI Overviews and Gemini access via Google-Extended and
  GoogleOther, both allowed. Your requested names are included but inert.
- Allowing GPTBot and CCBot also permits training use of your content. For
  AI-answer visibility WITHOUT training use, delete those two blocks and keep
  OAI-SearchBot, ChatGPT-User, Claude-SearchBot, PerplexityBot and
  Google-Extended.

WHY llms.txt MATTERS HERE
-------------------------
These pages render their content with JavaScript. Crawlers that do not execute
JS see very little. llms.txt gives them the full business brief — services,
materials, service area, process, every FAQ answer, NAP and ratings — as plain
text, so answer engines can cite you accurately regardless.

VERIFY AFTER LAUNCH
-------------------
- awningsandsignsunlimited.com/robots.txt loads
- awningsandsignsunlimited.com/llms.txt loads
- Structured data: https://validator.schema.org/
- Rich results: https://search.google.com/test/rich-results
- Submit sitemap.xml in Google Search Console and Bing Webmaster Tools

BUILD STATUS
------------
0 console errors · 0 WCAG AA contrast failures · 0 tap targets under 24px
0 horizontal overflow · 0 unresolved template holes · 0 placeholders
23/23 images loading · JSON-LD valid (LocalBusiness + 6 reviews + 8 FAQs
+ ImageGallery + WebSite/WebPage) · mobile-first verified at 360/390/414px
