# FitRoster Marketing URL

This folder contains a static release marketing page for FitRoster.

Current structure:

- `index.html` is a single static page with built-in copy for English, Simplified Chinese, Traditional Chinese, Japanese, Korean, Thai, Malay, Russian, German, French, and Spanish.
- `guide.html` is the multilingual HTML usage guide subpage. It covers setup, editable exercise names, custom exercises, coach-trainee workflows, records, analysis, backup, and settings with language- and device-specific screenshot paths.
- `support.html` is the public App Store support page with contact, FAQ, usage-guide, product, and privacy links in the same language set.
- `privacy.html` is the public App Store privacy policy page with the same multilingual language structure.
- `assets/site-i18n.js` provides shared language metadata, browser-language detection, manual language switching, and the added multilingual copy used by all three pages.
- `assets/iphone-*.jpg` and `assets/ipad-*.jpg` are complete screenshots captured from the running FitRoster iOS Simulator build. The iPad screenshots are landscape captures for release-page presentation.
- `assets/start-silver-fitroster.png` is the release logo asset copied from `Import Data/FitRoster Logo/start_silver_fitroster.PNG`.
- `assets/guide-screenshots/<locale>/` stores localized screenshots used by the HTML usage guide.
- `assets/guides/` stores legacy usage-guide PDFs. The Traditional Chinese PDF remains available as an archive while the release guide moves to HTML.

Open locally:

```bash
open Docs/MarketingURL/index.html
```

Deploy target:

- Deploy the whole `Docs/MarketingURL/` folder, including `assets/`.
- Replace the release contact link with the final public App Store or production support URL when available.
- Use this page as the App Store Connect marketing URL after it is published on a public HTTPS host.
- Use `https://fox3nova.github.io/fitroster/support.html` as the App Store Connect Support URL.
- Use `https://fox3nova.github.io/fitroster/privacy.html` as the App Store Connect Privacy Policy URL.

Language behavior:

- The pages detect `navigator.languages` and map supported locales to the closest available FitRoster language.
- Manual language selection is available from the top navigation and is saved in `localStorage` under `fitroster.marketing.language`.

Usage-guide screenshots:

- Run `Scripts/capture_release_screenshots.py` with the built simulator app to write App Store screenshots, manual screenshots, and the website guide screenshot copy.
- Website guide screenshots are copied to `assets/guide-screenshots/<locale>/<device>/`.
- The HTML guide uses the selected site language and each image's device target to load matching iPhone and iPad screenshot folders.

Adding future usage-guide PDF archives:

- Put the localized PDF in `assets/guides/`.
- Keep the locale naming explicit, for example `FitRoster_User_Guide_en.pdf` or `FitRoster_User_Guide_zh-Hans.pdf`.
