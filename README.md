# FitRoster Marketing URL

This folder contains a static release marketing page for FitRoster.

Current structure:

- `index.html` is a single static page with built-in copy for English, Simplified Chinese, Traditional Chinese, Japanese, Korean, Thai, Malay, Russian, German, French, and Spanish.
- `support.html` is the public App Store support page with contact, FAQ, usage-guide, product, and privacy links in the same language set.
- `privacy.html` is the public App Store privacy policy page with the same multilingual language structure.
- `assets/site-i18n.js` provides shared language metadata, browser-language detection, manual language switching, and the added multilingual copy used by all three pages.
- `assets/iphone-*.jpg` and `assets/ipad-*.jpg` are complete screenshots captured from the running FitRoster iOS Simulator build. The iPad screenshots are landscape captures for release-page presentation.
- `assets/start-silver-fitroster.png` is the release logo asset copied from `Import Data/FitRoster Logo/start_silver_fitroster.PNG`.
- `assets/guides/` stores usage-guide PDFs. The Traditional Chinese guide is available now, with English and Simplified Chinese slots reserved in the page UI.

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

Adding future usage-guide languages:

- Put the localized PDF in `assets/guides/`.
- Update the matching guide card in `index.html` from reserved to available.
- Keep the locale naming explicit, for example `FitRoster_User_Guide_en.pdf` or `FitRoster_User_Guide_zh-Hans.pdf`.
