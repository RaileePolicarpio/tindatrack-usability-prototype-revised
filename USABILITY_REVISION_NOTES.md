# TindaTrack Usability Revision 7 - Round 2 Implementation Notes

## Revision goal

Round 2 testing largely validated Revision 6. Testers described the revised system as clear, complete, easy to navigate, adaptable, time-saving, and capable of replacing paper records. The remaining concern was not missing functionality; it was the possibility that advanced or store-specific options could become confusing or visually crowded for businesses that do not need them.

Revision 7 therefore follows this principle:

**Keep the complete capability, but show specialized functions only when the store needs them.**

## Round 2 feedback translated into changes

### Advanced option complexity / initial onboarding
Revision 7 adds short first-use explanations for FIFO, stock adjustments, physical stock counts, and the More-actions menu. The owner tour was expanded to explain these concepts in plain language.

### Feature clutter potential
The previous Simple Mode setting is now a functional **Simple View**. In Inventory, common actions remain visible while less common tools are grouped under More.

### Store-to-store differences
Reseller Management, Expiration Tracking, and Batch/FIFO remain available because different testers valued different features. Disabling a module now removes its related UI from everyday screens instead of leaving unused controls visible.

### Expense customization
Custom expense categories already existed, but one tester still needed clarification. The Add Expense form now explicitly tells users to choose Custom and reveals the custom-category input only after that choice.

### Reports
The simplified Reports design is retained. Detailed reports remain hidden by default, and reseller-specific report content disappears when Reseller Management is disabled.

## What was deliberately not removed

- Reseller Management: highly relevant to wholesale/reseller-based stores.
- FIFO and expiration tracking: particularly useful for stores handling vegetables, food, or other expiring goods.
- Stock adjustments and physical counts: important for spoilage, damage, loss, and reconciliation.
- Detailed reports: still available, but kept behind progressive disclosure.

## Data preservation when modules are hidden

Turning off a specialized module hides its workflow but does not delete its existing demo records. This prevents a usability preference from becoming a destructive data action. Re-enabling the feature restores access to the saved demo information.
