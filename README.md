# TindaTrack Revised Working Prototype - Usability Revision 6

A responsive store-management prototype for sari-sari stores and other small retail businesses, including wholesalers, vegetable stores, school-supply retailers, and businesses that distribute products through resellers.

## Demo accounts

### Owner Demo
- Email: `owner@tindatrack.ph`
- Password: `owner1234`

### Reseller Demo
- Email: `reseller@tindatrack.ph`
- Password: `reseller1234`

The Owner controls the master product catalog, central inventory, stock-in, suppliers, product allocation, and overall reseller oversight. The Reseller operates a limited storefront using only stock assigned by the Owner.

## How to open

Open `index.html` in a modern browser, or run a local server:

```bash
python -m http.server 8000
```

Then open the local address shown by Python in your browser.

## Revision 6 highlights

### Operational reseller account
The reseller account is now an active store-operation account rather than a read-only portal.

Resellers can:
- Run **New Sale** using only their assigned stock.
- Accept Owner-enabled payment methods: Cash, GCash, and/or Customer Credit.
- Maintain **My Customers**.
- Record customer credit, due dates, payments, and completed credit history.
- View **My Stock** with received, sold, returned, damaged/lost, pending, and available quantities.
- Record their own operating expenses.
- View their own sales history, reports, estimated profit, and balance to the Owner.
- Export their own reports to Excel-compatible format and Print/Save as PDF.
- Request product returns.
- Report damaged, lost, spoiled, or other stock issues for Owner approval.
- Receive role-specific notifications and a short reseller tutorial.

### Owner oversight
The Owner can:
- View all reseller stock, sales, customer credit, reseller expenses, balances, pending requests, and transaction history.
- Release Store Stock to a reseller without treating the release as an end-customer sale.
- Set a **Reseller Cost** and **Minimum Selling Price**. The reseller may sell above the minimum but not below it.
- Configure each reseller as **Wholesale** or **Consignment**.
- Configure Cash, GCash, and Credit availability per reseller.
- Configure reseller sale notifications as **Grouped**, **Immediate**, or **Off**. Grouped is the default.
- Approve or reject reseller return requests and stock-issue reports.
- Optionally display reseller estimated profit in Owner reports.
- Preview a reseller account while remaining in the Owner session.

### Wholesale and consignment rules
- **Wholesale:** the reseller's balance to the Owner increases when stock is released.
- **Consignment:** the reseller's balance to the Owner increases when the reseller records a sale.
- For a consignment sale made on customer credit, the reseller still owes the Owner once the product is recorded as sold. Customer debt to the reseller and reseller debt to the Owner are tracked separately.

### Inventory authority
- The Owner alone manages the master inventory, Add/Edit Product, Stock-in, suppliers, Archive, central reconciliation, and FIFO configuration.
- A reseller receives a separate **My Stock** view containing only products allocated by the Owner.
- Reseller sales reduce Reseller Stock, not Store Stock a second time.
- Returns only move back to Store Stock after Owner confirmation.
- Stock issues only reduce official reseller stock after Owner approval.

### Owner reports and accounting clarity
- Direct Store Sales and Reseller Retail Sales are shown separately in Owner reporting.
- Reseller retail revenue is not mixed into the Owner's direct-store estimated profit.
- Reseller financial and customer activity remains visible through the Resellers report and reseller details.

## Revision 5 functionality retained

- Dedicated Reseller Management and stock allocation.
- Spoiled, expired, damaged, lost, personal-use, and inventory-correction adjustments.
- Physical inventory reconciliation with an audit trail.
- Simple inventory by default with optional Batch/FIFO tracking.
- Optional per-product expiration tracking and configurable expiration alerts.
- Needs Attention dashboard design with optional reseller and expiration summaries.
- Flexible Expense categories and payment methods.
- Simplified Reports with detailed reports on demand.
- Supplier purchase history.
- Business Feature toggles to reduce visual overload.
- Softer Dark Mode, responsive mobile/desktop layouts, and inventory action tooltips.
- Automatic Archive behavior when all tracked stock reaches zero.
- Restore through Stock-in and preserved Customer Credit History.

## Offline scope

This remains an online usability prototype. True offline operation is intentionally not simulated because a production implementation would require local transaction queues, multi-device synchronization, conflict resolution, and secure server-side persistence.

## Prototype limitation

This is a school usability prototype. Data and authentication are stored only in the current browser using `localStorage`. It does not implement real server authentication or cloud synchronization. Use demo information only.
