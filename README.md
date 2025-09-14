---
title: Chinese Character Learning App
description: Usage guide and technical documentation
---

## Usage Guide

### Basic Navigation
* **Select Study Parameters:**
    * Choose characters per day (1-10)
    * Select specific day from dropdown
    * Toggle between Traditional/Simplified mode
* **Character Interaction:**
    * Click character animation controls to see stroke order
    * Use "Show Meanings" to reveal/hide definitions
    * Study pronunciation with Pinyin and Zhuyin displays
* **Worksheet Generation:**
    * Click "Generate Worksheet" after selecting characters
    * Choose number of rows (5, 8, 10, or 12)
    * Toggle "Add Characters" checkbox to include/exclude reference characters
    * Download as PDF for printing

### Character Data Format
The application expects `adjustedCharacters.json` with the following structure:

```json
[
  {
    "char": "傳",
    "simplifiedChar": "传",
    "pinyin": "chuan2",
    "zhuyin": "ㄔㄨㄢˊ",
    "TradStrokeCount": 13,
    "SimpStrokeCount": 6,
    "meaning": "to transmit, to summon",
    "pinyinTone": "chuán",
    "unicode": "U+50B3",
    "radical": "人",
    "frequency": "common",
    "hskLevel": 4
  }
]
## Customization

### Adding New Characters
-   Add characters to `characters.txt` (one per line)
-   The system will automatically process and include them in the study sequence

### Modifying Worksheet Layout
-   Edit the CSS variables in the stylesheet to adjust:
    -   Cell sizes (`50px` for characters, `16px` for Zhuyin)
    -   Grid spacing and borders
    -   PDF output formatting

### Styling Changes
-   The app uses Tailwind CSS with custom styles. Modify the `<style>` section in `index.html` for:
    -   Color schemes
    -   Font sizes
    -   Layout adjustments
    -   Animation styles

---

## Technical Details

### Built With
-   **Frontend:** HTML5, CSS3, JavaScript (ES6+)
-   **Styling:** Tailwind CSS + Custom CSS
-   **Character Animation:** HanziWriter library
-   **PDF Generation:** html2pdf.js
-   **Font:** Google Fonts (Inter)
-   **Icons:** Custom favicon set

### Browser Support
-   Chrome 70+
-   Firefox 65+
-   Safari 12+
-   Edge 79+

### Performance Features
-   Lazy loading of character data
-   Efficient stroke animation rendering
-   Optimized PDF generation
-   Responsive image handling

---

## Troubleshooting

### Common Issues
-   **Character data not loading**
    -   Ensure `adjustedCharacters.json` exists in the same directory
    -   Check browser console for fetch errors
-   **PDF generation fails**
    -   Allow pop-ups for the site
    -   Ensure sufficient memory for large worksheets
-   **Animations not working**
    -   Check internet connection (HanziWriter loads from CDN)
    -   Verify browser supports Canvas API
-   **Mobile display issues**
    -   Use latest browser version
    -   Ensure viewport meta tag is respected

### Debug Mode
-   Open browser developer tools (F12) to see:
    -   Character loading status
    -   Animation performance
    -   PDF generation logs