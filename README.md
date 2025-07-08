# All-Manga-Downloader

All Manga Downloader: User Guide

The "All Manga Downloader" is a browser extension designed to help you download pages from manga and novel websites. It can either save individual image pages or compile them into a ZIP archive. 

MATCHES: Booklive (https://booklive.jp), Cmoa (https://www.cmoa.jp), EbookRenta (https://ebookrenta.com), Bookwalker (https://bookwalker.jp).

Getting Started:
1. Activation: The extension can be activated in two ways:
* By sending a "global_enabled" message via chrome.runtime.sendMessage.
* By pressing the '0' key on your keyboard (if it's not already globally enabled).

3. Once activated, a message box will appear on the top right of your screen, displaying options for scanning. This message box has a background image.
   
Scanning Content: Before you can download, you need to scan the pages of the manga or novel you are viewing.

For Mangas:

* Ensure the page contains a manga structure recognizable by the extension (e.g., #menu_slidercaption must exist).
* Lite Scan: Press the '1' key to start a "lite" scan. This sets dump_checks to 2.
* Hard Scan: Press the '2' key to start a "hard" scan. This sets dump_checks to 5. A "hard" scan checks more times if pages are fully saved.
* While scanning, the message box will update with the number of pages discovered. You will see a prompt to "Press 4 to finish scan".
* If the extension does not detect a manga, it will display an error message: "Is this a manga? It doesn't seem dumpeable... Press 7 to restart".

For Novels:
* Ensure the page contains a novel structure recognizable by the extension (e.g., #ctmble_menu_lower_indicator_div must exist).
* Start Scanning: Press the '3' key to begin the novel scanning process.
* Capture Pages: While the novel scanner is running, you need to click on the extension icon to scan the current page. Each captured page will be saved as "pX.png" (e.g., p1.png, p2.png).
* While scanning, the message box will show the number of pages captured. You will see a prompt to "Press 4 to finish scan".
* If the extension does not detect a novel, it will display an error message: "Is this a novel? It doesn't seem dumpeable... Press 7 to restart".

Finishing a Scan:
* Regardless of whether you are scanning manga or novels, to stop the scanning process, press the '4' key. This will finalize the scan and enable the download options.

4. Downloading Content: Once scanning is finished and enable_download is active, you will see download options in the message box.

* Download as Individual Images (PNGs):
  
 Press the '5' key to save all scanned pages as individual PNG image files. The files will be named document.title + " - " + key (e.g., "Manga Title - content-1.png").

* Download as a ZIP File:
  
 Press the '6' key to download all scanned pages compiled into a single .zip archive. The ZIP file will be named document.title + ".zip".
Restarting the Extension:

To reset the extension's state, clear all saved pages, and return to the initial menu, press the '7' key. This is particularly useful after a scan or in case of an error.

5. Important Notes:

* The extension's messages are displayed in a box at the top right of your screen.
* Information about the developer, Hikari16, and links to the project's README file on GitHub are included in the messages.
* Some internal processes, like merging image blobs for manga pages, are handled automatically by the extension.
* If a specific page was already saved during a previous scan, the extension will update its count or skip it based on dump_check.

6. In case of errors or if you want to contact me mail me to: evelynshefield@gmail.com.
