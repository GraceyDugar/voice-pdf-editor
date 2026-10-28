# SayPDF

**Edit a PDF by saying what you want.** SayPDF is a voice-controlled PDF editor built for [Wispr Flow](https://wisprflow.ai). Hold your Wispr key, say *"rotate page 4 left, delete the last page and add page numbers"*, let go, and it's done.

**Live demo:** https://graceydugar.github.io/voice-pdf-editor/

![SayPDF screenshot](saypdff.png)

## Try it in 30 seconds
1. Open the [live demo](https://graceydugar.github.io/voice-pdf-editor/). A sample PDF with a sideways page, a blank page and a duplicate is already loaded.
2. Click the command box and say (or type) **"Rotate page 4 left, remove blank pages and delete the last page"**.
3. Click **Download**. Your fixed PDF is ready.

## The problem
Fixing a PDF (removing a blank page, turning a sideways scan, reordering pages) usually means uploading private documents like ID cards, bank statements or contracts to ad-filled websites. SayPDF does it in your browser, by voice, and your file never leaves your device.

## What you can say
| Task | Example |
|---|---|
| Edit text | "Change Rental Agreement to Lease Agreement", "Replace Pune with Mumbai" |
| Remove pages | "Delete pages 2 to 4", "Remove blank pages", "Keep only pages 1 and 3" |
| Turn pages | "Rotate page 4 left", "Turn all pages upside down" |
| Reorder | "Move the last page to the front", "Swap pages 1 and 2", "Reverse the order" |
| Add | "Duplicate page 2", "Insert a blank page after page 1", "Merge another PDF" |
| Write on pages | "Write Approved on page 1", "Stamp PAID in red", "Watermark CONFIDENTIAL", "Sign the last page as Priya Shah", "Add page numbers" |
| View | "Zoom in", "Show page 2", "Next page", "Close" |
| Hinglish | "Page 3 hatao", "Khali pages hatao", "Aakhri page ko pehle lao", "45,000 ko 60,000 kar do" |
| Finish | "Undo", "Start over", "Save as Rent agreement final" |

Several commands can be chained in one sentence, in English or Hinglish (romanised or Devanagari). Every spoken command flashes as a large caption so you can see exactly what was heard. Page numbers always refer to what you see on screen when you start speaking.

## How it works with Wispr Flow
Wispr Flow types your speech into whatever text box is focused. SayPDF detects when dictated text lands in its command bar and runs it right away, so the whole flow is hands-free: no clicking, no Enter key.

## Set up Wispr Flow (2 minutes)
1. Install [Wispr Flow](https://wisprflow.ai) and allow microphone access.
2. Open SayPDF and click the command box.
3. Hold **Fn** (Mac) or **Ctrl + Win** (Windows), speak, and let go. SayPDF runs the command as soon as the text lands.

No Wispr? Use the mic button in Chrome, or just type.

## How it works
- **Command parser:** plain-English sentences are split into clauses and mapped to page operations (number words, ordinals, ranges, "last page", "all except" and more).
- **Rendering:** [PDF.js](https://mozilla.github.io/pdf.js/) draws page thumbnails; blank pages are detected from pixel ink coverage.
- **Export:** [pdf-lib](https://pdf-lib.js.org/) builds the new PDF with rotations, stamps, signatures, watermarks and page numbers.
- **Privacy:** no server, no upload, no tracking. One static HTML file.

## Limitations
- Text editing works on digital PDFs. Scanned PDFs are images, so their words can't be changed (yet).
- Edited text is covered and rewritten, so the original words still exist underneath the new ones.
- Password-protected PDFs need the password removed first.

## Roadmap
- OCR, so scanned PDFs become editable
- Saved routines: say "scan cleanup" to run your usual fixes in one go
- More Indian languages beyond Hinglish

## Run locally
Open `index.html` in a browser. That's it.

## Built for
The [No Hands: Wispr Challenge](https://www.wemakedevs.org/wispr) by WeMakeDevs and Wispr Flow, built by voice.

## License
MIT
