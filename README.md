# TindaTrack Revised Working Prototype - Usability Revision 7

Revision 7 is the post-Round-2 usability revision of TindaTrack. It keeps the complete Revision 6 store-management and reseller workflows, while reducing feature clutter and adding clearer first-use guidance for advanced options.

## Demo accounts

### Owner Demo
- Email: `owner@tindatrack.ph`
- Password: `owner1234`

### Reseller Demo
- Email: `reseller@tindatrack.ph`
- Password: `reseller1234`

## How to open

Open `index.html` in a modern browser, or run a local server:

```bash
python -m http.server 8000
```

Then open the local address shown by Python.

## Revision 7 highlights

### 1. Functional Simple View
The previous Simple Mode setting is now **Simple View** and actually changes the Inventory interface.

When Simple View is ON:
- Edit and Stock-in remain directly visible.
- Adjust Stock, Physical Stock Count, Stock History/FIFO Batches, and Archive are grouped under **More**.
- A short note explains why the actions are grouped.

When Simple View is OFF, the full set of inventory action icons is shown.

### 2. Optional modules now hide their related UI
Specialized features no longer leave unnecessary controls visible after they are disabled.

- **Reseller Management OFF:** reseller navigation, dashboard summaries, report cards/tabs/columns, reseller oversight settings, and reseller-specific alerts are hidden from the Owner interface.
- **Expiration Tracking OFF:** expiration product fields, stock-in expiration input, expiration alerts, expiration settings, and expiration-related inventory display are hidden.
- **Batch / FIFO OFF:** inventory-mode controls and FIFO-specific display are hidden; FIFO behavior is disabled while the setting is off.

Existing demo records are preserved when a feature is hidden so they can reappear if the feature is enabled again.

### 3. Clearer advanced inventory guidance
Short plain-language explanations were added to:
- Adjust Stock
- Physical Stock Count
- Stock History / FIFO Batches
- Stock-in when FIFO is enabled

FIFO is explained as using the **oldest received stock first**, while checkout continues to handle it automatically.

### 4. Expense category discoverability
The Add Expense form now keeps the custom-category field hidden until **Custom** is selected. The category field explicitly tells the user to choose Custom if the needed category is not listed.

### 5. Reports adapt to enabled features
The simple Reports summary remains the default. When Reseller Management is disabled, reseller sales cards, reseller report tabs, reseller inventory columns, and reseller data are removed from the Owner reports instead of remaining visible.

### 6. Revised first-time owner tour
The owner tour now explains:
- Everyday tasks first
- Optional store-specific features
- Adjust Stock vs Physical Stock Count
- What FIFO means
- Simplified reports
- Simple View and the More menu

The tour remains skippable and replayable from Settings.

## Revision 6 functionality retained

- Operational Owner and Reseller accounts
- Reseller checkout, customers, credit, expenses, reports, balance, returns, and stock issues
- Wholesale and consignment arrangements
- Owner reseller oversight and preview
- Inventory adjustments and physical reconciliation
- Batch/FIFO inventory and expiration tracking when enabled
- Supplier purchase history and flexible stock-in sources
- Customer Credit History
- Automatic product archive at zero tracked stock and restoration through stock-in
- Simplified reports with detailed reports on demand
- Softer dark mode and responsive desktop/mobile layouts
- Inventory hover tooltips

## Prototype limitation

This is a school usability prototype. Authentication and data are stored only in the current browser using `localStorage`. It does not implement real server authentication, cloud synchronization, or production offline synchronization. Use demo information only.
