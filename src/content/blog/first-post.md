---
title: "SSRF in PDF Generators"
pubDate: 2019-01-02
description: "Add it "
heroImage: "/blog-placeholder-about.jpg"
---

## Introduction

ADD it and change the blog

---

## FILE FOUND — 50

We received a `.class` Java file. I ran the `strings` command on it and found a message encrypted with Caesar cipher. Decoding it revealed the flag.

**Flag:** `FLAG{FORENSICS_101}`

---

## Help Ann — 100

We were given a corrupted PNG. I opened it in a hex editor and saw that the header bytes were missing. I copied a correct PNG header into it and saved the file. Opening it showed a QR code.

**Flag:** `Flag{Aw3s0m3-Y0u-G0t-th1s}`

---

## Just Smile — 100

After examining the image file, I noticed extra data appended after the `IEND` chunk. Using `binwalk`, I extracted it to find an ELF binary. It required a password, which I found in its own strings.

**Flag:** `FLAG{APPENEDING_FILES_REALLY!!}`

---

## Light — 50

Binary content at the bottom of the file was actually ASCII binary. I used a binary-to-text converter to decode it.

**Flag:** `Flag{So-L!gHt}`

---

## Wanna some Biscuits — 50

This was a web challenge where the cookie had a base64-encoded PHP serialized object. I modified `isAdmin` from `false` to `true`, re-encoded and re-serialized it.

**Flag:** `FLAG{REALLY!!_IN_COOKIES}`

---

## request Gate — 50

The challenge expected GET/POST requests only. I tried PUT with `/index.php` which wasn’t blocked, and it returned the flag.

**Flag:** `M3th0ds!sN0t0nlyG3T0rP0ST`

---

## Yellow Duck — 100

The base64 string contained an image file that was XOR encrypted. I used `xortool` to determine the key and decode the flag.

**Flag:** `flag{Y0u_CatchIt_0100110120100}`

---

## Final Thoughts

The challenges weren’t extremely difficult but required some digging and tool usage. It was a great learning experience and a fun format.
