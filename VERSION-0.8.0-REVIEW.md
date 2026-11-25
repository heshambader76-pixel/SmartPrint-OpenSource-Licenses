# SmartPrint Pro 0.8.0 - Third-party source coverage review

Date: 2026-11-25

## Published source archive

The publicly accessible **v0.7.0** archive is available here:

- [Covered sources, supplier notices and provenance materials](https://github.com/heshambader76-pixel/SmartPrint-OpenSource-Licenses/releases/tag/v0.7.0)

The proprietary SmartPrint app repository and its standalone Android Studio ZIP must remain private.

## Verified source changes between v0.7.0 and v0.8.0

Compared private app commits:
- 0.7.0: `2856ab279fb8f804ef908b2541bf1828ce8ce34d`
- 0.8.0 Remove Ads tested fix: `21b023eb73f7fd34221ba6b28ef6adf869b7af04`

GitHub's comparison shows unchanged third-party Android dependency versions in `SmartPrintPro/app/build.gradle.kts`, and no tracked native engine or font binary file changes. The application code and UI/build settings **did** change. This comparison is useful evidence but is not a substitute for a complete inventory of the actual final APK/AAB.

## Items needed before marking 0.8.0 licensing complete

- Compare exact font, native shared-library and third-party dependency inventories and hashes from the final 0.8.0 APK/AAB against the public source package and original supplier notices.
- Document authoritative license terms and correspondence for OpenSymbol 102.12. No unsupported font license grant should be asserted.
- Trace exact native binary build inputs and component versions, including sqlite3, NSS, NSPR and LibreOffice patches/recipes, and reconcile any missing corresponding sources.
- Confirm original SmartPrint icon/logo distribution rights separately; proprietary app assets are not automatically public covered source.
- Confirm that a final appropriate source and notices package is publicly available and that links from the app accurately identify it. A v0.8.0 final license Release is **not yet published**.
- Keep the private app source, billing verifier, credentials and signing assets out of this repository.

**Status: review in progress, not a statement of completed license compliance or readiness for commercial distribution.**

Official licensing information:
- [LibreOffice licensing](https://www.libreoffice.org/about-us/licenses/)
- [Mozilla Public License 2.0 FAQ](https://www.mozilla.org/en-US/MPL/2.0/FAQ/)
