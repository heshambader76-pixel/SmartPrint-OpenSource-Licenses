# SmartPrint Pro 0.8.0: requests for upstream verification

Prepared 26 November 2026. **These requests have not been sent.** They are precise, evidence-backed questions for the relevant maintainers; they do not imply that TDF, F-Droid, SQLite, or legal counsel has approved SmartPrint.

## 1. F-Droid / LibreOffice Android build 131, ARM64

**Suggested subject:** Build provenance request for LibreOffice Viewer 26.2.6.3 (F-Droid versionCode 131), static linkage and SQLite 3.53.0

Dear F-Droid / LibreOffice Android maintainers,

We are redistributing unmodified ARM64 native libraries from the signed F-Droid LibreOffice Viewer 26.2.6.3 build 131 inside SmartPrint Pro 0.8.0. SHA-256 comparisons verify that all fourteen ARM64 shared libraries match the signed F-Droid APK byte-for-byte; our covered-source package also contains the build 131 source archive and the current LibreOfficeKit Java/XML modifications.

We are trying to document an accurate source-to-binary and license record before commercial redistribution. Could you please point us to:
1. The complete build log/configuration and linker response/map (or object/archive lists) showing exactly which static third-party libraries and versions were linked into `liblo-native-code.so`, including patch sets and nondefault configure flags?
2. The effective build recipe, toolchain flags, upstream source and patch list for the shipped shared **SQLite 3.53.0** library? We verified that the binary's `sqlite3_sourceid` matches the upstream 3.53.0 `manifest.uuid`, while LibreOffice's `download.lst` refers to **sqlite-amalgamation-3530400.zip (3.53.4)**. Please clarify whether this shared SQLite came from a separate recipe/input, or whether 3.53.4 was not used for that shared library.
3. If the full map/log cannot be provided, is there a canonical public reproducible build environment and artifact that contains these inputs? Please identify the precise build/commit rather than a moving branch.

The technical evidence and unresolved items are listed publicly at:
https://github.com/heshambader76-pixel/SmartPrint-OpenSource-Licenses/blob/main/AUDIT-0.8.0.he.md

Our goal is to preserve correct applicable source and attribution notices, not request a commercial license exemption. Thank you.

**Potential channels:** https://gitlab.com/fdroid/fdroiddata/-/issues and https://bugs.documentfoundation.org/ . Confirm the right destination with the maintainer before publishing any nonpublic detail.

## 2. The Document Foundation / OpenSymbol maintainers

**Suggested subject:** License/attribution confirmation for OpenSymbol 102.12 TTF from LibreOffice 26.2.6.3

Dear The Document Foundation / OpenSymbol maintainers,

We redistribute the **OpenSymbol 102.12** TrueType font extracted unchanged from the F-Droid LibreOffice Viewer 26.2.6.3 build 131. The font is identical to the F-Droid binary and its upstream referenced downloaded TTF SHA-256 is `f543e6e2d7275557a839a164941c0a86e5f2c3f2a0042bfc434c88c6dde9e140`. We ship the matching `extras/source/truetype/symbol/OpenSymbol.sfd` from LibreOffice commit `8221e31b3ac356a1623c672912a3d2b492f7e3d1`, as well as the upstream README and current licensing notices.

Debian's per-file copyright metadata identifies `OpenSymbol.sfd` with **MPL-2.0 and Apache-2.0** conditions, but the SFD also records glyph contributions attributed to **Takeshi Abe** and **Ming Hua**, and parts from Google, and the actual TTF lacks explicit license fields. We would appreciate written confirmation of:
1. Which license(s) govern redistribution of this exact OpenSymbol 102.12 **TTF binary** in an independent proprietary/commercial Android app, including all contributed glyph outlines?
2. Whether any attributed glyph contributions require separate consent, NOTICE, attribution, trademark, or source availability terms beyond the LibreOffice MPL-2.0 + Apache-2.0 notices and matching SFD?
3. Whether the shipped upstream OpenSymbol README, full SFD and LibreOffice copyright/license notices suffice, and if not, which exact attribution or license text should be added?

Audit and evidence: https://github.com/heshambader76-pixel/SmartPrint-OpenSource-Licenses/blob/main/AUDIT-0.8.0.he.md

We are not asking for legal advice; we are seeking the upstream provenance and applicable permission/notice materials so an independent open-source licensing counsel can review them.

**Potential channels:** https://bugs.documentfoundation.org/ and https://www.libreoffice.org/about-us/ .

## Important limits and next steps

- Technical audit: The 14 native libraries, 34 fonts, 95 Android resolved dependencies, runtime supplier notices and public covered-source archive have been compared to the detailed extent in `AUDIT-0.8.0.he.md`. That evidence must not be described as a complete static linkage bill of materials.
- OpenSymbol's inclusion in an open-source application, and Debian's source-file license record, support the provenance but are **not themselves a final owner-specific legal opinion** on commercial redistribution of every glyph.
- No messages have been sent to maintainers from this repository update.
- Do not modify the 0.8.0 APK or the private app's source to close these documentation gaps.
