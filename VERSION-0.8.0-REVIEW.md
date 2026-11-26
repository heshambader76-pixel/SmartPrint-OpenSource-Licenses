# SmartPrint Pro 0.8.0: third-party licensing evidence and remaining checks

Updated: 26 November 2026

## Released public material

- Existing public [v0.7.0 covered-source Release](https://github.com/heshambader76-pixel/SmartPrint-OpenSource-Licenses/releases/tag/v0.7.0).
- [Covered-source ZIP](https://github.com/heshambader76-pixel/SmartPrint-OpenSource-Licenses/releases/download/v0.7.0/SmartPrint-Pro-0.7.0-Covered-Sources.zip), approximately 1.08 GB, is listed as a public GitHub release asset.
- This public repository contains **no proprietary Android Studio app source**, private billing verifier, credentials, or signing keys.

The existing app version 0.8.0 links to the v0.7.0 Release. That URL is not a statement that the actual 0.8.0 native bundle has been fully reconciled with the public v0.7.0 archive.

## Evidence compared for app releases

Private project, reviewed commits:
- Base v0.7.0: `2856ab279fb8f804ef908b2541bf1828ce8ce34d`
- 0.8.0 owner-approved APK: `21b023eb73f7fd34221ba6b28ef6adf869b7af04`

Compared repository trees and the build configuration at both commits:
- **95** Android runtime third-party dependency coordinates are recorded in `third_party/android/runtime-components.json` at both commits. The Git blob SHA is identical: `23efefa55048160170e846286ce5d5db6d645878`. This inventory lists exact coordinates, declared licenses, supplier notices, upstream POM links and artifact SHA-256 values.
- The Gradle dependency declarations in `SmartPrintPro/app/build.gradle.kts` are unchanged in the inspected version comparison, although this build file itself changed for version and test billing configuration.
- GitHub commit comparison shows no changed tracked native engine, font or third-party legal notice files between these commits.
- App functionality, PDF UI, locales, license-link behavior, and build settings did change. Thus this is **evidence of tracked third-party payload continuity**, not a proof of identical complete APK/AAB content or perfect build-to-source correspondence.

## OpenSymbol: specific upstream evidence

The 0.8.0 private project preserves `OpenSymbol-README.txt`, which describes regenerating the font from `extras/source/truetype/symbol/OpenSymbol.sfd` with FontForge. The version 102.12 font and its preferred SFD source are described in the existing covered-source package notice.

Independent package sources also identify OpenSymbol as a component of LibreOffice:
- [Debian fonts-opensymbol 102.12 package](https://packages.debian.org/stable/fonts/fonts-opensymbol)
- [Debian LibreOffice copyright metadata, including OpenSymbol.sfd](https://sources.debian.org/copyright/license/libreoffice/4%3A25.2.3-2%2Bdeb13u6/)
- [LibreOffice upstream tagged font directory](https://github.com/LibreOffice/core/tree/libreoffice-26.2.6.3/extras/source/truetype/symbol)
- [LibreOffice licensing overview](https://www.libreoffice.org/licenses/)

**Unresolved:** those references identify origins, copyright and licensing context, but have not been used to establish conclusively the license scope of the exact redistributed 102.12 font binary, including all third-party glyph contributions. No blanket OFL-1.1 license is claimed for OpenSymbol.

## Other matching-source and attribution items

- The project notice identifies the LibreOffice/LibreOfficeKit **26.2.6.3** upstream tag, F-Droid matching source archive, and project-covered Java/XML modifications. Further per-component mapping is needed to establish actual downstream binaries and their precise patches/build inputs.
- The existing native notice identifies NSS **3.128**, NSPR **4.39**, SQLite **3.53.0**, and NDK r29 / LLVM 21 for libc++. Check build input provenance and notices for each final binary, including embedded/static components.
- The font notice distinguishes legacy **Liberation Sans Narrow** (GPL-2.0 plus font agreement/exception) from modern **Liberation 2.1.5** (OFL-1.1); they are not interchangeable licenses.
- Project owner must affirm rights in original app logo and vector artwork separately. These proprietary graphics are not automatically subject to covered-source publication.
- Google Mobile Ads, Play Services, UMP and Billing SDK terms and app-store policies are separate from open-source copyright notices.

## Gate to claim complete licensing review

Before representing v0.8.0 as fully audited, independently inspect the final distributed APK/AAB and public 1.08 GB archive at a binary/file-manifest level, record the exact matching source files and build recipes, and close the font and graphic-rights questions.

**Current status: public materials available; third-party dependency list and tracked payload continuity verified; final binary-to-source and select rights checks NOT completed. Do not label this a final legal sign-off.**

Contact: [support@costrichapp.com](mailto:support@costrichapp.com).
