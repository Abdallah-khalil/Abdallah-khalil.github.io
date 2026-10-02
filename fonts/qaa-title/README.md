# Qaa Title (typeface JSON)

The extruded 3D hero title of the cinematic tour's intro (`apps/web/src/app/tour/tour-intro-scene.tsx`,
drei `<Text3D>`), which reads the three.js "typeface" JSON format rather than a font file. Latin only:
typeface outlines are not shaped, so Arabic stays in SDF text (`OceanText`), which troika shapes.

- Derived from `IBMPlexSansArabic-SemiBold.ttf` in `../ibm-plex-sans-arabic/` (IBM Plex Sans Arabic
  1.1.0, its Latin glyphs).
- Modified: subset to printable ASCII (U+0020–U+007E, 95 glyphs) and converted to typeface JSON
  (outlines and advance widths only, no hinting or kerning). Because the result is a modified
  version, it is renamed: "Plex" is a Reserved Font Name under the licence, so this file is
  called **Qaa Title** and does not use that name.
- Converter: `.ptah/specs/cinematic-tour/tools/ttf-to-typeface.mjs` (no dependencies):
  `node ttf-to-typeface.mjs IBMPlexSansArabic-SemiBold.ttf qaa-title.typeface.json "Qaa Title"`.
- Licence: SIL Open Font License 1.1, in `LICENSE.txt` next to the file (copyright IBM Corp.).
