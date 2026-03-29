# Quran Hafs EPUB

A complete open-source digital Mushaf in the Hafs an Asim recitation, built in EPUB 3.3 format for a comfortable and beautiful reading experience across all modern devices.

This project is a *Sadaqa Jariya* (ongoing charity).

---

## Why EPUB?

Most digital Mushafs are distributed as PDFs — and most of those are scanned images of printed pages, not actual text. This means the entire page is just a picture: you cannot search it, select text from it, or have it read aloud, unless a successful OCR is applied. Also, zooming-in degrades the image quality, producing blurry and pixelated Arabic letters. And to read comfortably on a phone you typically need 200-300% zoom, which forces constant horizontal scrolling just to read a single line.

High quality text-based PDF Mushafs exist, but they come with their own tradeoffs. A well-typeset PDF Mushaf with embedded fonts can easily reach 50-300MB in size — compared to under 2MB for this EPUB — while still locking the layout to a fixed page size designed for print.

EPUB is fundamentally different. The text reflows naturally to any screen size and any font size the reader chooses, with no horizontal scrolling and no layout breaking. Arabic letters are rendered as live vector glyphs — sharp and beautiful at any zoom level on any device. The file stays small because it contains text, not images.

EPUB 3.3 also has native accessibility support. Screen readers — software used by visually impaired people that reads content aloud, such as VoiceOver on Apple devices or TalkBack on Android — can fully interpret an EPUB document. This makes the Quran accessible to blind or visually impaired Muslims who cannot read a printed or image-based Mushaf. A scanned PDF offers them nothing.

Dedicated Quran apps are for sure excellent tools, but they depend on a company or developer maintaining them. Apps get discontinued, removed from stores, or stop receiving updates. An EPUB file is a self-contained, open standard document — it works on any EPUB reader app, of which there are many free and high quality options available on all platforms. It does not need an internet connection, does not collect your data, and will remain readable on any EPUB-compatible reader for the foreseeable future. You own the file. No account, no subscription, no tracking.

---

## Features

- Complete Quranic text in the Hafs an Asim recitation
- Typeset in the KFGQPC Uthmanic Hafs V22 font
- Full Hizb, Rub (1/4 hizb), Nisf (1/2 hizb), Thalatharbaa (3/4 hizb) and Thumun (1/8) division markers inline with the text
- Complete Waqf (pause) and Ibtida (resumption) marks
- Surah index and clickable Hizb index for quick navigation
- Decorative dividers between Surahs
- Compatible with day, night, and sepia reading modes
- EPUB 3.3 with full accessibility support (ARIA labels, epub:type semantics)

---

## Download

Download the latest release from the releases page:

👉 **[Latest Release](../../releases/latest)**

---

## Recommended Reading Apps

| App | Platform |
|---|---|
| [Readest](https://readest.com) | Android / iOS / Desktop |
| [Cantook by Aldiko](https://www.demarque.com/en) | Android / iOS |
| [Calibre](https://calibre-ebook.com) | Desktop |

---

## How to Build

### Requirements

- Python 3.8+
- Data files in `_dev/docs/`:
  - `quran-uthmani.txt` — Quranic text from Tanzil.net
  - `quran-data.xml` — Division metadata (Surahs, Hizbs, Thumuns), also from Tanzil.net

### Steps
```bash
cd _dev/tools

# Generate XHTML files
python generate_quran_xhtml.py

# Package the EPUB
python package_epub.py
```

Output is saved to `_dev/output/quran-hafs.epub`.

---

## Sources & Credits

| Source | Link |
|---|---|
| Quranic text | [tanzil.net](https://tanzil.net) |
| Mushaf font — KFGQPC Uthmanic Hafs V22 | [fonts.qurancomplex.gov.sa/ten-readings](https://fonts.qurancomplex.gov.sa/ten-readings) |
| Auxiliary font — Amiri by Dr. Khaled Hosny | [amirifont.org](https://amirifont.org) |

---

## License

- **Code** — CC BY-NC-SA 4.0 — see [LICENSE-CODE](LICENSE-CODE)
- **EPUB output** — CC BY-NC-SA 4.0 — see [LICENSE-CONTENT](LICENSE-CONTENT)
- **Quranic text** — © Tanzil.net — redistribution with attribution permitted
- **Fonts** — SIL Open Font License

---

## Dedication

*This humble work is an ongoing charity (Sadaqa Jariya) for my parents and grandparents, the living and the deceased among them, for my wife and children, and for all the believers around the world, who love the Book of Allah and whose hearts are attached to its recitation, all of them, from the pious predecessors until the Day of Judgement.*

*O Allah, accept it as purely for Your Noble Sake, and benefit all those who recite it and memorize it.*

*Ameen*