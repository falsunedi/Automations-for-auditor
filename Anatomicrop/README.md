# Anatomicrop

Anatomicrop is a macOS Quick Action that automatically crops 120 pixels from the bottom of selected images. It's designed to help UX auditors and researchers quickly remove browser toolbars, status bars, or other unwanted UI elements from the bottom of screenshots.

## Features

- 🚀 **Batch Processing**: Crop multiple images at once
- 📁 **Non-Destructive**: Original images remain untouched; cropped versions are saved in a separate folder
- ⚡ **Quick Action**: Accessible directly from Finder's context menu
- 🔧 **Auto-Install Dependencies**: Automatically installs ImageMagick if not present

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

Follow the on-screen instructions. This package manager is required to install ImageMagick, which powers the cropping functionality.

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

### Alternative Method

1. Select your images in Finder
2. Click the selected images
3. Choose **Quick Actions > Anatomicrop** from the menu bar

## Supported Image Formats

Anatomicrop supports all common image formats including:
- PNG
- JPG/JPEG
- GIF
- TIFF
- BMP
- WebP

## Troubleshooting

### Quick Action Doesn't Appear

**Solution:** Make sure you've installed the workflow by double-clicking `Anatomicrop.workflow`. If it still doesn't appear, try logging out and back in to macOS.

### ImageMagick Installation Fails

**Solution:** Manually install ImageMagick by opening Terminal and running:
```bash
brew install imagemagick
```

If Homebrew isn't installed, complete Step 1 of the installation instructions first.

### Permission Errors

**Solution:** The first time you run the Quick Action, macOS may ask for permission to access files. Make sure to grant these permissions in System Preferences > Security & Privacy > Privacy.

### Nothing Happens When Running the Action

**Solution:** Check if a `cropped` folder was created in the same directory as your images. If not, try running the action on a single image first to check for error messages.

## Technical Details

- **Crop Method**: Removes 120 pixels from the bottom using ImageMagick's `-gravity South -chop 0x120` command
- **Processing**: Images are processed sequentially
- **Output**: Maintains original image format and quality
- **Dependencies**: ImageMagick (auto-installed via Homebrew)

## Uninstalling

To remove Anatomicrop:

1. Open **Automator** application
2. Go to **File > Open**
3. Navigate to `~/Library/Services/`
4. Find `Anatomicrop.workflow`
5. Move it to Trash

## Use Cases

- Remove browser address bars from web page screenshots
- Strip toolbars from application screenshots
- Batch-process UX research screenshots
- Clean up screen captures for presentations or reports

## Feedback & Issues

If you encounter any issues or have suggestions for improvements, please open an issue in the repository.