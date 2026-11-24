# Dynamic Relationships + Inventory Module (v0.8.7)

This is the original Dynamic Relationships extension (based on upstream v0.8.4 source) with an optional, integrated Inventory section. Inventory is rendered inside the Dynamic Relationships panel and uses the same chat-scoped `state.entities` registry. Item storage remains in a separate IndexedDB database for continuity with Inventory System v0.3.x.

## Integration changes
- Inventory panel is nested inside the Dynamic Relationships panel.
- User and main character are ensured in the shared character registry; detected NPCs are shared.
- Inventory instructions are appended to the existing Dynamic Relationships prompt under its existing prompt key; no competing Inventory extension prompt is registered.
- The original state-output section order is explicitly preserved: Current Setting -> Noticed Characters -> Secret Thoughts. The inventory command comment is requested after these sections, only when an item change occurred.
- No Inventory generation interceptor is registered.
- Inventory module and auto-apply have separate toggles.
- Existing item database stores are retained; owner IDs for legacy `user` and `char` are mapped to current shared registry IDs.

## Install from GitHub
Upload the contents of this folder to the root of a GitHub repository, then install using SillyTavern Extensions -> Install Extension -> Git URL.

## Testing status
`node --check index.js` and ZIP integrity checks passed. This package has not been run inside SillyTavern. Please test with Inventory disabled first, then enabled, and verify the three original output sections remain in the assistant response.
