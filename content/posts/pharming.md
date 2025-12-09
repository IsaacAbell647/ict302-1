+++
title = "Pharming: The Silent Redirect Attack"
date = "2025-12-08"
draft = false
description = "Understanding pharming attacks and how to protect yourself from malicious website redirects"
tags = ["pharming", "dns-attacks", "cyber-security"]
authors = ["Isaac","Connor","Josh","Ben"]
+++

## What is Pharming?

Pharming redirects you from legitimate websites to fake ones automatically, even when you type the correct URL. Unlike phishing (which tricks you into clicking), pharming manipulates DNS (Domain Name System) to send you to fake sites without your knowledge.

**The Danger:** You can do everything right, type the URL correctly, use bookmarks, check for HTTPS, and still end up on a fake site.

## How It Works

**Normal:** You type `bankofamerica.com` → DNS translates to correct IP → You reach real website

**Pharming Attack:** You type `bankofamerica.com` → Poisoned DNS gives fake IP → You reach scammer's identical fake site → They steal your credentials

### Two Types:

**1. Local Pharming** - Malware on YOUR computer changes DNS settings or hosts file
- Infected from: malicious downloads, email attachments, untrusted browser extensions

**2. Server-Side Pharming** - Hackers compromise DNS servers
- Affects thousands of users at once
- Harder to detect individually

## Warning Signs

**Look for:**
- ✓ Browser security warnings about certificates
- ✓ Website looks slightly different than usual
- ✓ Features don't work properly
- ✓ Slower loading times
- ✓ Password that usually works suddenly doesn't
- ✓ Extra verification steps you've never seen
- ✓ URL has extra characters or misspellings

## Protection Strategies

### 1. Use Trusted DNS Servers
Switch from your ISP's default to:
- **Google:** 8.8.8.8 and 8.8.4.4
- **Cloudflare:** 1.1.1.1 and 1.0.0.1
- **OpenDNS:** 208.67.222.222 and 208.67.220.220

**How to change (Windows):** Control Panel → Network → Change Adapter Settings → Properties → IPv4 → Use the following DNS

**How to change (Mac):** System Preferences → Network → Advanced → DNS

### 2. Keep Everything Updated
- Operating system
- Web browsers
- Antivirus software
- Router firmware

### 3. Security Essentials
- ✓ Install antivirus with real-time protection
- ✓ Enable firewall
- ✓ Use browser security features (Safe Browsing, SmartScreen)
- ✓ Enable two-factor authentication everywhere

### 4. Secure Your Router
- ☐ Change default admin password
- ☐ Update firmware regularly
- ☐ Use WPA3 or WPA2 encryption
- ☐ Disable WPS and remote management

### 5. Safe Browsing Habits
- ✓ Bookmark important sites (banking, shopping)
- ✓ Check for HTTPS padlock
- ✓ Click padlock to verify certificate
- ✓ Use official apps for banking
- ✓ Be cautious with downloads

## What To Do If Pharmed

**Immediate Actions:**

1. **Stop** - Close browser, don't enter more information
2. **Clear DNS Cache:**
   - **Windows:** Open Command Prompt → Type `ipconfig /flushdns`
   - **Mac:** Open Terminal → Type `sudo dscacheutil -flushcache; sudo killall -HUP mDNSResponder`
3. **Scan for malware** - Run full antivirus scan
4. **Check hosts file** for suspicious entries:
   - **Windows:** `C:\Windows\System32\drivers\etc\hosts`
   - **Mac/Linux:** `/etc/hosts`
5. **Change passwords** from a different, clean device
6. **Contact your bank** if you entered financial information
7. **Monitor accounts** for unauthorized activity

### Security Checklist

**Before Entering Sensitive Info:**
- ☐ Is the URL correct?
- ☐ Is there an HTTPS padlock (ex: https://websitename)?
- ☐ Does the certificate match the company?
- ☐ Does the site look and feel normal? Are some features taking too long to load?
- ☐ Are all features working properly?

**If anything seems off, stop and verify through another channel (call the company, use their official app).**


## Remember

> **Just because you typed the right URL doesn't mean you're on the right site.**

**Key Takeaways:**
1. Pharming is invisible. You won't know you're being redirected
2. Use reputable DNS servers
3. Keep software and router updated
4. Enable 2FA as backup protection
5. Trust your instincts. If something feels off, verify through another method

**The Golden Rule:** If a website asks you to re-enter saved information or something feels different, stop and contact the company directly before proceeding.