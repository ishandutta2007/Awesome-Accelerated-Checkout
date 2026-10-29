# Awesome-Accelerated-Checkout

# Awesome-Accelerated-Checkout

**Top Accelerated Checkout (Opensource) 🌟 Star if you like it! 🌟**



**Curated List of SaaS Products & Open-Source GitHub Projects**

*Focused on One-Click Checkout, Digital Wallets, Payment Orchestration & Express Payment Buttons*

**Last updated: October 2026**



This repository tracks notable **SaaS platforms** and **open-source projects** for **Accelerated Checkout**. These tools enable merchants to reduce checkout friction, recognize returning shoppers, and complete transactions with saved payment and shipping details—from proprietary wallet networks with hundreds of millions of stored profiles to self-hosted payment orchestration layers that give merchants full control over routing, retries, and processor relationships.



**Examples** include Shop Pay, Apple Pay, Google Pay, PayPal One Touch, Amazon Pay, Click to Pay, Link by Stripe, Bolt, Venmo, and Fast (the category leaders and cautionary tales in commercial space).



**Open-source emphasis**: This section is expanded with every relevant project for self-hosting, payment orchestration, and open checkout infrastructure. **Critical note**: True open-source accelerated checkout—a wallet network with saved shopper profiles—does not exist. Open-source projects address **payment infrastructure** (orchestration, routing, processor abstraction) rather than proprietary buyer recognition networks.



Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.



## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)

- [Open-Source GitHub Projects](#open-source-github-projects)

- [How to Contribute](#how-to-contribute)

- [Disclaimer](#disclaimer)



## SaaS/Hosted Platforms



- **[Shop Pay](https://shop.app/)**

  **Shopify's accelerated checkout** with saved payment and shipping details across a network of **250M+ shoppers in 24 countries** . Converts up to **50% higher than guest checkout** and at least 10% better than other accelerated wallets according to Shopify-commissioned research; average order value runs about 16% higher . Available off-Shopify via the **Shop Pay Commerce Component**, which requires Shopify Payments eligibility and collects email before payment . **Pricing**: Same Shopify Payments fees as standard processing; no additional charges . **Free tier**: None (requires Shopify Payments). **Best for**: merchants on Shopify or custom platforms wanting access to the largest proprietary accelerated checkout network.



- **[Apple Pay](https://www.apple.com/apple-pay/)**

  **Apple's wallet and payment authorization** for web and apps. Requires Apple Developer Program membership, a Merchant ID, and a Payment Processing Certificate; integration through a supported PSP or direct Apple Pay JS APIs . **Pricing**: No direct Apple fees; standard processor fees apply. **Free tier**: None (developer membership required). **Best for**: merchants wanting Face/Touch ID authorization with strong privacy positioning and broad iOS/Mac shopper coverage.



- **[Google Pay](https://pay.google.com/)**

  **Google's payment API** for web and Android. Integrates via `PaymentsClient` JavaScript, with `isReadyToPay` to detect saved payment methods and `loadPaymentData` to present the payment sheet . **Pricing**: No direct Google fees; processor fees apply. **Free tier**: None. **Best for**: merchants wanting Android/Chrome shopper coverage with a familiar Google account-based flow.



- **[PayPal One Touch](https://www.paypal.com/)**

  **PayPal's persistent login** that keeps customers signed in for up to **6 months**, enabling return visits without re-entering passwords or payment details . Supported through Recurly and other gateways. **Pricing**: Standard PayPal merchant fees. **Free tier**: None. **Best for**: merchants with existing PayPal volume wanting to maximize repeat purchase conversion for PayPal users.



- **[Amazon Pay](https://pay.amazon.com/)**

  **Amazon account-based checkout** using saved addresses and payment methods. Available as an external wallet in gateways like Razorpay (India, up to ₹20,000 per transaction) . **Pricing**: Standard Amazon Pay merchant fees. **Free tier**: None. **Best for**: merchants selling to Amazon-accustomed shoppers wanting a recognizable, trusted checkout option.



- **[Click to Pay](https://clicktopay.com/)**

  **Card network-backed accelerated checkout** (Visa, Mastercard, Amex, Discover) that recognizes shoppers by email and sends a one-time password for authentication. Integrated via Adyen as a standalone component or alongside card fields . **Pricing**: Standard card processing fees; no additional Click to Pay surcharge. **Free tier**: None. **Best for**: merchants wanting card-based acceleration without pushing shoppers into a proprietary wallet ecosystem.



- **[Link by Stripe](https://link.com/)**

  **Stripe's saved payment details network** that autofills customer information across Stripe-powered checkouts. Stripe claims Link increases conversion by **over 7%** . Available through Stripe Checkout with no additional fees beyond standard card pricing . **Pricing**: Same as standard Stripe card fees. **Free tier**: None (requires Stripe account). **Best for**: Stripe merchants wanting network-effect acceleration without integrating a separate wallet button.



- **[Bolt](https://www.bolt.com/)**

  **One-click checkout, identity, and payments platform** offering hosted checkout, embeddable checkout, and "Checkout Everywhere" buy-now links/QR codes. Product suite includes Bolt ID, Check-In (passwordless login), fraud scoring, and subscriptions . **Valuation collapsed 97%** from $11B (2022) to $300M; currently raising a **$27M pay-to-play bridge round** with the CEO personally committing $5M . Headcount reduced from 900 to ~60 . **Pricing**: Quote-only. **Free tier**: None. **Best for**: merchants evaluating alternatives to Shop Pay with awareness of vendor stability risk.



- **[Venmo](https://venmo.com/)**

  **PayPal-owned social payment app** with merchant checkout via Braintree. US-only for merchant payments; recurring/automatic payments require **express prior written approval** from PayPal plus one-time authorization, customer consent, notice, and cancellation procedures . **Pricing**: Standard Braintree/Venmo merchant fees. **Free tier**: None. **Best for**: US merchants targeting Venmo-active demographics, particularly younger shoppers.



- **[Fast](https://fast.co/)** (**Defunct**)

  **One-click checkout startup that shut down abruptly in April 2022** after raising ~$125M (including a $102M Series B led by Stripe) and burning ~$10M/month on just $600K in annual revenue . Its collapse is a widely cited cautionary tale about checkout startups competing against entrenched networks like Shop Pay and PayPal without product-market fit or sustainable unit economics . **Pricing**: N/A. **Free tier**: N/A. **Best for**: historical reference—**do not build on this platform**.



## Open-Source GitHub Projects



- **[Hyperswitch](https://github.com/juspay/hyperswitch)**

  **Open-source payment orchestration platform** (Apache 2.0 for core; suite includes app server, web client, vault, control center, and WooCommerce plugin) — **the most significant open-source infrastructure for accelerated checkout-adjacent problems**. **Features**: Single API to access **100+ payment processors** (Stripe, Adyen, Braintree, Worldpay, Checkout.com, Cybersource) across **130+ countries**; smart routing and automatic retries to improve authorization rates; seamless failover between processors; PCI-compliant card vault; Control Center for analytics . **Tech stack**: Rust (core), TypeScript/React (web), Terraform for AWS/GCP deployment. **Deploy**: Self-hosted (Terraform modules) or Hyperswitch Cloud (hosted). **Trade-off**: **Orchestration layer, not a consumer wallet**—it does not provide a saved-shopper network or one-click buyer recognition. It solves the merchant-side problem of processor lock-in, routing, and retry logic. **Best for**: merchants wanting to reduce dependency on a single processor, improve success rates via smart routing, and own their payment infrastructure—the closest open-source analog to the *merchant-side* value Bolt attempted to provide.



- **[FluentCart](https://github.com/fluent-cart/fluent-cart)**

  **Open-source WordPress eCommerce solution** (GPLv3) with **one-click checkout** as a built-in feature alongside coupons, subscriptions, licenses, and a headless REST API . **Features**: Performance-first architecture with separate shop tables and dynamic asset loading; 3× faster order processing claimed; zero bloat plugin; full code auditability . **Tech stack**: PHP (WordPress). **Deploy**: WordPress plugin (self-hosted). **Trade-off**: **WordPress-specific**—one-click checkout is a feature within a full eCommerce plugin, not a network-effect wallet. No shopper identity network across merchants. **Best for**: WordPress store owners wanting a lightweight, open-source eCommerce platform with one-click checkout built in.



- **[Amwal Magento Plugin](https://github.com/amwal-tech/amwal-magento)**

  **One-click checkout plugin for Magento 2** (license per repo) — **a narrow, platform-specific implementation** enabling instantaneous purchases from product, mini-cart, and cart pages . **Tech stack**: PHP (Magento 2). **Deploy**: Magento 2 extension. **Trade-off**: **Magento-only**; low community validation (1 star); no broader payment orchestration or wallet network. **Best for**: Magento 2 merchants wanting a basic one-click checkout extension.



- **[Quick Checkout for WooCommerce](https://github.com/noruzzamans/Quick-Checkout-Direct-Checkout-Button-Quick-View-for-WooCommerce)**

  **WooCommerce plugin that simplifies the checkout process** (license per repo) — **a checkout UX simplification tool**, not a wallet or one-click network . **Tech stack**: PHP (WooCommerce). **Deploy**: WordPress plugin. **Trade-off**: **Minimal scope**; streamlines existing checkout fields rather than recognizing returning shoppers or storing payment details across merchants. **Best for**: WooCommerce store owners wanting a faster checkout form without network effects.



- **[BTCPay Server](https://github.com/btcpayserver/btcpayserver)**

  **Self-hosted, open-source Bitcoin payment gateway** (MIT) — **zero-fee, no-KYC payment processing** with a WooCommerce plugin, Lightning Network support, and full invoice management . **Features**: Direct P2P payments to your wallet; no middlemen; QR code checkout; automated refunds and reporting; multilingual . **Tech stack**: .NET (C#). **Deploy**: Self-hosted or third-party host. **Trade-off**: **Bitcoin/Lightning only**—not a traditional accelerated checkout for cards or wallets. No shopper recognition network. **Best for**: merchants wanting to accept Bitcoin with zero processing fees and full sovereignty over funds.



- **[OpenReceive](https://pypi.org/project/openreceive/)**

  **Python library for Bitcoin/Lightning checkout** (MIT) — **a receive-only wallet integration** for Django, FastAPI, and SQLAlchemy applications . **Features**: Lightning invoices created in your connected wallet; optional swaps from USDT/USDC/ETH/SOL; receive-only NWC connection (cannot spend funds); persistent payment attempts with idempotent settlement . **Tech stack**: Python. **Deploy**: Embedded in Python applications. **Trade-off**: **Bitcoin/crypto only**; developer-library, not a checkout UI or wallet network. **Best for**: Python developers wanting to add Lightning checkout to their application without custodial risk.



- **[TPT Pay](https://github.com/tpt-solutions/tpt-payments)**

  **Self-hostable payment API with double-entry ledger** (MIT) — **a Stripe-API-compatible alternative** in early development. **Features**: REST API compatible with Stripe v2024-06-20; append-only double-entry ledger; webhook engine; card network adapter abstraction (sandbox adapter shipped; bank sponsor/direct acquiring adapters planned) . **Tech stack**: Go, PostgreSQL, NATS JetStream, HashiCorp Vault. **Deploy**: Docker Compose / self-hosted. **Trade-off**: **Early-stage**; no production card acquiring path shipped (sandbox only); no shopper wallet or acceleration features. **Best for**: developers wanting a Stripe-API-compatible ledger foundation to build payment infrastructure upon.



- **[D613 Pay (WooCommerce)](https://wordpress.org/plugins/d613-pay/)**

  **WooCommerce plugin for Zelle, Venmo, PayPal, and Cash App** (free plugin; Auto-Verify paid add-on) — **manual payment confirmation with optional email-based auto-verification** . **Features**: Branded pay page per rail with handle/email/phone/QR code; Pending Confirmation order status; Auto-Verify reads bank/wallet payment alert emails (DKIM/DMARC verified) to confirm orders . **Tech stack**: PHP (WordPress). **Deploy**: WordPress plugin. **Trade-off**: **Manual/email-based confirmation**, not one-click checkout. Venmo here is used as a **payment rail with manual confirmation**, not Braintree's Venmo merchant integration. **Best for**: small merchants wanting to accept peer-to-peer payment apps without per-transaction processor fees.



### Additional Strong Open-Source Options



- **BTCPay for GiveWP** — Bitcoin donation gateway for GiveWP (MIT). Zero-fee, self-hosted, Lightning-capable . **Best for**: nonprofits wanting Bitcoin donations without processing fees.

- **Braintree Flutter Plugin** (`braintree_checkout_flutter`) — Flutter plugin for PayPal, Venmo, and card payments via Braintree (MIT per package). Vault-only; server-side capture required . **Best for**: Flutter developers wanting native Venmo/PayPal flows in mobile apps.



**Frameworks for building custom systems**: Combine **Hyperswitch** as the payment orchestration and routing layer with **BTCPay Server** or **OpenReceive** for crypto rails, and **FluentCart** or a WooCommerce plugin for storefront checkout—creating a merchant-controlled payment stack. **None of these provide the buyer-recognition network effects** that Shop Pay, Link, or PayPal One Touch deliver; that value is inherently proprietary.



## How to Contribute



1. Fork the repo.

2. Add/edit entries in `README.md` (follow existing format).

3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.

4. Submit PR with a short explanation.



Star the repo if you find it useful!



## Disclaimer



- This is a **community-curated** list — not exhaustive and not an endorsement.

- Accelerated checkout platforms handling payment and personal data must comply with **PCI DSS**, data protection regulations (GDPR, CCPA, etc.), and card network rules.

- **The "wallet network vs. payment infrastructure" distinction is critical.** **Shop Pay, Apple Pay, Google Pay, PayPal One Touch, Amazon Pay, Click to Pay, Link, Bolt, and Venmo** are **consumer-facing wallets/networks**—their value comes from saved shopper profiles and recognition. **Hyperswitch, BTCPay Server, OpenReceive, TPT Pay, and FluentCart** are **payment infrastructure**—they enable processing, routing, or acceptance but do **not** provide a cross-merchant shopper network. **No open-source project replicates the network effects of Shop Pay or Link.**

- **Fast is included as a historical cautionary tale, not a recommendation.** The company shut down in April 2022 after raising ~$125M and burning ~$10M/month on ~$600K annual revenue . Its failure illustrates the difficulty of competing against entrenched wallets without sustainable economics . **Do not build on defunct infrastructure.**

- **Bolt's stability is uncertain.** Its valuation collapsed 97% from $11B to $300M, and it is currently raising a $27M pay-to-play bridge round described by TechCrunch as potentially "the company's last shot at survival" . **Evaluate vendor risk carefully before committing.**

- **Shop Pay's off-Shopify availability depends on Shopify Payments eligibility.** The Commerce Component requires email collection before payment and engineering work against Shopify APIs—not a plugin install . **Verify eligibility and integration effort before planning.**

- **Hyperswitch is the most substantive open-source project in this space**, but it solves **merchant-side orchestration** (processor routing, retries, failover), not consumer acceleration . It is the right tool if you want to reduce processor lock-in and improve authorization rates; it is not a Shop Pay replacement.

- Self-hosted open-source solutions require proper server setup, backup configuration, and ongoing maintenance. **Payment infrastructure is security-critical**—ensure your hosting meets PCI DSS requirements and your organization's security standards before processing live transactions.



---



**Made for developers, merchants, and organizations building transparent checkout infrastructure.**

Let's make Accelerated Checkout more open, data-driven, and merchant-friendly.
