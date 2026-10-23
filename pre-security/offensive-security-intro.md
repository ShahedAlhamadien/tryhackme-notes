# Offensive Security Intro

**Path:** Pre Security
**Section:** Introduction to Cyber Security
**Date:** [10/23/2026]

## OverView
Offensive Security means thinking like an attacker to find weaknesses in a system before a real attacker does.

## Key Terms
**Hidden page** = a page that exists on a site but has no visible link to it.
**DirBoster** = a tool that tries common page names (from a wordlist) to discover hidden pages.

## Attack Steps
1. Opened the lab (virtual machine) and explored the "Fake Bank" website, then found my account page.
2. Opened the Terminal and ran DirBuster against 'fackebank.thm' to discover hidden pages.
3. Found two hidden pages: '/bank-transfer' and '/images' .
4. Manually visited 'http//fakebank.thm/bank-transfer' since it had no visible link on the site.
5. Used the form on the page to deposit $2000+ into my account.
6. A green message appeared: **THE BANK HACKED** - this was the answer

## Finally Note
Admin pages must be protected with proper authentication, not just hidden from navigation. "Security through obscurity" is not real security.
