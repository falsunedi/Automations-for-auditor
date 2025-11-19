# Anatomicrop

Anatomicrop is a macOS Quick Action that automatically crops 120 pixels from the bottom of selected images.

## What It Does

Anatomicrop removes exactly 120 pixels from the bottom of each selected image and saves the cropped version in a `cropped` subfolder within the same directory as your original images.

**Example:**
- Original image: `/Users/yourname/Screenshots/screenshot1.png`
- Cropped image: `/Users/yourname/Screenshots/cropped/screenshot1.png`

## Prerequisites

- **macOS** (tested on macOS 10.15+)
- **Homebrew** (will be installed during setup if not present)

## Installation

### Step 1: Install Homebrew (if not already installed)

Open Terminal and run:

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Step 2: Install the Anatomicrop Quick Action

1. Navigate to the `Anatomicrop` folder in this repository
2. Double-click the `Anatomicrop.workflow` file
3. macOS will ask if you want to install the Quick Action
4. Click "Install" to add it to your Quick Actions

**Note:** The first time you use Anatomicrop, it will automatically download and install ImageMagick via Homebrew. This is a one-time setup that may take a minute or two.

## How to Use

1. **Select Images**: In Finder, select one or more images you want to crop
2. **Right-Click**: Right-click (or Control-click) on the selected images
3. **Quick Actions**: Hover over "Quick Actions" in the context menu
4. **Run Anatomicrop**: Click "Anatomicrop"

The cropped images will be saved in a new `cropped` folder in the same directory as your original images.

