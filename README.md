# Dynamic Relationships 0.8.12

Dynamic Relationships is a SillyTavern extension for tracking character relationships and scene state. This build also includes a minimal per-character inventory module.

## Inventory module
- Inventory records are stored in the current chat metadata alongside Dynamic Relationships state.
- Inventory UI is part of the Dynamic Relationships panel; no separate extension or character registry is created.
- Each item has only a name and quantity.
- Manual add, quantity update, and delete operations are supported.
- The activity journal records manual and AI changes, timestamps, owner, action, and quantity change.
- AI inventory updates use an `INVENTORY_ACTIONS` comment block in assistant output, including an empty actions list when nothing changed; the formatter removes the protocol block from the rendered message. Transfers are logged on both giver and receiver sides. Replies without a valid block are recorded diagnostically. User thoughts are filtered from the thoughts footer.
- Settings include inventory enable/disable and exclusion of entities explicitly marked or named Narrator/Рассказчик from inventory tracking (enabled by default); active {{char}} is not excluded automatically.
- When inventory tracking is disabled, data remains stored and AI inventory processing is skipped.

## Install
Copy this extension folder into `SillyTavern/public/scripts/extensions/third-party/` (or install through the extension installer if hosted in a repository), then reload SillyTavern.
