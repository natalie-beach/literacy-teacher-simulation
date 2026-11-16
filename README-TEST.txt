LITERACY TEACHER: NON-DESTRUCTIVE H5P PLAYER TEST

STATUS: TEST PACKAGE ONLY. NOT A COMPLETE WORKING PLAYER YET.

Included:
  h5p-test.html         separate test page, never replaces index.html
  original-scenario.h5p original Canvas H5P export, unchanged

REQUIRED THIRD FILE (not included because package downloads were unavailable here):
  h5p-sw.js             exact service worker for player version 1.5.1

Download the service worker in your browser from:
https://cdn.jsdelivr.net/npm/@missing-elements/h5p-offline-player@1.5.1/dist/h5p-sw.js
Save it with the exact filename h5p-sw.js.

Then upload these THREE files to the root of your GitHub repository:
  h5p-test.html
  original-scenario.h5p
  h5p-sw.js

DO NOT delete or replace index.html, app.js, config.js, style.css, questions.json, or Code.gs.

After GitHub Pages publishes, open:
https://natalie-beach.github.io/literacy-teacher-simulation/h5p-test.html

This is a standalone playback test, not the finished segmented course. It does NOT send scores to Sheets.

Important: The player requires a Service Worker and may not work on GitHub Pages project-path hosting due to worker scope/path constraints. If it fails, send the exact browser error or a screenshot. The CDN URLs are pinned to the versions shown in the project's setup documentation, but compatibility with this particular export has not been tested. H5P video resources may also require internet access or authentication.

Source and setup details:
https://github.com/missing-elements/h5p-offline-player/blob/main/docs/setup.md
