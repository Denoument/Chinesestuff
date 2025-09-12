Chinese Character Lookup & Stroke Order
This is a web-based tool for looking up Chinese characters by Pinyin, Zhuyin, or the character itself. It provides detailed information and an animated stroke-order guide for each character, helping users learn to write them correctly.

Key Features
Multilingual Search: Look up characters using Pinyin, Zhuyin (Bopomofo), or the Chinese character directly. The search is not case-sensitive.

Stroke Order Animation: Watch a step-by-step animation of how each character is written.

Play/Pause/Resume Controls: Control the animation playback to study each stroke at your own pace.

Traditional & Simplified Toggle: Easily switch between the Traditional and Simplified versions of a character to see the differences.

Detailed Information: Displays the character's stroke count, Pinyin, Zhuyin, and English meaning.

Dependencies
This app is built with simple web technologies and has a few external dependencies:

HTML, CSS, JavaScript: The core structure, styling, and functionality of the app.

Tailwind CSS: Used for all of the modern, responsive styling.

HanziWriter.js: A powerful JavaScript library that handles the Chinese character rendering and stroke-order animations.

adjustedCharacters.json: A local JSON file containing the character data (Pinyin, Zhuyin, meanings, and stroke counts) for the app to function. You must have this file in the same directory as the HTML file.

How to Use
Clone or Download: Save the index.html and the adjustedCharacters.json files to the same directory on your computer.

Run a Local Server: Due to browser security restrictions, you cannot directly open the index.html file and access the local JSON data. You must serve the files using a local web server.

Using Python: If you have Python installed, navigate to the directory in your terminal and run one of the following commands:

For Python 3: python3 -m http.server

For Python 2: python -m SimpleHTTPServer

Using Node.js: If you have Node.js installed, you can install a simple server package with npm install -g http-server, then run http-server in the directory.

Open in Browser: After starting the server, open your web browser and navigate to http://localhost:8000 (or the address shown by your server).

Search: Use the search bar to type in a query. You can use Pinyin (e.g., hao), Zhuyin (e.g., ㄏㄠˇ), or the character itself (e.g., 好).

Explore:

Click the Play Animation button to see the stroke order. This button will change to Pause and then Resume as needed.

Use the Switch to Simplified/Traditional button to toggle between the two character forms.