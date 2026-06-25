# 🛡️ AdsAway

### A curated, aggressive ad & telemetry blocklist for Pi-hole, AdGuard Home, NextDNS, Technitium, and other DNS filtering platforms.

<p align="center">
  <img src="https://img.shields.io/badge/DNS%20Blocking-Network%20Wide-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Privacy-Enhanced-green?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Pi--hole-Compatible-orange?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Open%20Source-Community%20Driven-purple?style=for-the-badge" />
</p>

---

## ✨ What is AdsAway?

AdsAway is a curated DNS blocklist designed to eliminate advertising, telemetry, analytics, tracking, and marketing infrastructure across your entire network.

Unlike massive "block everything" lists, AdsAway focuses on domains that are commonly used for:

* 📢 Advertising
* 📈 Analytics
* 👣 User tracking
* 📱 Mobile ad SDKs
* 📺 Smart TV telemetry
* 🛍️ Marketing pixels
* 🕵️ Fingerprinting services

AdsAway works at the DNS layer, meaning protection applies to:

* Windows
* macOS
* Linux
* Android
* iPhone / iPad
* Smart TVs
* Streaming devices
* Game consoles
* IoT devices

No browser extension required.

---

## 🚀 Features

✅ Network-wide ad blocking

✅ Blocks major ad networks

✅ Blocks telemetry and analytics endpoints

✅ Blocks mobile advertising SDKs

✅ Helps reduce tracking and fingerprinting

✅ Compatible with Pi-hole, AdGuard Home, NextDNS, Technitium, and dnsmasq

✅ Lightweight and easy to maintain

---

## 🎯 Blocked Platforms

AdsAway includes coverage for infrastructure commonly associated with:

| Platform           | Coverage |
| ------------------ | -------- |
| Google Ads         | ✅        |
| DoubleClick        | ✅        |
| Microsoft Ads      | ✅        |
| Amazon Advertising | ✅        |
| TikTok Ads         | ✅        |
| X (Twitter) Ads    | ✅        |
| Facebook Tracking  | ✅        |
| Instagram Tracking | ✅        |
| Yahoo Advertising  | ✅        |
| Yandex Advertising | ✅        |
| Pinterest Tracking | ✅        |
| Quora Tracking     | ✅        |
| InMobi             | ✅        |
| IronSource         | ✅        |
| PostHog Analytics  | ✅        |
| Snowplow Analytics | ✅        |
| FingerprintJS      | ✅        |

---

## ⚠️ Aggressive Blocking Notice

AdsAway prioritizes privacy and ad reduction.

Some domains included in the list may affect:

* Social media integrations
* Login widgets
* Embedded comments
* Certain mobile app features
* Smart TV advertising systems

Most users will not notice any issues, but advanced users should review logs and whitelist domains if needed.

---

# 📥 Installation

## Pi-hole

### Method 1 — Web Interface

Open:

```text
Settings → Adlists
```

Add the AdsAway URL:

```text
https://raw.githubusercontent.com/YOUR_USERNAME/adsaway/main/adsaway.txt
```

Click:

```text
Add Adlist
```

Then update gravity:

```bash
pihole -g
```

or

```text
Tools → Update Gravity
```

---

### Method 2 — Command Line

SSH into your Pi-hole server:

```bash
sudo nano /etc/pihole/adlists.list
```

Add:

```text
https://raw.githubusercontent.com/ChalkClayAte/blocklist/refs/heads/main/adsaway
```

Then run:

```bash
pihole -g
```

---

## AdGuard Home

Navigate to:

```text
Filters → DNS Blocklists
```

Add:

```text
https://raw.githubusercontent.com/YOUR_USERNAME/adsaway/main/adsaway.txt
```

Save and update filters.

---

## NextDNS

Navigate to:

```text
Security → Denylist
```

Import the list URL or domains manually.

---

## Technitium DNS

Open:

```text
DNS Apps → Block Lists
```

Add the AdsAway URL and refresh blocklists.

---

# 🔄 Updating

AdsAway is designed to be subscribed to directly.

When your DNS platform refreshes blocklists, you'll automatically receive the latest updates.

No manual downloads required.

---

# 📊 Philosophy

AdsAway follows a simple principle:

> Block what is clearly advertising, tracking, telemetry, and analytics infrastructure.

The project intentionally avoids:

* Malware signatures
* Country-specific censorship
* Adult-content filtering
* Political filtering
* Social-media blocking

AdsAway focuses solely on reducing ads and tracking.

---

# 🛠️ Reporting False Positives

Found a domain that breaks a service?

Please open an issue and include:

* Domain name
* Service affected
* Steps to reproduce
* Screenshots (if applicable)

We aim to keep AdsAway aggressive but usable.

---

# ❓ Frequently Asked Questions

### Does AdsAway block YouTube ads?

Partially.

DNS filtering can block some supporting ad infrastructure, but YouTube serves many advertisements from the same systems used to deliver video content.

For complete YouTube ad blocking, browser-based content blockers are still required.

---

### Does AdsAway replace uBlock Origin?

No.

AdsAway works at the DNS level.

uBlock Origin works at the browser level.

Using both provides the best experience.

---

### Will AdsAway speed up browsing?

Potentially.

Blocking ad servers, trackers, and analytics requests can reduce the number of network requests made by websites and apps.

---

### Why are some ads still visible?

Modern platforms often serve advertisements from the same domains used for normal content.

DNS filtering cannot distinguish between content and advertisements when both originate from the same hostname.

---

### Is AdsAway safe?

AdsAway only blocks DNS lookups to known advertising, tracking, telemetry, and analytics domains.

No traffic inspection or device modifications are performed.

---

# 🤝 Contributing

Contributions are welcome.

You can help by:

* Reporting false positives
* Suggesting new domains
* Improving documentation
* Submitting pull requests

---

# ⭐ Support the Project

If AdsAway improves your browsing experience:

⭐ Star the repository

🐛 Report issues

🔀 Submit pull requests

📢 Share the project

---

<p align="center">
  Built for people who want fewer ads, less tracking, and more control over their network.
</p>
