# UI Test Automation

This project contains an automated UI test script using Python and Playwright. The script, `image_preview_test.py`, tests the file upload and image preview functionality on a web application.

## Prerequisites

- Python 3.8 or higher installed on your system.
- Basic understanding of command-line execution.

## Installation

1. **Navigate to the project directory** (if you aren't already there):
   ```powershell
   cd d:\test_automation_ui
   ```

2. **Install the required Python dependencies:**
   ```powershell
   pip install -r requirements.txt
   ```
   *(This will install Playwright. Alternatively, you can just run `pip install playwright`)*

3. **Install Playwright browsers:**
   Playwright requires specific browser binaries to run. Install them by running:
   ```powershell
   playwright install
   ```

## Running the Tests

The `image_preview_test.py` script can be executed from the command line. It has several configurable arguments.

### Basic Execution (Headless Mode)

To run the test silently without opening a visible browser window:

```powershell
python image_preview_test.py --headless
```

### Visual Execution (Headed Mode)

To watch the test execute in a visible browser window, run it without the `--headless` flag. You can also add a delay (`--slow-mo-ms`) to slow down the interactions so they are easier to follow:

```powershell
python image_preview_test.py --slow-mo-ms 2000
```

### Available Command-Line Arguments

- `--url`: The target URL to test. (Default: `https://www.pixelssuite.com/convert-to-png`)
- `--png`: Path to the image file to upload during the test. (Default: `sample.png` - will be auto-generated if it doesn't exist)
- `--out-dir`: The directory where screenshots should be saved. (Default: `results\`)
- `--csv`: The path to the CSV file where test execution results are logged. (Default: `execution_results.csv`)
- `--headless`: Run the browser in headless mode (no visible UI).
- `--timeout-ms`: Maximum time (in milliseconds) to wait for elements. (Default: `60000` / 1 minute)
- `--slow-mo-ms`: Slow down Playwright operations by the specified amount of milliseconds. Useful for debugging or visual observation. (Default: `0`)

### Example: Running with Custom Parameters

```powershell
python image_preview_test.py --url "https://www.pixelssuite.com/convert-to-png" --headless --timeout-ms 30000 --out-dir custom_results
```

## Test Outputs

After a test execution, two types of artifacts are generated:

1. **Screenshots:** Found in the `results\` directory (or your custom `--out-dir`). A screenshot is taken at the end of the test sequence. Look for `preview_pass.png` if the preview was detected, or `preview_fail.png` / `preview_error.png` if it wasn't.
2. **Execution Logs:** The test results are appended to `execution_results.csv`. This file logs the file path, whether the preview was detected, the final PASS/FAIL status, and the path to the corresponding screenshot.
