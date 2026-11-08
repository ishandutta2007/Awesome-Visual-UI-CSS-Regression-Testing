# Awesome-Visual-UI-CSS-Regression-Testing

# Awesome Visual UI & CSS Regression Testing

> A curated list of top Visual UI and CSS Regression Testing platforms — both SaaS/Hosted commercial solutions and open-source alternatives for catching unintended visual changes in web and mobile interfaces.  
> 🌟 Star this repo if you find it useful! 🌟

---

## 📋 Table of Contents

- [SaaS / Hosted Platforms](#-saas--hosted-platforms)
  - [BrowserStack Percy](#browserstack-percy)
  - [Applitools Eyes](#applitools-eyes)
  - [Chromatic](#chromatic)
  - [Sauce Labs Visual Testing](#sauce-labs-visual-testing)
  - [LambdaTest SmartUI](#lambdatest-smartui)
  - [Happo](#happo)
- [Open-Source Software](#-open-source-software)
  - [Argos](#argos)
  - [reg-suit](#reg-suit)
  - [Visual Regression Tracker](#visual-regression-tracker)
  - [visualcheck](#visualcheck)
- [Comparison at a Glance](#-comparison-at-a-glance)
- [Contributing](#-contributing)

---

## 🟦 SaaS / Hosted Platforms

Commercial, cloud-hosted Visual UI and CSS Regression Testing platforms. These are not open-source but are included as reference points for feature comparison.

### BrowserStack Percy
**Type:** Cloud visual testing integrated with BrowserStack suite  
Percy captures screenshots from your tests and compares them against baselines in BrowserStack's cloud, where the DOM is re-rendered for consistency. It supports Playwright, Cypress, Selenium, Puppeteer, WebdriverIO, and Storybook. Percy is now bundled into BrowserStack's broader testing platform, with pricing integrated into annual plans rather than sold standalone. Internal survey data cited by BrowserStack claims Percy increased visual review accuracy for users [citation:1]. **Consideration:** Because Percy re-renders the DOM in its cloud rather than capturing locally, there is a second rendering environment separate from your test browser, which can occasionally produce differences unrelated to actual code changes [citation:13].

### Applitools Eyes
**Type:** AI-powered visual validation with Visual AI  
Applitools uses its Visual AI engine to replicate human perception, filtering out rendering noise and flagging only meaningful UI changes [citation:2]. It validates across browsers, devices, and viewports with automated maintenance that learns from approvals. Gartner reviewers highlight integration features and dashboard usability, with baseline management and auto-maintenance mode as standout capabilities [citation:2]. Applitools also covers functional, API, and accessibility testing alongside visual regression. **Pricing** is quote-based; third-party sources cite starting points around $99–199/month for smaller checkpoint volumes, with enterprise tiers for advanced AI analysis [citation:12]. **Trade-off:** First-time configuration requires writing a test framework, and the most advanced AI features are gated to enterprise plans [citation:12].

### Chromatic
**Type:** Cloud visual testing built for Storybook (with Playwright/Cypress support)  
Chromatic is built by the Storybook maintainers and has the deepest Storybook integration of any visual testing tool. It builds your Storybook, renders every story in its own cloud infrastructure, and screenshots each one [citation:13]. The "SteadySnap" anti-flake rendering (September 2025) stabilizes cloud captures. Pricing is snapshot-based and multiplies across stories × viewports × browsers: Free plan includes 5,000 snapshots/month on Chrome only; Starter is $179/month for 35,000 snapshots (adds Safari, Firefox, Edge); Pro is $399/month for 85,000; overages cost $0.008 per snapshot [citation:13]. **Limitation:** Deployments are Storybook-only, and E2E visual coverage is not its center of gravity [citation:13].

### Sauce Labs Visual Testing
**Type:** Visual testing within Sauce Labs device cloud  
Sauce Visual is integrated into Sauce Labs' virtual and real device cloud. Plans include 500 monthly snapshots on entry tiers, with smart hybrid diff, Figma integration, and an interaction testing API [citation:4][citation:14]. Suited for teams already using Sauce Labs for cross-browser and mobile testing who want visual regression in the same platform. **Consideration:** Snapshot allowances are relatively low on standard plans, so heavy visual testing may require add-ons or enterprise negotiation.

### LambdaTest SmartUI
**Type:** Visual regression with Figma and Storybook support  
SmartUI by LambdaTest (now TestMu AI) captures screenshots, compares against approved baselines, and uses Visual AI to filter pixel noise like anti-aliasing and font rendering [citation:15]. It works with Playwright, Selenium, and Cypress, and can test Figma designs and Storybook screenshots directly. The free plan includes 2,000 screenshots; paid plans start at $199/month billed annually [citation:15]. Positioned for teams wanting visual testing alongside LambdaTest's cross-browser cloud.

### Happo
**Type:** Visual and accessibility testing with AI agent integration  
Happo offers a free plan with 5,000 snapshots/month in Chrome and no credit card required [citation:6]. It catches layout, accessibility (WCAG contrast), and motion regressions in a single review, with deterministic diffs that filter sub-pixel noise. A standout feature is its **MCP server** for AI coding agents: Claude Code and Cursor can read every diff in a pull request, fix regressions, and hand back a passing PR [citation:6]. Unlimited users on every plan. Accessibility testing is included on all tiers, not sold separately.

---

## 🟩 Open-Source Software

Self-hosted, community-driven Visual UI and CSS Regression Testing tools. All listed projects offer source code you can deploy on your own infrastructure.

### Argos
**Stack:** TypeScript / Node.js / PostgreSQL / S3 | **License:** MIT  
Argos is the leading open-source visual testing platform, with the entire stack — backend, frontend, and screenshot comparison engine — developed openly under MIT [citation:10]. Your tests (Playwright, Cypress, Storybook, Vitest, or any pipeline producing screenshots) capture images in your real browser, upload them to Argos, and it diffs against baselines on every pull request [citation:10][citation:13]. It also compares non-image files (JSON, Markdown, HTML), detects flaky tests, and deploys PR previews of Storybook or static sites. Agent-ready with structured JSON output and CLI review. **Important:** Argos is operated as a managed cloud service and is the supported way to run it. Self-hosting is **not officially supported or documented** — the production setup targets AWS and depends on PostgreSQL, RabbitMQ, Redis, S3, DynamoDB, plus GitHub App and Stripe integrations [citation:10]. **Pricing** for the managed service: Pro is $100/month flat with 35,000 screenshots included, versus $179/month for the same volume on Chromatic [citation:13].  
**Best for:** Teams wanting an MIT-licensed visual testing platform with local capture (your real browser), file-format flexibility, and a managed option that is significantly cheaper than Chromatic at volume.

### reg-suit
**Stack:** Node.js / CLI | **License:** MIT  
reg-suit is a command-line visual regression testing tool inspired by snapshot testing. It compares current images against previous images, generates an HTML report, and stores snapshots in external cloud storage (AWS S3, Google Cloud Storage) [citation:8]. Its plugin architecture handles key generation (git-hash-based comparison), publishing (S3/GCS), and notifications (GitHub PR comments, GitLab merge requests, Slack, Chatwork). It works on any CI service and local machines. **Trade-off:** It is a CLI harness, not a full platform — you bring your own screenshot capture step and storage, and review happens via the generated HTML report rather than a hosted dashboard.  
**Best for:** Teams wanting a lightweight, plugin-driven CLI for visual regression that integrates into existing CI pipelines without a hosted service.

### Visual Regression Tracker
**Stack:** TypeScript / Java / .NET | **License:** Apache-2.0  
A self-hosted visual regression tracking platform with a backend and frontend application for tracking differences via image comparison [citation:9]. SDKs and agents are available for Java, JavaScript, .NET, Playwright, and Cypress. The GitHub organization shows active maintenance across repositories (last updates March–April 2026 for the core backend/frontend) [citation:9]. Provides a web UI for reviewing diffs and managing baselines, making it a more complete self-hosted alternative to pure CLI tools.  
**Best for:** Teams wanting a self-hosted visual regression platform with a web UI and SDKs for multiple languages/frameworks.

### visualcheck
**Stack:** Python / Playwright | **License:** MIT  
visualcheck is a Python-based visual regression checker with a **Figma-first baseline approach**. It prioritizes Figma design baselines over runtime captures, then falls back to runtime if no Figma baseline exists. Features include pixel diff + SSIM comparison, ignore regions (e.g., cookie banners, chat widgets), and a self-contained HTML report [citation:7]. Configuration is YAML-based (`visualcheck.yaml`), with environment-specific URLs, desktop/mobile viewports, and thresholds. Installation is via `pip install visualcheck` with Playwright's Chromium.  
**Best for:** Teams designing in Figma wanting design-to-code visual validation with a simple Python CLI and HTML reporting.

---

## 📊 Comparison at a Glance

| Software | License | Capture Model | Hosted | Self-Hosted | Free Tier | Best For |
|----------|---------|---------------|--------|-------------|-----------|----------|
| **BrowserStack Percy** | Proprietary | Cloud re-render | ✅ | ❌ | (BrowserStack plans) | BrowserStack suite users |
| **Applitools Eyes** | Proprietary | Cloud Visual AI | ✅ | ❌ | Trial | AI noise filtering + enterprise |
| **Chromatic** | Proprietary | Cloud render | ✅ | ❌ | 5,000 snapshots | Storybook-centric teams |
| **Sauce Labs Visual** | Proprietary | Cloud device cloud | ✅ | ❌ | 500 snapshots | Sauce Labs users |
| **LambdaTest SmartUI** | Proprietary | Cloud | ✅ | ❌ | 2,000 snapshots | LambdaTest ecosystem |
| **Happo** | Proprietary | Cloud | ✅ | ❌ | 5,000 snapshots | AI agents + accessibility |
| **Argos** | MIT | Local capture, cloud diff | ✅ (managed) | ⚠️ Not supported | (Managed plan) | Open-source + local capture |
| **reg-suit** | MIT | CLI (your capture) | ❌ (DIY) | ✅ (CLI) | ✅ | Plugin-driven CI visual regression |
| **Visual Regression Tracker** | Apache-2.0 | Self-hosted platform | ❌ | ✅ | ✅ | Self-hosted UI + SDKs |
| **visualcheck** | MIT | Local (Playwright) | ❌ | ✅ | ✅ | Figma-first design validation |

---

## 🤝 Contributing

Contributions are welcome! If you know of an open-source Visual UI or CSS Regression Testing tool that should be listed here, please open a pull request with:

- Project name and URL
- Brief description (1–2 sentences)
- Stack and license
- Why it stands out

Please ensure the project is actively maintained (releases within the last 12 months) and genuinely open-source. Note that the open-source ecosystem for visual testing is smaller than for feature flags or API clients; many available tools are CLI harnesses or self-hosted platforms rather than full SaaS equivalents.

---

## 📄 License

This list is released under CC0 1.0 Universal (Public Domain). The software projects listed retain their respective licenses.

---

⭐ **If this list helped you discover a useful tool, please star the repo!** ⭐
