# APK Upload Guide

This guide explains how to upload and release APK files for MediCompanion AI.

## Method 1: GitHub Releases (Recommended)

GitHub Releases is the best way to distribute APK files as it provides:
- Version management
- Download statistics
- Release notes
- Automatic changelog generation

### Steps:

1. **Navigate to the Releases page**
   - Go to: https://github.com/naimhakimi-sketch/MediCompanion-AI-Release/releases
   - Click "Create a new release" or "Draft a new release"

2. **Create a new tag**
   - Tag format: `v1.0.0` (follow semantic versioning)
   - Choose the target branch (usually `main`)

3. **Fill in release details**
   - Release title: `MediCompanion AI v1.0.0`
   - Description: Add release notes (see template below)

4. **Upload APK file**
   - Drag and drop or click to upload your APK file
   - Recommended naming: `MediCompanion-AI-v1.0.0.apk`

5. **Publish release**
   - Click "Publish release" to make it available to users
   - Or "Save draft" to review later

### Release Notes Template:

```markdown
## What's New in v1.0.0

### Features
- New feature 1
- New feature 2

### Improvements
- Improvement 1
- Improvement 2

### Bug Fixes
- Fixed issue 1
- Fixed issue 2

### Installation
1. Download the APK file below
2. Enable "Install from unknown sources" on your Android device
3. Install the APK file
4. Open MediCompanion AI and enjoy!

### System Requirements
- Android 7.0 (API level 24) or higher
- Minimum 2GB RAM
- 100MB free storage space
```

## Method 2: Direct Repository Upload

If you prefer to store APK files directly in the repository:

1. **Add APK to releases folder**
   ```bash
   cd /path/to/MediCompanion-AI-Release
   cp /path/to/your/app.apk releases/MediCompanion-AI-v1.0.0.apk
   ```

2. **Commit and push**
   ```bash
   git add releases/MediCompanion-AI-v1.0.0.apk
   git commit -m "Release: MediCompanion AI v1.0.0"
   git push origin main
   ```

3. **Update README.md**
   - Add download link to the new APK file
   - Update version information

**Note:** GitHub has a 100MB file size limit for direct uploads. For larger files, use Git LFS or GitHub Releases.

## Method 3: Using Git LFS (Large File Storage)

For APK files larger than 100MB:

1. **Install Git LFS**
   ```bash
   git lfs install
   ```

2. **Track APK files**
   ```bash
   git lfs track "*.apk"
   git add .gitattributes
   ```

3. **Add and commit APK**
   ```bash
   git add releases/MediCompanion-AI-v1.0.0.apk
   git commit -m "Release: MediCompanion AI v1.0.0"
   git push origin main
   ```

## Best Practices

1. **Version Naming**: Use semantic versioning (MAJOR.MINOR.PATCH)
2. **APK Signing**: Always sign your APK with the same keystore
3. **Testing**: Test APK on multiple devices before release
4. **Backup**: Keep backup of signing keys and previous APK versions
5. **Changelog**: Always provide detailed release notes
6. **Size Optimization**: Try to keep APK size under 50MB for better download experience

## Security Notes

- Never commit your keystore files to the repository
- Keep your signing keys secure and backed up
- Consider using GitHub Actions for automated builds
- Use ProGuard/R8 for code obfuscation in release builds
