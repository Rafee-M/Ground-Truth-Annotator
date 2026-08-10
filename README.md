
<h1 align="center">Ground Truth Annotator</h1>

<p align="center">
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white" alt="HTML5">
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white" alt="CSS3">
  <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black" alt="JavaScript">
  <img src="https://img.shields.io/badge/runs-100%25%20locally-blue" alt="Runs Locally">
  <img src="https://img.shields.io/badge/license-MIT-lightgrey" alt="License">
</p>

Supplementary project to our Junior Design Project.
A lightweight, local-first annotator for correcting AI-generated ground truth data on medical prescription handwriting OCR. No server, no install, offline first.



## Features 

**Editing**
- Side by side view: raw transcription + JSON on one side, prescription image on the other
- Drag to resize the panels, click the swap button to flip their sides.
- Mouse-wheel zoom and click-drag pan image control/transformation
- Linked drug name editing: correct a drug name once, in either the transcription or the JSON, and the matching occurrence on the other side updates automatically, using an overlay that highlights each linked pair in its own color

**Medicine database**
- A search bar in the top panel queries Medex dataset and highlights the matched text in each result
- Fuzzy, typo tolerant suggestions appear under the editor as you type a drug name, ranked by closeness to what's typed

**Workspace**
- Dark mode, following OS setting by default and remembering a manual override
- Autohide toggle to collapse the top control bar and reclaim screen space
- Fullscreen support (F11)
- Export writes corrections back to the original `###IMAGE` / `###ENDIMAGE` `.txt` format

## Built With

- Vanilla HTML, CSS, and JavaScript
- [fuzzball.js](https://github.com/nol13/fuzzball.js) — fuzzy string matching for the drug name suggestions, loaded from a CDN
- Browser native APIs: the File and Directory Access API for loading local files and image folders, the Fetch API with `localStorage` caching for the medicines dataset, `URL.createObjectURL` for previewing and exporting files, and the Fullscreen API

## How to Use

1. **Load Data:** 
   - Select your ground truth `.txt` file.
   - Select the folder containing your prescription images.
2. **Click "Start":** The tool will match the filenames parsed from the text file with the images in your folder.
3. **Export:** Click **Export** (or press `Alt + S`) to download your updated `.txt` file ready for training.

## Keyboard Shortcuts
| Shortcut | Action |
|---|---|
| `Alt` + `→` | Next entry |
| `Alt` + `←` | Previous entry |
| `Alt` + `S` | Export corrected file |

## Setup

No installation, no `node_modules`. Open `index.html` directly in your browser, or use the hosted [Github Pages version](https://rafee-m.github.io/Ground-Truth-Annotator/)
