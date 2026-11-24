# Dynamic Relationships + Inventory v0.8.9

Integrated Inventory module nested inside Dynamic Relationships. Inventory uses the shared Dynamic Relationships character registry and a separate IndexedDB for item records.

## v0.8.9 changes
- Fixed Inventory IndexedDB request/transaction result handling.
- Bumped inventory database schema to v4 and ensures the `byChat` indexes exist on stores, including existing stores.
- Owner loading now displays loading state and reports registry/database errors instead of remaining blank.
- MESSAGE_RECEIVED handler accepts event payload objects or IDs and reports scan completion explicitly.
- Prevents fallback footer rendering when the formatter already rendered state footers.
- Removes raw state-block paragraphs from formatted message display before adding footer cards.

## Install
Upload these repository files to the root of a GitHub repository, then install via SillyTavern Extensions → Install Extension using the repository URL. Disable/remove the standalone Inventory extension. Back up chat and inventory data before upgrading.

Runtime testing in SillyTavern has not been performed in this environment.
