# FitRoster Marketing URL

This folder contains a static release marketing page for FitRoster.

Current structure:

- `index.html` is a single static page with built-in copy for English, Simplified Chinese, and Traditional Chinese.
- `privacy.html` is the public App Store privacy policy page with the same English, Simplified Chinese, and Traditional Chinese language structure.
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
- Use `https://fox3nova.github.io/fitroster/privacy.html` as the App Store Connect Privacy Policy URL.

Adding future usage-guide languages:

- Put the localized PDF in `assets/guides/`.
- Update the matching guide card in `index.html` from reserved to available.
- Keep the locale naming explicit, for example `FitRoster_User_Guide_en.pdf` or `FitRoster_User_Guide_zh-Hans.pdf`.
