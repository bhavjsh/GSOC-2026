![GSoC Logo](https://summerofcode.withgoogle.com/assets/media/logo.svg)

# Google Summer of Code 2026 [Final Report]

## Project Information

| Field | Details |
|---|---|
| **Contributor** | [Bhavini Joshi](https://github.com/bhavjsh) |
| **Organization** | [FOSSASIA](https://github.com/fossasia) |
| **Project Title** | Enhancement and Feature Development of FOSSASIA Flutter Apps for PSLab and Smart Badges |
| **Repositories** | [PSLab](https://github.com/fossasia/pslab-app) · [Badge Magic](https://github.com/fossasia/badgemagic-app) · [Magic ePaper](https://github.com/fossasia/magic-epaper-app) |
| **Mentors** | [Mario Behling](https://github.com/mariobehling), [Marc Nause](https://github.com/marcnause), [Vishveshwara Uthayakumaran](https://github.com/Vishveshwara), [Dhruv Rastogi](https://github.com/Dhruv1797) |

# 1. Project Overview

My GSoC 2026 work started across three FOSSASIA Flutter applications: **PSLab, Badge Magic, and Magic ePaper**. Working across these repositories helped me understand different codebases, development workflows, and project structures within the organization.

After the initial period, my main focus shifted to FOSSASIA's smart badge ecosystem, particularly **Badge Magic**, an LED badge design and transfer application, and **Magic ePaper**, an NFC e-paper card and tag designer.

Most of my feature development and contributions during GSoC were focused on these two applications.

# 2. Timeline

| Phase | Focus |
|---|---|
| **Community Bonding** | PSLab, Badge Magic, Magic ePaper |
| **Before Midterm** | Badge Magic, Magic ePaper |
| **After Midterm** | Badge Magic, Magic ePaper |

# 3. Community Bonding Period

During community bonding, I initially worked across all three repositories **PSLab, Badge Magic, and Magic ePaper**. The main goal was to get familiar with the applications while working on fixes, improvements, and smaller features.

## 3.1 PSLab

- Added **[desktop mouse-wheel and keyboard support](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+mouse+keyboard)** along with recording playback controls for the Oscilloscope, Logic Analyzer, Multimeter, and Power Source.
- Improved **[responsiveness of instrument screens](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+responsive)** across different desktop window sizes, including the Accelerometer and Gyroscope.
- Added **[Hindi language support](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+Hindi)**.
- Added a **[`-v` / `--version` CLI flag](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+version)** for displaying the application version.
- Fixed the **[macOS CI build](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+Xcode)** by pinning the Xcode version.
- Removed duplicated **[save-filename dialog logic](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+filename)** across instrument screens.
- Added **[arrow-key and Enter navigation](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+oscilloscope+playback)** for oscilloscope playback.
- Fixed **[file overwrite during app branch upload](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh+upload)**.

**30 merged pull requests**

[View all merged PSLab PRs](https://github.com/fossasia/pslab-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

## 3.2 Badge Magic and Magic ePaper

I also worked on initial fixes and improvements in the **Badge Magic** and **Magic ePaper** codebases while getting familiar with their architecture and workflows.

# 4. Coding Period [Before Midterm]

After community bonding, my main focus shifted to the smart badge applications.

## 4.1 Badge Magic

The first phase of work on Badge Magic focused on improving the badge creation workflow, clipart handling, saved badges, and overall usability.

### Key Contributions

- Improved the clipart picker and preview, including **[transparency](https://github.com/fossasia/badgemagic-app/pull/1725)**, **[spacing](https://github.com/fossasia/badgemagic-app/pull/1711)**, and **[ordering of recently added cliparts](https://github.com/fossasia/badgemagic-app/pull/1684)**.
- Added a **[200-character validation limit to the save-badge dialog](https://github.com/fossasia/badgemagic-app/pull/1710)** and fixed persistence issues.
- Fixed **[save-badge dialog persistence](https://github.com/fossasia/badgemagic-app/pull/1710)**.
- Fixed **[speed dialer persistence](https://github.com/fossasia/badgemagic-app/pull/1709)**.
- Fixed **[preview text persistence](https://github.com/fossasia/badgemagic-app/pull/1709)** across navigation.
- Fixed **[default font handling for narrow characters](https://github.com/fossasia/badgemagic-app/pull/1722)**.
- Prevented **[empty cliparts from being saved](https://github.com/fossasia/badgemagic-app/pull/1704)**.
- Added **[`AGENTS.md` contributor documentation](https://github.com/fossasia/badgemagic-app/pull/1698)**.
- Added **[launcher icons](https://github.com/fossasia/badgemagic-app/pull/1676)** for supported platforms.
- Fixed the **[erase toolbar icon](https://github.com/fossasia/badgemagic-app/pull/1685)**.
- Fixed the **[redirect-after-save behaviour](https://github.com/fossasia/badgemagic-app/pull/1680)**.

**33 merged pull requests in total, including 20 during this phase**

[View merged Badge Magic PRs](https://github.com/fossasia/badgemagic-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

## 4.2 Magic ePaper

The first phase of Magic ePaper focused on templates, image processing, e-paper rendering, the editor workflow, and improving the overall application experience.

### Key Contributions

- Added **[card templates](https://github.com/fossasia/magic-epaper-app/pull/426)** including Event Badge and Entry Pass Tag, together with their **[editing and preview flow](https://github.com/fossasia/magic-epaper-app/pull/457)**.
- Added **[barcode upload](https://github.com/fossasia/magic-epaper-app/pull/412)** support and improved the scanner UI.
- Implemented **[Bayer ordered dithering](https://github.com/fossasia/magic-epaper-app/pull/519)**.
- Implemented **[Sierra-2 dithering](https://github.com/fossasia/magic-epaper-app/pull/532)**.
- Implemented **[Burkes dithering](https://github.com/fossasia/magic-epaper-app/pull/533)**.
- Added **[gamma-corrected grayscale conversion](https://github.com/fossasia/magic-epaper-app/pull/529)** for improved e-paper rendering.
- Added support for the **[Waveshare 2.13" (G) 4-color NFC e-paper display](https://github.com/fossasia/magic-epaper-app/pull/527)**.
- Built a **[native canvas editor](https://github.com/fossasia/magic-epaper-app/pull/487)** for the Open Editor flow.
- Added **[Hindi localization](https://github.com/fossasia/magic-epaper-app/pull/439)**.
- Improved **[image-library error handling](https://github.com/fossasia/magic-epaper-app/pull/512)**.
- Added an **[open-source licenses screen](https://github.com/fossasia/magic-epaper-app/pull/484)**.
- Improved **[mobile](https://github.com/fossasia/magic-epaper-app/pull/466)** and **[desktop](https://github.com/fossasia/magic-epaper-app/pull/469)** responsiveness.
- Added **[`AGENTS.md`](https://github.com/fossasia/magic-epaper-app/pull/398)** contributor documentation.
- Added **[issue](https://github.com/fossasia/magic-epaper-app/pull/323)** and **[pull request](https://github.com/fossasia/magic-epaper-app/pull/322)** templates.
- Fixed **[CI artifact upload issues](https://github.com/fossasia/magic-epaper-app/pull/459)**.

**65 merged pull requests in total, including 38 during this phase**

[View merged Magic ePaper PRs](https://github.com/fossasia/magic-epaper-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

# 5. Coding Period [After Midterm]

## 5.1 Badge Magic

The second phase focused more heavily on hardware communication, desktop support, sharing features, and improving the structure of the codebase.

### Key Contributions

- Added **[USB HID transfer support](https://github.com/fossasia/badgemagic-app/pull/1825)**, including **[Windows USB support](https://github.com/fossasia/badgemagic-app/pull/1822)**, allowing badges to be transferred directly from desktop.
- Integrated the **[animated GIF gallery](https://github.com/fossasia/badgemagic-app/pull/1859)** into the **[Home/Animation tab](https://github.com/fossasia/badgemagic-app/pull/1933)**.
- Added **[mouse-scroll support for the speed dial](https://github.com/fossasia/badgemagic-app/pull/1923)** on desktop.
- Added **[shared logging](https://github.com/fossasia/badgemagic-app/pull/1897)** as part of the codebase refactor.
- Split **[`FileHelper`](https://github.com/fossasia/badgemagic-app/pull/1891)** and **[large screens](https://github.com/fossasia/badgemagic-app/pull/1871)** into focused classes.
- Centralized UI colors in **[`theme/color.dart`](https://github.com/fossasia/badgemagic-app/pull/1849)**.
- **[Reorganized folders](https://github.com/fossasia/badgemagic-app/pull/1862)** and **[normalized filenames to `snake_case`](https://github.com/fossasia/badgemagic-app/pull/1858)**.
- Added **[badge sharing and import via QR code](https://github.com/fossasia/badgemagic-app/pull/1779)**.
- Added an **[open-source licenses screen](https://github.com/fossasia/badgemagic-app/pull/1794)**.
- Fixed the **[Linux build](https://github.com/fossasia/badgemagic-app/pull/1820)**.
- Improved the **[desktop home-screen layout](https://github.com/fossasia/badgemagic-app/pull/1821)**.
- Fixed **[clipart sizing and grouping](https://github.com/fossasia/badgemagic-app/pull/1740)** issues.
- Improved **[saved-badge previews and layouts](https://github.com/fossasia/badgemagic-app/pull/1754)**.
- Fixed **[naming issues](https://github.com/fossasia/badgemagic-app/pull/1865)** across the application.

**33 merged pull requests in total, including 13 during this phase**

[View merged Badge Magic PRs](https://github.com/fossasia/badgemagic-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

## 5.2 Magic ePaper

The final phase expanded Magic ePaper with more templates, image-processing features, NFC functionality, and support for additional e-paper hardware. This phase also included substantial codebase cleanup and preparation for beta testing.

### Key Contributions

- Added **[QR Tag](https://github.com/fossasia/magic-epaper-app/pull/559)** card templates.
- Added **[Weather Snapshot](https://github.com/fossasia/magic-epaper-app/pull/557)** card templates.
- Added **[Contact Business](https://github.com/fossasia/magic-epaper-app/pull/551)** card templates.
- Added **[Calendar](https://github.com/fossasia/magic-epaper-app/pull/548)** card templates.
- Added **[Restaurant Menu](https://github.com/fossasia/magic-epaper-app/pull/567)** card templates.
- Added **[bulk CSV data import](https://github.com/fossasia/magic-epaper-app/pull/544)** for card templates.
- Implemented the **[OCR scan](https://github.com/fossasia/magic-epaper-app/pull/666)** feature.
- Implemented the **[sketch filter](https://github.com/fossasia/magic-epaper-app/pull/692)**.
- Improved the overall **[NFC workflow](https://github.com/fossasia/magic-epaper-app/pull/560)**.
- Added a dedicated **[NFC command console](https://github.com/fossasia/magic-epaper-app/pull/616)**.
- Added a **[sticker vault](https://github.com/fossasia/magic-epaper-app/pull/615)** to the native canvas editor.
- Optimized the **[Rust dithering pipeline](https://github.com/fossasia/magic-epaper-app/pull/626)** for better performance.
- Added support for the **[Waveshare 1.54" NFC display](https://github.com/fossasia/magic-epaper-app/pull/638)**.
- Added support for the **[Waveshare 2.13" e-Paper (G) 4-color NFC display](https://github.com/fossasia/magic-epaper-app/pull/527)**.
- Added support for the **[Santek EZ Sign 2.13" NFC e-paper display](https://github.com/fossasia/magic-epaper-app/pull/688)**.
- Reorganized files according to **[plural naming conventions](https://github.com/fossasia/magic-epaper-app/pull/675)**.
- Renamed **[mismatched and duplicate filenames](https://github.com/fossasia/magic-epaper-app/pull/673)**.
- Moved **[screens and widgets out of utility folders](https://github.com/fossasia/magic-epaper-app/pull/674)**.
- Cleaned up **[filenames across the codebase](https://github.com/fossasia/magic-epaper-app/pull/672)**.
- **[Restructured the README](https://github.com/fossasia/magic-epaper-app/pull/625)**.
- Upgraded **[Flutter](https://github.com/fossasia/magic-epaper-app/pull/609)**, **[Gradle](https://github.com/fossasia/magic-epaper-app/pull/587)**, and **[iOS deployment targets](https://github.com/fossasia/magic-epaper-app/pull/587)**.

**65 merged pull requests in total, including 27 during this phase**

[View merged Magic ePaper PRs](https://github.com/fossasia/magic-epaper-app/pulls?q=is%3Apr+is%3Amerged+author%3Abhavjsh)

# 6. Screenshots and Demonstrations

## 6.1 Badge Magic

<table>
<tr>
<td align="center">

**USB HID Transfer**

<img width="360" alt="USB HID Transfer" src="https://github.com/user-attachments/assets/c90fc170-70b9-4666-bc1f-9bf40400208d" />

</td>

<td align="center">

**Badge Import via QR Code**

<img width="360" alt="Badge Import via QR Code" src="https://github.com/user-attachments/assets/59da50d0-da7a-45eb-a538-2a36b1be563d" />

</td>

<td align="center">

**Clipart Picker**

<img width="360" alt="Clipart Picker" src="https://github.com/user-attachments/assets/1fb4079d-efb1-4fd7-aaa0-dc0779dfa20b" />

</td>
</tr>

<tr>
<td align="center">

**USB Settings**

<img width="360" alt="USB Settings" src="https://github.com/user-attachments/assets/b5727880-a48c-4ad6-8d20-ebff2469b0a6" />

</td>

<td align="center">

**Animation Gallery**

<img width="360" alt="Animation Gallery" src="https://github.com/user-attachments/assets/e8ffb906-7aad-40c4-a54f-a3b338bfd574" />

</td>

<td align="center">

**Save Badge Dialog**

<img width="360" alt="Save Badge Dialog" src="https://github.com/user-attachments/assets/86afb717-c25f-44e7-883a-60fc3a49b0fa" />

</td>
</tr>
</table>

## 6.2 Magic ePaper

<table>
<tr>
<td align="center">

**Card Templates**

<img width="360" alt="Card Templates" src="https://github.com/user-attachments/assets/3fd1ac33-64ef-4f25-b104-765bc13c6869" />

</td>

<td align="center">

**Editable Image**

<img width="360" alt="Editable Image" src="https://github.com/user-attachments/assets/633e7736-e4ed-4578-aa67-fc1f01f97538" />

</td>

<td align="center">

**Barcode Upload**

<img width="360" alt="Barcode Upload" src="https://github.com/user-attachments/assets/53dcb245-dd01-4ebc-9465-9eedc5f3e4b5" />

</td>
</tr>

<tr>
<td align="center">

**Dithering Algorithms**

<img width="360" alt="Dithering Algorithms" src="https://github.com/user-attachments/assets/00511f84-413d-4d6e-b3b5-689b8ce06d29" />

</td>

<td align="center">

**Native Canvas Editor**

<img width="360" alt="Native Canvas Editor" src="https://github.com/user-attachments/assets/d37a447e-7412-4cd4-b7a9-30d52dd13406" />

</td>

<td align="center">

**Bulk CSV Import**

<img width="360" alt="Bulk CSV Import" src="https://github.com/user-attachments/assets/56e12fef-301e-474a-8395-b960c30428c0" />

</td>
</tr>

<tr>
<td colspan="3" align="center">

**Santek EZ Sign 2.13" NFC E-Paper Display**

<img width="800" alt="Santek EZ Sign 2.13 inch NFC e-paper display" src="https://github.com/user-attachments/assets/054a73e4-08bd-4b1e-8145-a7077c44c630" />

</td>
</tr>
</table>

# 7. Challenges and Learnings

| Challenge | What I Learned |
|---|---|
| **Working Across Different Repositories** | Worked across different codebases, architectures, project structures, and development workflows, which helped me adapt to different projects. |
| **Image Processing** | Implemented Bayer, Sierra-2, and Burkes dithering and worked with the Rust dithering pipeline, gaining practical experience in image processing and performance optimization for e-paper displays. |
| **Cross-Platform Development** | Worked on both mobile and desktop environments, handling different screen sizes along with mouse and keyboard interactions. |
| **Hardware Communication** | Worked with NFC and USB HID communication to understand how the applications interact with real hardware displays. |
| **Supporting Multiple Displays** | Worked with different e-paper displays, including Waveshare and Santek EZ Sign, each having different capabilities and communication requirements. |

# 8. Future Work

I plan to continue contributing to FOSSASIA's **PSLab, Badge Magic, and Magic ePaper** applications beyond GSoC.

# 9. Acknowledgements

I would like to thank my mentors for their guidance and support throughout GSoC 2026.

I am grateful to the **FOSSASIA** community for providing an open and collaborative environment to work on real-world open-source projects.

Finally, I would like to thank **Google Summer of Code** for giving me the opportunity to contribute to open source and gain hands-on experience working on production applications.
