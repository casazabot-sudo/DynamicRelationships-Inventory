# Dynamic Relationships 0.8.11

Dynamic Relationships is a SillyTavern extension for tracking character relationships and scene state. This build also includes a minimal per-character inventory module.

## Inventory module
- Inventory records are stored in the current chat metadata alongside Dynamic Relationships state.
- Inventory UI is part of the Dynamic Relationships panel; no separate extension or character registry is created.
- Each item has only a name and quantity.
- Manual add, quantity update, and delete operations are supported.
- The activity journal records manual and AI changes, timestamps, owner, action, and quantity change.
- AI inventory updates use an `INVENTORY_ACTIONS` comment block in assistant output; the formatter removes this protocol block from the rendered message. Replies with no inventory changes are also recorded in the journal as diagnostic entries.
- Settings include inventory enable/disable and exclusion of the main character/Narrator from inventory tracking (enabled by default).
- When inventory tracking is disabled, data remains stored and AI inventory processing is skipped.

## Install
Copy this extension folder into `SillyTavern/public/scripts/extensions/third-party/` (or install through the extension installer if hosted in a repository), then reload SillyTavern.
