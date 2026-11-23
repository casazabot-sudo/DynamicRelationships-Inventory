# Dynamic Relationships + Optional Inventory Module

GitHub repository-ready package for SillyTavern. This is based on Dynamic Relationships 0.8.4 with an optional Inventory module integrated into the same extension.

## Install through SillyTavern GitHub installer

1. Publish these repository files to a GitHub repository (the files in this package must be at repository root).
2. In SillyTavern, open Extensions and choose Install extension.
3. Paste your repository URL, for example `https://github.com/YOUR-USERNAME/DynamicRelationships-Inventory`.
4. Install, then reload SillyTavern.
5. Disable/remove the separate Inventory System extension to avoid duplicate handlers.
6. First test with Inventory module turned off; then enable it and test.

## Important

This is repo-ready content, not a published GitHub repository. You must upload it to GitHub before SillyTavern can install it by GitHub URL. Runtime testing in SillyTavern has not been performed.

## Inventory module

- Toggle to enable/disable inventory prompt and AI response processing.
- Separate toggle for automatic application of AI changes.
- Per-chat local inventory data with backup/restore and manual item management.

The original Dynamic Relationships features are intended to remain available. Check the extension console and generation behavior after installation before relying on this experimental build.


## v0.8.6 fix

Inventory panel initialization now retries until the extension settings container exists and reinitializes on app/chat-ready events, addressing the missing module panel reported after install.
