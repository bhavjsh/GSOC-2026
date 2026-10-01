![GSoC Logo](https://summerofcode.withgoogle.com/assets/media/logo.svg)

# Google Summer of Code 2026 [Final Report]

## Project Information

- **GitHub:** [bhavjsh](https://github.com/bhavjsh)
- **Organization:** [FOSSASIA](https://github.com/fossasia)
- **Project Title:** Enhancement and Feature Development of FOSSASIA Flutter Apps for PSLab and Smart Badges
- **Repositories:** [pslab-app](https://github.com/fossasia/pslab-app), [badgemagic-app](https://github.com/fossasia/badgemagic-app), [magic-epaper-app](https://github.com/fossasia/magic-epaper-app)
- **Mentors:** [Mario Behling](https://github.com/mariobehling), [Marc Nause](https://github.com/marcnause), [Vishveshwara Uthayakumaran](https://github.com/Vishveshwara), [Dhruv Rastogi](https://github.com/Dhruv1797)

---

## Project Overview

The GSoC 2026 journey began by working across FOSSASIA's Flutter apps, including **PSLab**, which helped build a solid understanding of the codebases, review process, and tooling used across the organization. From there, the focus moved into FOSSASIA's **smart badge ecosystem**, the **Badge Magic app** (LED badge design/transfer tool) and the **Magic ePaper app** (NFC e-paper card/tag designer), where the majority of GSoC deliverables were built and shipped across the coding period.

---

## Timeline


- Community Bonding [May 1 – May 25, 2026]: PSLab app
- Before Midterm [May 26 – Jul 31, 2026]: Badge Magic + Magic ePaper 
- After Midterm [Aug 1 – Oct 4, 2026]: Badge Magic + Magic ePaper 

---

## Community Bonding Period (May 1 – May 25, 2026)

### PSLab App

Community bonding was spent getting familiar with FOSSASIA's apps and workflow by contributing to the **PSLab Flutter app**:

- Added desktop mouse-wheel/keyboard support and recording playback controls across the Oscilloscope, Logic Analyzer, Multimeter, and Power Source instrument screens
- Fixed responsiveness of the Accelerometer, Gyroscope, and other instrument screens across desktop window sizes
- Added Hindi language support and a `-v`/`--version` CLI flag to print the app version
- Fixed the macOS CI build (pinned Xcode version) and deduplicated save-filename dialog logic across instrument screens
- Several smaller fixes: prevented overwrite during app branch upload, added arrow-key/Enter navigation for oscilloscope playback, and more

This gave solid hands-on experience with the codebase and contribution process ahead of the coding period.

🔗 **All merged PRs (30):** https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh

---

## Before Midterm (May 26 – Jul 31, 2026)

After community bonding, focus shifted to FOSSASIA's smart badge apps.

### Badge Magic App

- Fixed several clipart picker/preview issues: preserved transparency, fixed inconsistent spacing and prioritized recently-added cliparts in the picker
- Added validation (200-character limit) and persistence fixes for the save-badge dialog, speed dialer and preview text across navigation
- Fixed the default font for narrow characters and prevented saving empty cliparts
- Added `AGENTS.md` contributor documentation and launcher icons for all platforms
- Various smaller UX fixes: erase toolbar icon, redirect-after-save bug, etc.

🔗 **All merged PRs (33 total, 20 in this phase):** https://github.com/fossasia/badgemagic-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh

### Magic ePaper App

- Added multiple card templates (Event Badge, Entry Pass Tag, and more) and built out the card-template editing/preview flow
- Added barcode upload support and improved the scanner UI
- Implemented a full set of dithering methods — **Bayer ordered**, **Sierra-2 (two-row)**, and **Burkes** — with gamma-corrected grayscale conversion for accurate e-paper rendering
- Added support for the **Waveshare 2.13" (G) 4-color NFC** e-paper display
- Built an in-house lightweight canvas editor for the Open Editor flow, keeping canvas designs editable via the image library
- Added Hindi localization, graceful error handling for the image library, an open-source licenses screen, and various responsiveness/UI fixes (compact two-column mobile layout, AppBar, desktop icon/window title)
- Set up contributor docs (`AGENTS.md`), issue/PR templates, and CI fixes for artifact uploads

🔗 **All merged PRs (65 total, 38 in this phase):** https://github.com/fossasia/magic-epaper-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh

---

## After Midterm (Aug 1 – Oct 4, 2026)

### Badge Magic App

- Added **USB HID transfer** support (including USB support for Windows) for sending badges directly from desktop
- Merged the animated GIF gallery into the Home/Animation tab and added mouse-scroll support for the speed dial on desktop
- Major **codebase refactor**: consolidated logging onto one shared logger, split `FileHelper` and large screens into focused classes, centralized UI colors into `theme/colors.dart`, reorganized folders, and normalized file names to snake_case
- Added badge sharing/import via QR code and an open-source licenses screen
- Fixed the Linux build and made the home screen layout responsive on desktop
- Various UI fixes like clipart sizing/grouping, saved-badges preview/layout, inconsistent naming cleanup

🔗 **All merged PRs (33 total, 13 in this phase):** https://github.com/fossasia/badgemagic-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh

### Magic ePaper App

- Added many more card templates like QR tag, weather snapshot, contact business, calendar, restaurant menu, plus **bulk CSV data import for card templates**, built to support large events
- Implemented an **OCR scan** feature and a **sketch filter**
- Improved the overall **NFC experience** and added a dedicated **NFC command console**
- Added a **sticker vault** to the native canvas editor
- **Optimized the Rust dithering pipeline** for performance
- Added **Waveshare 1.54" NFC** display support, **Waveshare 2.13inch e-Paper (G) 4-color NFC display** (an additional display option, currently under untested/beta status) 
- Added **Santek EZ Sign 2.13" NFC e-paper display**, an external 4 colored display 
- Large codebase refactor: reorganizedand renamed files to plural/snake_case convention, moved screens and widgets out of util folders, removed duplicate/redundant code
- Restructured the README and upgraded Flutter/Gradle/iOS deployment targets

🔗 **All merged PRs (65 total, 27 in this phase):** https://github.com/fossasia/magic-epaper-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh

---

## Screenshots

PSLab 

Badge Magic

Magic ePaper 


---

## Challenges & Learnings

- Working across three Flutter codebases with different conventions, each with their own mentors and review process
- Implementing dithering algorithms (Bayer, Sierra-2, Burkes) and a Rust dithering pipeline for accurate, performant e-paper rendering
- Building responsive layouts that work well across both mobile and desktop (mouse/keyboard support)
- Handling NFC and USB HID communication with real hardware displays
- Supporting multiple e-paper display models (Waveshare, Santek EZ Sign) with differing capabilities and protocols

## Future Work

Continuing contributions to FOSSASIA's PSLab, Badge Magic, and Magic ePaper apps beyond GSoC.

## Acknowledgements

A huge thanks to my mentors for their guidance and support throughout GSoC 2026 and to the **FOSSASIA** community and **Google Summer of Code** for this opportunity.
