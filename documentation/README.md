# Gmail Password Recovery Tool

This tool automates the Gmail password recovery workflow using Puppeteer with undetected-browser to avoid detection.

## Features

- Navigates to Gmail sign-in page
- Inputs email address and clicks next
- Automatically clicks the "Forgot password" option

## Prerequisites

- Node.js (v14 or higher)
- npm (v6 or higher)

## Installation

1. Clone or download this repository
2. Install dependencies:

```bash
npm install
```

## Usage

1. Open `index.js` and replace `'example@gmail.com'` with the actual email address you want to recover

```javascript
const emailToRecover = 'your.email@gmail.com'; // Replace with the actual email
```

2. Run the script:

```bash
npm start
```

3. The script will open a browser window and automatically perform the password recovery workflow

## Debug Logs and Output Structure

- All screenshots, HTML pages, and console logs are saved in a structured folder system under `Debug-Logs`.
- Each run creates a folder named after the email being processed (e.g., `Debug-Logs/your.email@gmail.com`).
- Inside each email folder:
  - `/screenshots`: Contains all screenshots for the run.
  - `/html-pages`: Contains HTML source files saved for debugging.
  - `/console`: Contains `.txt` files with full console logs, each named with the date and time (e.g., `Feb24-1842.txt`).
- Console logs include timestamps for every line.

## Updating and Feature Additions

- This README and `instructions.txt` will be updated with every new feature or addition as requested.

## Notes

- The browser runs in visible mode by default. To run in headless mode, change `headless: false` to `headless: true` in the script
- A screenshot of the recovery page will be saved as `recovery-page.png`
- This tool uses the [undetected-browser](https://github.com/AlloryDante/undetected-browser) package to avoid detection

## Troubleshooting

If you encounter any issues:

- Make sure you have the latest version of Node.js installed
- Check that all dependencies are properly installed
- Google might change their selectors or workflow; if this happens, the selectors in the code may need to be updated