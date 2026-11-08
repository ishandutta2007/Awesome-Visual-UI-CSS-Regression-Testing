# Awesome Visual UI & CSS Regression Testing

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Track Awesome List](https://www.trackawesomelist.com/badge.svg)](https://www.trackawesomelist.com/ishandutta2007/Awesome-Visual-UI-CSS-Regression-Testing/)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](https://creativecommons.org/publicdomain/zero/1.0/)

> A curated list of top Visual UI and CSS Regression Testing platforms — comparing SaaS/Hosted enterprise solutions and active open-source frameworks for catching unintended visual bugs, layout shifts, and pixel-level regressions across web and mobile user interfaces.

---

## 📋 Table of Contents

- [Sector Overview & Market Dynamics](#-sector-overview--market-dynamics)
- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
- [Open-Source Software](#-open-source-software)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)
- [License](#-license)

---

## 🌐 Sector Overview & Market Dynamics

The global visual regression and automated UI testing market is currently estimated at **$1.8 billion to $2.2 billion**, embedded within the broader **$25+ billion** automated software quality assurance industry expanding at a ~15–19% CAGR. The sector exhibits a **moderately fragmented yet top-heavy market structure**; while infrastructure giants like BrowserStack and Sauce Labs dominate broad device clouds, specialized visual AI and component testing niches remain highly competitive alongside agile open-source ecosystems.

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted visual UI and CSS regression testing platforms. Sorted in descending order by company scale (valuation / annual revenue).

| Platform | Company Valuation / Revenue | Starting Pricing Tier | Free Tier / Free Trial Limits | Key Capabilities & Ecosystem |
|:---|:---|:---|:---|:---|
| **[BrowserStack Percy](https://percy.io/)** | **~$4.0B valuation** (~$225M ARR) | **$199/month** (Percy Desktop, billed annually) | **5,000 screenshots/month** free forever (1,000 for App Percy); unlimited users & projects | Cloud DOM re-rendering, multi-browser matrix, Playwright, Cypress, Selenium, Storybook, and mobile app visual diffs. |
| **[LambdaTest SmartUI](https://www.lambdatest.com/smart-ui)** | **~$400M valuation** (~$19M ARR) | **$199/month** (billed annually for SmartUI Web) | **2,000 screenshots** lifetime free tier; or 15-day trial with full cross-browser test access | Visual AI smart pixel noise reduction, native Figma baseline comparison, Storybook integration, Playwright, and Selenium support. |
| **[Applitools Eyes](https://applitools.com/)** | **~$250M valuation** (acquired by Thoma Bravo, ~$30M ARR) | **$99/month** (Starter self-serve plan) | **14-day free trial** (up to 100 checkpoints/month free tier allowance) | Industry-leading Visual AI engine mimicking human eye perception, DOM inspection, accessibility contrast validation, and cross-environment baselining. |
| **[Sauce Labs Visual](https://saucelabs.com/products/visual-testing)** | **~$250M–$500M valuation** (~$92M ARR) | **$149/month** (Sauce Labs Cloud entry tier) | **28-day free trial** with VM/device runtime; paid entry tiers include 500 visual snapshots/month | Integrated with Sauce Labs virtual & real device cloud, hybrid diffing engine, interaction testing API, and Figma design comparison. |
| **[Chromatic](https://www.chromatic.com/)** | **~$60M–$80M valuation** (~$10M funding raised) | **$179/month** (Starter tier for 35,000 snapshots) | **5,000 snapshots/month** free forever (Chrome only, 1 user) | Built by Storybook core maintainers, SteadySnap anti-flake rendering, component-driven diffing, and Playwright/Cypress end-to-end visual tests. |
| **[Happo](https://happo.io/)** | Bootstrapped / Micro-SaaS (<$5M ARR) | **$149/month** (Starter plan for 50,000 snapshots) | **5,000 snapshots/month** free forever (Chrome only, pauses on limit); unlimited team seats | Deterministic diffing, integrated WCAG accessibility & contrast review, and native MCP server for AI coding agents (Claude Code, Cursor). |

---

## 🟩 Open-Source Software

Self-hosted, developer-friendly open-source frameworks, libraries, and platforms for automated visual UI and CSS regression testing. Sorted in descending order by GitHub stargazers count.

| Project | Stars | Stack | License | Description & Highlights |
|:---|:---:|:---|:---|:---|
| **[BackstopJS](https://github.com/garris/BackstopJS)** | [![BackstopJS Stars](https://img.shields.io/github/stars/garris/BackstopJS?style=social&color=white)](https://github.com/garris/BackstopJS/stargazers) | Node.js / Puppeteer / Playwright | MIT | Veteran visual regression tool supporting responsive DOM screenshot diffing across screen sizes, interacting with simulated user journeys, and generating self-contained HTML test reports. |
| **[pixelmatch](https://github.com/mapbox/pixelmatch)** | [![pixelmatch Stars](https://img.shields.io/github/stars/mapbox/pixelmatch?style=social&color=white)](https://github.com/mapbox/pixelmatch/stargazers) | JavaScript / Node.js | ISC | The smallest, simplest, and fastest pure JS pixel-level image comparison library. Powers diffing engines across numerous visual testing tools with anti-aliased pixel detection and perceptual difference tuning. |
| **[jest-image-snapshot](https://github.com/americanexpress/jest-image-snapshot)** | [![jest-image-snapshot Stars](https://img.shields.io/github/stars/americanexpress/jest-image-snapshot?style=social&color=white)](https://github.com/americanexpress/jest-image-snapshot/stargazers) | TypeScript / Jest | Apache-2.0 | Seamless Jest matcher produced by American Express for visual regression testing. Bridges Jest snapshot assertions with pixelmatch or SSIM image diffing inside CI/CD workflows. |
| **[loki](https://github.com/oblador/loki)** | [![loki Stars](https://img.shields.io/github/stars/oblador/loki?style=social&color=white)](https://github.com/oblador/loki/stargazers) | JavaScript / Storybook | MIT | Zero-configuration visual regression testing specifically architected for Storybook. Renders components in headless Chrome or React Native and diffs pixel shifts quickly. |
| **[lost-pixel](https://github.com/lost-pixel/lost-pixel)** | [![lost-pixel Stars](https://img.shields.io/github/stars/lost-pixel/lost-pixel?style=social&color=white)](https://github.com/lost-pixel/lost-pixel/stargazers) | TypeScript / Playwright | MIT | Open-source alternative to Percy and Chromatic. Tests Storybook, Ladle, Next.js, and static web pages locally or across CI pipelines without vendor lock-in. |
| **[reg-suit](https://github.com/reg-viz/reg-suit)** | [![reg-suit Stars](https://img.shields.io/github/stars/reg-viz/reg-suit?style=social&color=white)](https://github.com/reg-viz/reg-suit/stargazers) | TypeScript / Node.js | MIT | Plugin-driven visual regression testing CLI tool. Compares images based on Git commit hashes, stores snapshots in AWS S3 or Google Cloud Storage, and posts visual diff summary reports directly on pull requests. |
| **[Visual Regression Tracker](https://github.com/Visual-Regression-Tracker/Visual-Regression-Tracker)** | [![VRT Stars](https://img.shields.io/github/stars/Visual-Regression-Tracker/Visual-Regression-Tracker?style=social&color=white)](https://github.com/Visual-Regression-Tracker/Visual-Regression-Tracker/stargazers) | TypeScript / NestJS / React | Apache-2.0 | Complete open-source self-hosted platform providing an interactive web dashboard for visual baseline management, baseline approval workflows, and SDKs for Cypress, Playwright, Java, and .NET. |
| **[react-native-owl](https://github.com/FormidableLabs/react-native-owl)** | [![react-native-owl Stars](https://img.shields.io/github/stars/FormidableLabs/react-native-owl?style=social&color=white)](https://github.com/FormidableLabs/react-native-owl/stargazers) | TypeScript / React Native | MIT | Visual regression testing suite engineered explicitly for React Native mobile apps. Automates emulator screenshots and produces baseline pixel diff reports. |
| **[cypress-visual-regression](https://github.com/cypress-visual-regression/cypress-visual-regression)** | [![cypress-visual-regression Stars](https://img.shields.io/github/stars/cypress-visual-regression/cypress-visual-regression?style=social&color=white)](https://github.com/cypress-visual-regression/cypress-visual-regression/stargazers) | JavaScript / Cypress | MIT | Dedicated Cypress testing plugin for automated visual regression checking, providing customizable image thresholding and diff screenshot generation on test runs. |
| **[Argos](https://github.com/argos-ci/argos)** | [![Argos Stars](https://img.shields.io/github/stars/argos-ci/argos?style=social&color=white)](https://github.com/argos-ci/argos/stargazers) | TypeScript / Node.js / React | MIT | Modern open-source visual testing stack designed for developer teams and AI agents. Uses local browser capture to avoid cloud render quirks, and pairs with an interactive review UI and GitHub App integration. |
| **[differencify](https://github.com/NimaSoroush/differencify)** | [![differencify Stars](https://img.shields.io/github/stars/NimaSoroush/differencify?style=social&color=white)](https://github.com/NimaSoroush/differencify/stargazers) | JavaScript / Puppeteer | MIT | Puppeteer-powered visual regression testing library providing clean async/await API controls for capturing and evaluating web page screenshot changes. |
| **[reg-cli](https://github.com/reg-viz/reg-cli)** | [![reg-cli Stars](https://img.shields.io/github/stars/reg-viz/reg-cli?style=social&color=white)](https://github.com/reg-viz/reg-cli/stargazers) | JavaScript / Node.js | MIT | Lightweight command-line utility for comparing two image directories and generating an interactive HTML difference report, often used alongside headless browser scripts. |

---

## 📊 Comparison at a Glance

| Tool / Platform | Category | Core Capture Engine | Baseline Diff Model | Self-Hostable? | Free Plan / Allowance | Primary Use Case |
|:---|:---|:---|:---|:---:|:---|:---|
| **BrowserStack Percy** | Commercial SaaS | Cloud DOM re-render | Pixel & DOM diff | ❌ | 5,000 screenshots/month | Multi-framework cross-browser enterprise teams |
| **LambdaTest SmartUI** | Commercial SaaS | Cloud headless browsers | Visual AI noise reduction | ❌ | 2,000 screenshots lifetime | Teams using LambdaTest cloud and Figma mockups |
| **Applitools Eyes** | Commercial SaaS | Multi-SDK cloud capture | Perceptual Visual AI | ❌ | 14-day trial (100 checkpoints/mo) | High-accuracy visual diffing without false-positive flakiness |
| **Sauce Labs Visual** | Commercial SaaS | Cloud VM & real devices | Hybrid visual diff | ❌ | 28-day trial (500 snapshots on entry tier) | Existing Sauce Labs cross-browser infrastructure |
| **Chromatic** | Commercial SaaS | Cloud container rendering | SteadySnap pixel diff | ❌ | 5,000 snapshots/month | Storybook-centric component libraries and design systems |
| **Happo** | Commercial SaaS | Cloud cross-browser | Deterministic sub-pixel diff | ❌ | 5,000 snapshots/month | Combined layout, WCAG accessibility, and AI agent workflows |
| **BackstopJS** | Open-Source | Puppeteer / Playwright | Pixel diff & thresholding | ✅ | Free / Open-source (MIT) | Standalone CI visual regression testing with HTML reports |
| **pixelmatch** | Open-Source | Headless Canvas / Buffers | Perceptual pixel diff | ✅ | Free / Open-source (ISC) | High-performance low-level image comparison engine |
| **jest-image-snapshot** | Open-Source | Jest test harness | Pixelmatch / SSIM | ✅ | Free / Open-source (Apache-2.0) | Unit & integration visual assertions in Jest environments |
| **loki** | Open-Source | Chrome / Storybook | Image diffing | ✅ | Free / Open-source (MIT) | Frictionless visual regression testing for Storybook stories |
| **lost-pixel** | Open-Source | Playwright local | Holistic image diffing | ✅ | Free / Open-source (MIT) | Open-source alternative to Percy & Chromatic |
| **reg-suit** | Open-Source | Bring your own capture | Git hash S3/GCS diffing | ✅ | Free / Open-source (MIT) | Serverless CI-based visual regression workflows |
| **Visual Regression Tracker** | Open-Source | Multi-language SDKs | Server-side image diff | ✅ | Free / Open-source (Apache-2.0) | Self-hosted visual regression platform with review UI |
| **react-native-owl** | Open-Source | iOS / Android simulator | Screenshot pixel diff | ✅ | Free / Open-source (MIT) | Mobile UI visual regression testing in React Native apps |
| **cypress-visual-regression** | Open-Source | Cypress runner | Canvas diffing | ✅ | Free / Open-source (MIT) | End-to-end visual tests directly inside Cypress |
| **Argos** | Open-Source | Local browser runner | Cloud or local image diff | ⚠️ (Managed preferred) | Open-source code (MIT) / Managed tier | Modern UI visual review workflow with GitHub integration |
| **differencify** | Open-Source | Chrome / Puppeteer | Blink-diff / Pixelmatch | ✅ | Free / Open-source (MIT) | Quick Puppeteer-based snapshot test automation |
| **reg-cli** | Open-Source | CLI file system | Pixelmatch diffing | ✅ | Free / Open-source (MIT) | Fast CLI image directory comparison and reporting |

---

## 🤝 Contributing

Contributions are welcome! If you would like to submit a new open-source visual UI testing library or updated SaaS platform details:

1. Fork this repository.
2. Ensure the tool is actively maintained and relevant to visual UI / CSS regression testing.
3. For open-source projects, include the official GitHub star badge (`https://img.shields.io/github/stars/<owner>/<repo>?style=social&color=white`) linking to its stargazers page.
4. Open a pull request with a concise overview of what the tool accomplishes and why it stands out.

---

## 📄 License

This repository and curated list are released under the [Creative Commons Zero v1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/) (Public Domain). Respective trademarks, logos, and software projects belong to their individual owners.
