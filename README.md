# Freeplane LLM Addon

A Freeplane addon that integrates with LLM APIs for brainstorming and content generation.

## Features

- **Quick Prompt (Ctrl+Alt+G):** Generate ideas from any selected node
- **Multiple LLM Providers:** Support for OpenAI, OpenRouter, and DeepSeek
- **Compare Connected Nodes:** Analyze relationships between nodes
- **Image Generation:** Create images based on node content
- **Automatic Tagging:** Generated content is tagged with model information

## Installation

1. Download the latest `.addon.mm` file from [Releases](https://github.com/alex-tw-lam/freeplane_ml_addon/releases)
2. In Freeplane: `Tools → Add-ons → Install Add-on`
3. Select the downloaded file and restart Freeplane

## Quick Start

1. Configure your API key: `LLM → Configure Prompts & Model`
2. Select a node in your mind map
3. Press `Ctrl+Alt+G` to generate content
4. Use `Tools → LLM AddOn` for advanced features

## Development

### Prerequisites
- Java 17+
- Gradle (or use included gradlew)

### Build
```bash
./gradlew freeplaneCreateAddon
```

### Release
```bash
git tag v0.7.0
git push origin v0.7.0
```

## Supported Providers

- **OpenAI:** GPT models
- **OpenRouter:** Multiple model access
- **DeepSeek:** Chat and coding models
- **Novita:** Image generation

## License

See LICENSE file for details.