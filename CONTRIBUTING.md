# Contributing to MediCompanion AI Release

Thank you for contributing to MediCompanion AI! This guide will help you upload and manage APK releases.

## Quick Start for Uploading APK

### Using GitHub Releases (Recommended)

1. Go to https://github.com/naimhakimi-sketch/MediCompanion-AI-Release/releases
2. Click "Draft a new release"
3. Create a new tag (e.g., `v1.0.0`)
4. Add release title: "MediCompanion AI v1.0.0"
5. Fill in release notes (use [template](./RELEASE_NOTES_TEMPLATE.md))
6. Upload your APK file
7. Click "Publish release"

For detailed instructions, see [UPLOAD_GUIDE.md](./UPLOAD_GUIDE.md)

## Release Checklist

Before publishing a new release:

- [ ] APK is properly tested on multiple devices
- [ ] APK is signed with the production keystore
- [ ] Version number follows semantic versioning
- [ ] Release notes are complete and accurate
- [ ] All known issues are documented
- [ ] APK file is named correctly: `MediCompanion-AI-vX.Y.Z.apk`
- [ ] Previous releases are still accessible

## Version Numbering

Follow [Semantic Versioning](https://semver.org/):

- **Major (X.0.0)**: Breaking changes or major new features
- **Minor (0.X.0)**: New features, backwards compatible
- **Patch (0.0.X)**: Bug fixes and minor improvements

Examples:
- `v1.0.0` - Initial release
- `v1.1.0` - Added new feature
- `v1.1.1` - Fixed bugs in v1.1.0

## File Naming Convention

APK files should follow this format:
```
MediCompanion-AI-v[VERSION].apk
```

Examples:
- `MediCompanion-AI-v1.0.0.apk`
- `MediCompanion-AI-v1.2.3.apk`

## Automated Releases

This repository includes a GitHub Actions workflow that can automate release creation:

1. Tag your commit: `git tag v1.0.0`
2. Push the tag: `git push origin v1.0.0`
3. The workflow will create a draft release
4. Review and publish the release on GitHub

## Best Practices

1. **Test Thoroughly**: Always test on multiple devices before release
2. **Keep History**: Never delete old releases unless absolutely necessary
3. **Document Changes**: Always provide detailed release notes
4. **Announce Updates**: Notify users of new releases through appropriate channels
5. **Monitor Feedback**: Track user feedback and bug reports after release

## Security

⚠️ **Never commit these files to the repository:**
- Keystore files (*.jks, *.keystore)
- Key passwords or credentials
- Private API keys
- Signing configurations

## Need Help?

For questions about the release process, refer to:
- [Upload Guide](./UPLOAD_GUIDE.md) - Detailed upload instructions
- [Release Notes Template](./RELEASE_NOTES_TEMPLATE.md) - Template for release notes
- GitHub Actions workflow - Automated release creation

## Maintainer Access

Only authorized maintainers should upload releases. If you need access, please contact the repository owner.
