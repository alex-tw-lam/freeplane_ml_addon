# Release Process

## Automated Release (Recommended)

### Option 1: Tag-based Release
1. Commit your changes
2. Create and push a tag:
   ```bash
   git tag v0.7.0
   git push origin v0.7.0
   ```
3. GitHub Actions will automatically:
   - Build the addon file
   - Create a GitHub release
   - Upload `LLM-AddOn-v0.7.0.addon.mm` to the release

### Option 2: Manual Workflow
1. Go to [Actions](https://github.com/alex-tw-lam/freeplane_ml_addon/actions) in your repo
2. Select "Build and Release Addon" workflow
3. Click "Run workflow"
4. Enter the version number (e.g., v0.7.0)
5. Click "Run workflow"

## Local Development Build

If you need to build locally:

### Prerequisites
- Java 17+
- Gradle 8.5+ (or use included gradlew)

### Build Steps
```bash
# Using gradlew (recommended)
./gradlew jar
./gradlew freeplaneCreateAddon

# Or using system gradle
gradle jar
gradle freeplaneCreateAddon
```

The addon file will be generated as `LLM-AddOn-v0.7.0.addon.mm` in the project root.

## Installation

1. Download the latest `.addon.mm` file from [Releases](https://github.com/alex-tw-lam/freeplane_ml_addon/releases)
2. In Freeplane: Tools → Add-ons → Install Add-on
3. Select the downloaded file and restart Freeplane

## Version Management

- Update `version.properties` file before creating releases
- The workflow automatically uses the version from this file
- Releases are automatically tagged and uploaded to GitHub