# Ground Truth Annotator

Supplementary project to our Junior Design Project.

A lightweight, local tool designed to speed up the manual correction of AI-generated ground truth data for medical prescription handwriting OCR.

Everything runs 100% locally in your browser—no medical data or images leave your machine.

## How to Use

1. **Load Data:** 
   - Select your ground truth `.txt` file.
   - Select the folder containing your prescription images.
2. **Click "Display / Start":** The tool will match the filenames parsed from the text file with the images in your folder.
3. **Correct & Navigate:** 
   - Edit the text directly on the left panel while viewing the image on the right.
   - Drag the divider to resize panels, or use your mouse wheel to zoom/pan on dense handwriting.
4. **Export:** Click **Export** (or press `Alt + S`) to download your updated `.txt` file ready for training.

## Keyboard Shortcuts

- `Alt` + `→` : Move to the next entry
- `Alt` + `←` : Move to the previous entry
- `Alt` + `S` : Export the corrected `.txt` file

## Setup

No installation or node modules required. Just open `index.html` in your browser or host it via GitHub Pages.
