![GSoC Logo](https://summerofcode.withgoogle.com/assets/media/logo.svg)

# Google Summer of Code 2026 [Final Report]

## Project Information

| Field | Details |
|---|---|
| **GitHub** | [bhavjsh](https://github.com/bhavjsh) |
| **Organization** | [FOSSASIA](https://github.com/fossasia) |
| **Project Title** | Enhancement and Feature Development of FOSSASIA Flutter Apps for PSLab and Smart Badges |
| **Repositories** | [pslab-app](https://github.com/fossasia/pslab-app), [badgemagic-app](https://github.com/fossasia/badgemagic-app), [magic-epaper-app](https://github.com/fossasia/magic-epaper-app) |
| **Mentors** | [Mario Behling](https://github.com/mariobehling), [Marc Nause](https://github.com/marcna​use), [Vishveshwara Uthayakumaran](https://github.com/Vishveshwara), [Dhruv Rastogi](https://github.com/Dhruv1797) |

---

## 1. Project Overview

The GSoC 2026 journey began by working across FOSSASIA's Flutter applications, including **PSLab, Badge Magic, and Magic ePaper**. This helped build a solid understanding of the different codebases, project structures, development workflows, and tooling used across the organization.

The focus then moved into FOSSASIA's **smart badge ecosystem**, particularly the **Badge Magic app** (LED badge design and transfer tool) and the **Magic ePaper app** (NFC e-paper card and tag designer), where the majority of GSoC deliverables were developed and shipped throughout the coding period.

---

## 2. Timeline

| Phase | Period | Focus |
|---|---|---|
| **Community Bonding** | May 1 – May 25, 2026 | PSLab, Badge Magic, Magic ePaper |
| **Before Midterm** | May 26 – July 31, 2026 | Badge Magic, Magic ePaper |
| **After Midterm** | August 1 – October 4, 2026 | Badge Magic, Magic ePaper |

---

# 3. Community Bonding Period

During the community bonding period, I initially worked across all three FOSSASIA Flutter repositories: **PSLab, Badge Magic, and Magic ePaper**. This helped me become familiar with the different codebases, development workflows, project structures and the overall FOSSASIA ecosystem before moving into the main coding period.

## 3.1 Initial Work Across the Repositories

The initial contributions included work across the three applications, with a primary focus on understanding the existing codebases and addressing initial issues and improvements.

### Key Contributions

- Added desktop mouse-wheel and keyboard support and recording playback controls across the PSLab Oscilloscope, Logic Analyzer, Multimeter, and Power Source instrument screens.
- Fixed responsiveness of the PSLab Accelerometer, Gyroscope, and other instrument screens across different desktop window sizes.
- Added Hindi language support and a `-v` / `--version` CLI flag to print the PSLab app version.
- Fixed the macOS CI build by pinning the Xcode version and deduplicated save-filename dialog logic across instrument screens.
- Worked on initial improvements and fixes in the Badge Magic and Magic ePaper codebases while becoming familiar with their architecture and workflows.
- Implemented several smaller fixes, including preventing overwrite during app branch upload and adding arrow-key/Enter navigation for PSLab oscilloscope playback.

This period provided a foundation for working across the three applications and prepared the codebases for the larger feature development carried out during the coding period.

### Contributions

**30 merged pull requests**

[View all merged PRs](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

---

# 4. Coding Period: Before Midterm

After the community bonding period, the focus shifted to FOSSASIA's smart badge applications.

## 4.1 Badge Magic App

### Key Contributions

- Fixed several clipart picker and preview issues, including preserving transparency, fixing inconsistent spacing, and prioritizing recently added cliparts in the picker.
- Added validation with a 200-character limit and persistence fixes for the save-badge dialog, speed dialer, and preview text across navigation.
- Fixed the default font for narrow characters and prevented saving empty cliparts.
- Added `AGENTS.md` contributor documentation and launcher icons for all platforms.
- Implemented various smaller UX fixes, including the erase toolbar icon and redirect-after-save bug.

### Contributions

**33 merged pull requests in total, including 20 during this phase**

[View all merged PRs](https://github.com/fossasia/badgemagic-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

---

## 4.2 Magic ePaper App

### Key Contributions

- Added multiple card templates, including Event Badge, Entry Pass Tag, and more, and built out the card-template editing and preview flow.
- Added barcode upload support and improved the scanner UI.
- Implemented a full set of dithering methods — **Bayer ordered**, **Sierra-2 (two-row)**, and **Burkes** — with gamma-corrected grayscale conversion for accurate e-paper rendering.
- Added support for the **Waveshare 2.13" (G) 4-color NFC** e-paper display.
- Built an in-house lightweight canvas editor for the Open Editor flow, keeping canvas designs editable via the image library.
- Added Hindi localization, graceful error handling for the image library, an open-source licenses screen, and various responsiveness and UI fixes, including a compact two-column mobile layout, AppBar improvements, and desktop icon/window title improvements.
- Set up contributor documentation through `AGENTS.md`, issue and pull request templates, and CI fixes for artifact uploads.

### Contributions

**65 merged pull requests in total, including 38 during this phase**

[View all merged PRs](https://github.com/fossasia/magic-epaper-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

---

# 5. Coding Period: After Midterm

## 5.1 Badge Magic App

### Key Contributions

- Added **USB HID transfer** support, including USB support for Windows, for sending badges directly from desktop.
- Merged the animated GIF gallery into the Home/Animation tab and added mouse-scroll support for the speed dial on desktop.
- Performed a major **codebase refactor**, including consolidating logging onto one shared logger, splitting `FileHelper` and large screens into focused classes, centralizing UI colors into `theme/colors.dart`, reorganizing folders, and normalizing file names to `snake_case`.
- Added badge sharing and import via QR code and an open-source licenses screen.
- Fixed the Linux build and made the home screen layout responsive on desktop.
- Implemented various UI fixes, including clipart sizing and grouping, saved-badges preview and layout improvements, and inconsistent naming cleanup.

### Contributions

**33 merged pull requests in total, including 13 during this phase**

[View all merged PRs](https://github.com/fossasia/badgemagic-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

---

## 5.2 Magic ePaper App

### Key Contributions

- Added additional card templates, including QR Tag, Weather Snapshot, Contact Business, Calendar, and Restaurant Menu, along with **bulk CSV data import for card templates** to support large events.
- Implemented an **OCR scan** feature and a **sketch filter**.
- Improved the overall **NFC experience** and added a dedicated **NFC command console**.
- Added a **sticker vault** to the native canvas editor.
- **Optimized the Rust dithering pipeline** for improved performance.
- Added support for the **Waveshare 1.54" NFC** display.
- Added support for the **Waveshare 2.13" e-Paper (G) 4-color NFC display** as an additional display option, currently under untested/beta status.
- Added support for the **Santek EZ Sign 2.13" NFC e-paper display**, an external 4-color display.
- Performed a large codebase refactor by reorganizing and renaming files to follow plural and `snake_case` conventions, moving screens and widgets out of utility folders, and removing duplicate and redundant code.
- Restructured the README and upgraded Flutter, Gradle, and iOS deployment targets.

### Contributions

**65 merged pull requests in total, including 27 during this phase**

[View all merged PRs](https://github.com/fossasia/magic-epaper-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

---

# 6. Screenshots and Demonstrations

## 6.1 Badge Magic

### Ss

---

## 6.2 Magic ePaper

### Ss

---

# 7. Challenges and Learnings

- Working across different repositories and adapting to different codebases, architectures, and project structures.
- Implementing dithering algorithms, including Bayer, Sierra-2, and Burkes, along with a Rust dithering pipeline for accurate and performant e-paper rendering.
- Building responsive layouts that work well across both mobile and desktop, including mouse and keyboard support.
- Handling NFC and USB HID communication with real hardware displays.
- Supporting multiple e-paper display models, including Waveshare and Santek EZ Sign, with differing capabilities and protocols.

---

# 8. Future Work

Continuing contributions to FOSSASIA's PSLab, Badge Magic, and Magic ePaper applications beyond GSoC.

---

# 9. Acknowledgements

A huge thanks to my mentors for their guidance and support throughout GSoC 2026, and to the **FOSSASIA** community and **Google Summer of Code** for this opportunity.
