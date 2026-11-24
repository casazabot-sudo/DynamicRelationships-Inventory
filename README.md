# Dynamic Relationships Inventory 0.8.13

Integrated inventory module and stability fixes for state footer parsing/rendering.

## Changes
- Robust parsing for scene setting labels and emoji variants.
- More tolerant noticed-character section parser, including alternate marker spelling and multiline fields.
- Thoughts parser accepts both `Name: thought` and a standalone registered name followed by multiline thought. User persona thoughts are filtered (including entities marked user/main_character), while active bot character thoughts are not automatically excluded.
- Footer CSS scoped to the extension container, including narrow-screen rules.
- Inventory AI may update user inventory when a completed event is narrated.
- Completed transfers/removals reconcile untracked stock and add explicit journal correction entries.
- Narrator exclusion is limited to explicitly named/typed Narrator; main character owner inventory is not omitted by default.
- Version metadata synchronized to 0.8.13.

## Validation
Node syntax check, parser sample tests, inventory transfer reconciliation sample, and ZIP integrity check performed. Runtime validation inside SillyTavern was not performed.
