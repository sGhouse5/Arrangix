# Arrangix

Arrangix arranges your photos onto pages and exports them as a **Word (.docx)** or **PDF** file.
It is a single file, `Arrangix.html`. Open it in a browser, add photos, choose a layout, and download.
Your photos are processed inside your browser and are not uploaded anywhere.

---

## 1. Core rules (non-negotiable)

These rules take priority over every feature.

1. **Never distort a photo.** A photo keeps its original aspect ratio at all times. It is never stretched, squashed, or cropped to fill a column, cell, or page.
2. **Width and height always scale together.** A photo may get bigger or smaller to fit the layout, but both sides change by the same factor.
3. **Rotation keeps proportions.** Turning a photo swaps its width and height. It never changes the ratio between them.
4. **Proportions and quality come before filling space.** A photo may sit narrower than its column or cell, leaving blank space, rather than being forced to fill it.
5. **Grid structure never changes because of rotation.** In Grid mode, rows × columns fixes the cell sizes and the page count. Rotation only turns the photo inside its own cell.
6. **Rotation never enlarges a photo in Smart mode.** A rotated photo keeps the same scale it had before rotating.
7. **No watermark.** A watermark was tried and removed. None is added to exports.

---

## 2. Adding and managing photos

- Click the drop area to choose photos, or drag and drop them in.
- Supported types: JPEG, PNG, WebP, GIF, BMP, and HEIC/HEIF (iPhone photos).
- Each photo appears as a thumbnail with four buttons:

| Button | What it does |
|---|---|
| ⠿ | Grab here to move the photo (Grid mode only; Smart mode arranges photos itself). See "Moving photos" below |
| ⧉ | Duplicate the photo |
| ↻ | Rotate 90° (click again for 180°, 270°, back to 0°) |
| ✕ | Remove the photo |

- **Moving photos (Grid mode):** grab a photo by its ⠿ dots, like moving an app on a phone's home screen. The photo lifts and follows your finger or pointer, its old spot becomes a dashed slot, and the other photos slide aside live. **The slot is exactly where the photo will land.** Let go to drop it. Press Esc, or let go far outside the list, to cancel. Dragging near the top or bottom edge scrolls the page. Swiping anywhere else on a photo still scrolls normally, and tapping a photo still selects it. One move is one Undo step. With the keyboard, focus the dots, press Space to lift, use the arrow keys to move, then Space or Enter to drop, or Esc to cancel.
- **Clear all** removes every photo.
- **Undo** (link next to Clear all, or Ctrl/Cmd+Z) steps back through remove, clear all, rotate, duplicate, reorder and sort. It remembers the last 20 actions. Adding photos is not undone.
- **Sort photos** (Grid mode only): a dropdown that always shows the current order, with three choices: **Order added** (the order you uploaded in, with copies kept beside their original), **Date taken — oldest first**, and **Date taken — newest first**. After you drag photos by hand it reads **Custom order** (not a choice you can pick). The date comes from the photo's built-in data (JPEG only). PNG, screenshots and converted HEIC photos use the file's last-modified date. In Smart mode the dropdown is disabled, because Smart arranges photos itself.
- **Select photos:** click a thumbnail (Shift-click for a range) to select it. **Select all**, **Rotate selected** and **Remove selected** work on the selection, and Undo covers them. Thumbnails show the whole photo.
- **Similar photos:** photos that are the same picture (the same screenshot added twice, or a resized or re-saved copy) are grouped. The **first photo of a group in the current list is the Original** and is tagged "Original A". The others are tagged in list order: "Similar A1", "Similar A2". A second group is B, a third is C, and each group has its own outline colour. A summary line shows for example "A: original + 2 similar · B: original + 1 similar". If you reorder the list, "Original" moves to whichever photo comes first. **Remove N similar (keeps originals)** removes every Similar photo, never an Original, and can be undone. Photos you make with the ⧉ button are labelled in their group but never removed by that button. The check is strict: it compares the whole picture and every small region, so screenshots of the same window or logos with different text get no tag. It says "Similar" rather than "Duplicate" because only an exact pixel match could be called identical, and resized or re-saved copies are never exact.
- **Soft-print warning:** the summary line warns when photos would be below 150 DPI at their drawn size (for example a 1080 px screenshot filling a wide page). It is shown only in the app and nothing is written to the file.
- **Keyboard and screen readers:** every control can be reached with Tab. Enter or Space opens the file chooser and selects thumbnails. With the ⠿ handle focused, the arrow keys move a photo (Grid only). Buttons have descriptive labels, and the summary line is announced.
- A live preview shows each page, with ‹ › buttons to move between pages. A summary line shows the photo count and page count.

---

## 3. Layout modes

### Grid
- You choose **Rows** and **Columns**. Each page is divided into equal cells.
- Photos fill cells in your order.
- Each photo is shown **whole and centred** in its cell. If the photo's shape differs from the cell's, white bars appear. Nothing is cropped or stretched.
- The last page may have blank cells. The summary line says how many.

### Smart
- You choose **Columns**. **Rows is hidden** because it is not used.
- Photos are packed by **height**: each page is filled top to bottom, then a new page starts. This usually needs fewer pages than Grid.
- The original order is not kept.
- Each photo is sized to the column width, centred in its column. It only shrinks, never stretches, if it would otherwise be too wide or taller than the page.

---

## 4. Settings

| Setting | Options | Notes |
|---|---|---|
| Rows | 1–10 | Grid only |
| Columns | 1–10 | Both modes |
| Gap | 0–30 mm | Space between photos. Very large gaps are limited automatically so the layout cannot break. |
| Page size | A4, A5, A3, Letter, Square (20×20 cm), Custom | Custom accepts 50–558 mm for each side (Word's limit is about 558 mm). Orientation applies to every size except Square. |
| Orientation | Portrait, Landscape | The preview changes shape to match. |
| Quality | Standard (150 DPI), High (220), Maximum (300), Original detail | Standard is the default. See section 6. |
| Auto-rotate | On / Off | Grid only. Off by default. See section 5. |
| File name | Optional text | See section 7. |
| Format | Word (.docx) or PDF | |

- The page margin is **0.25 in (about 6.35 mm)** on every side. Tick **Printer-safe margin** to use **10 mm** instead. This keeps photos clear of the edge many printers cannot print. Photos scale down uniformly to fit, so the page count may rise.
- Invalid values are corrected automatically (for example, 50 rows becomes 10).
- **Remembered settings:** mode, rows, columns, gap, page size, orientation, quality, auto-rotate, printer-safe margin, and format are saved in your browser and restored next time. The file name and your photos are not saved. Click **Reset settings** to restore the defaults.

---

## 5. Rotation

There are two separate kinds, and they never interfere with each other.

**Manual rotate (↻ on a thumbnail)**
- Your own correction, for a photo that is genuinely sideways (for example a scan).
- Works in Grid and Smart.
- Automatic rotation never overwrites it.
- Phone photos normally display upright already, because browsers apply the orientation stored in the photo.

**Auto-rotate (checkbox, Grid only)**
- Turns a photo an extra 90° only if that makes it **at least 5% bigger** inside its cell.
- Never makes a photo smaller.
- Recalculated whenever rows, columns, gap, page size, or orientation change.
- Ignored completely in Smart mode.

**In Smart mode**, a rotated photo keeps its size. A landscape photo rotated to portrait becomes narrower than the column and sits centred. It still needs more height than before, because its long side is now vertical, so the page count can still go up. The summary line shows the effect immediately.

---

## 6. Quality

- Each photo is redrawn at the size it appears on the page, using high-quality smoothing, and saved as a JPEG at 90% quality.
- **Standard** is 150 DPI, **High** 220, **Maximum** 300.
- **Original detail** keeps the photo's own resolution, up to 600 DPI. Files can become very large.
- Any single image is capped at about 16 megapixels to avoid browser failures. If a photo was reduced, a note appears after export.
- Photos are redrawn rather than embedded as the original file, so phone orientation data cannot cause sideways pictures in Word or PDF.

---

## 7. Downloaded file name

- If you type a name, for example `Trip`, the file is `Arrangix-Trip.pdf` or `Arrangix-Trip.docx`.
- If you leave it empty, the default is `Arrangix-grid-2026-11-04_08-26-33` style: tool name, mode, then date and time in **India time (IST)**.
- Characters that are not allowed in file names (`\ / : * ? " < > |`) are removed.
- A `.pdf` or `.docx` that you type yourself is dropped so it does not repeat.
- Names are limited to 100 characters.

---

## 8. Output details

- **Word (.docx):** every photo is placed at an exact position on its page. Pages are separated by page breaks.
- **PDF:** each photo is placed at an exact position and size.
- Before a photo is written to the file, its box is adjusted to the drawn image's exact proportions, so rounding to whole pixels cannot stretch it.
- No outside libraries are needed for Word or PDF. The ZIP and PDF writers are built into the file, so export works offline.

---

## 9. Privacy and offline use

- Photos never leave your device.
- Everything works offline **except converting HEIC/HEIF photos in browsers that cannot read them natively**. Safari and other Apple browsers read HEIC themselves, so no internet is needed there. Elsewhere the converter loads from the internet when you add a HEIC photo. If that is impossible, the photo shows "needs an internet connection", a notice explains what to do, and **Try again** or **Dismiss** is offered. All other photo types keep working.

---

## 10. Memory use

- When a photo is added, it is decoded once and a small (700 px) preview is made for thumbnails and the preview page. The full-size version is then released.
- At export, photos are loaded one at a time, drawn, and released. This keeps large batches lighter.
- Rotated thumbnails and previews are drawn from the small preview, so their proportions can differ from the original by under one pixel. Exports always use the full-size photo.

---

## 11. Known limits

- **Printing:** many home printers cannot print the outer 5–6 mm of a page, so photos close to the edge may be clipped on paper with the default margin. Tick Printer-safe margin to avoid this. Screen and PDF output are not affected.
- **Word compatibility:** photos are floating images anchored to the page. The Word output was checked in LibreOffice (positions, margins and proportions were correct) but has not been tested in Microsoft Word or Google Docs, where positions may differ.
- **HEIC:** outside Apple browsers it needs internet to convert (a clear notice is shown when it can't). Converted photos are released when removed (an undo-able removal keeps them until it is pushed out of the 20-step history).
- **Time zone:** the default file name always uses India time, whatever the device's time zone.
- **Accessibility:** tested with keyboard automation and label checks only, not with a real screen reader.
- **Phones:** tested in an emulated phone browser (no horizontal scrolling, touch drag works), not on a real device.
- **Smart mode:** photo order is not kept. This is deliberate: free packing fills the page best (in testing, keeping order cost Smart 4–15 points of page coverage). Use Grid when order matters.

---

## 12. Troubleshooting

| Problem | What to do |
|---|---|
| A thumbnail says "could not read" | Read the reason shown next to it. The browser could not decode that file, so try re-saving it as JPEG or PNG. |
| HEIC photo fails | Read the notice. Outside Apple browsers the converter needs internet. Connect and press Try again, or convert the photo to JPEG first. |
| File is very large | Lower the Quality setting. Avoid "Original detail" for big batches. |
| Photos look small in Grid | Try a different rows/columns count, or switch Auto-rotate on for landscape photos in portrait cells. |
| More pages than expected in Smart mode | Check for manually rotated photos. Rotated landscape photos need more height. |
| Settings are not remembered | The browser may block local storage for local files. Use the **Reset settings** link and set them again. |

---

## 13. Decisions made along the way

- **Watermark:** tried at the bottom-left of each page, then removed completely, because its location was never settled.
- **Fit vs crop:** an option to crop photos to fill cells was dropped, because it breaks the rule that photos are never cropped.
- **Smart mode:** changed from fixed counts per page to true height-based packing.
- **Rotation:** redesigned so Grid-oriented auto-rotation can never inflate Smart mode's page count, and so rotation never enlarges a photo in Smart mode.
- **Album / fitted rows:** a third layout (rows of equal height, widths from each photo's shape) was tested and dropped. It covered no more of the page than Grid or Smart, so it added a mode without a clear gain. Fitting rows inside Grid was also dropped, because mixing aligned and fitted rows looks worse than uniform bars.
- **Smart keeping order:** rejected. Free packing is Smart's purpose.
- **Move to start/end buttons:** left out. The thumbnail cards are too narrow for more buttons, so Sort and drag cover ordering.
- **Rejected ideas:** per-photo cell span and page background colour.
- **Added later:** accessibility, soft-print warning, more page sizes, duplicate detection, multi-select and whole-photo thumbnails.
- **Not done:** changing the default file name time zone (always India time).

---

## 14. Ideas for later

- Check Word output in Microsoft Word and Google Docs, and the app on real phones and a real screen reader.
- Optional only if asked for: Smart keeping order (rejected so far because it costs page coverage).
