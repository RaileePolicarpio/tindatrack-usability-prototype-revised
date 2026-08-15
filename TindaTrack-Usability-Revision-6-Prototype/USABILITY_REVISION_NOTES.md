# TindaTrack Usability Revision 6 - Implementation Notes

## Design direction

Revision 6 expands the reseller feature after clarifying that a reseller is not only a person whose stock is monitored. A reseller is an operational user who sells products to their own customers while remaining under the Owner's inventory authority.

The interface still follows the usability principle established from testing: **add the requested capability without showing every specialized function to every user**.

## Role model

### Owner
The Owner controls the master store, including products, Store Stock, Stock-in, suppliers, FIFO settings, Archive, and release of products to resellers. The Owner can monitor reseller activity without needing the reseller's password.

### Reseller
The Reseller receives an assigned inventory called **My Stock**. The reseller can sell those products, manage their own customers and customer credit, record reseller expenses, view their own reports, and report stock issues or request returns.

The Reseller cannot alter the Owner's central inventory or supplier records.

## Inventory flow

Normal allocation and sale:

`Store Stock -> My Stock (Reseller) -> Sold`

Return:

`My Stock -> Pending Return -> Owner confirms -> Store Stock`

Damage/loss/spoilage:

`My Stock -> Stock Issue Report -> Owner approves -> Adjusted Reseller Stock`

A reseller sale does not deduct Store Stock again because Store Stock was already reduced when the Owner released the units.

## Customer credit vs reseller debt

Two balances are intentionally separate:

1. **Customer -> Reseller:** the reseller's customer credit / utang.
2. **Reseller -> Owner:** the reseller's obligation for products received or sold, depending on the arrangement.

For Consignment, the reseller's amount due to the Owner increases when a sale is recorded, even if the end customer selected Credit. This prevents the Owner's receivable from depending on whether the reseller has already collected from their customer.

## Reseller arrangements

- **Wholesale:** Owner receivable is created when stock is released.
- **Consignment:** Owner receivable is created when reseller stock is sold.

Each released product records a Reseller Cost and a Minimum Selling Price. The reseller can choose a customer selling price at or above the minimum.

## Notification strategy

Routine reseller sales can be Grouped, Immediate, or Off. Grouped is the default to avoid notification overload. Important activities such as customer credit, pending returns, and stock-issue reports remain visible to the Owner through reseller oversight and notifications.

Resellers receive only relevant alerts, such as low assigned stock, expiration, overdue customer credit, new stock received, and approval results.

## Accounting presentation

Reseller retail sales are operational data that the Owner may monitor, but they are not automatically the same as the Owner's direct retail revenue. Revision 6 therefore separates **Store Sales** and **Reseller Sales** in Owner summaries and keeps direct-store estimated profit separate from reseller retail profit.

## Offline scope

The prototype remains online-only. Production offline functionality would require secure local persistence, synchronization, conflict resolution, and server-side identity controls, so it is documented as a future enhancement rather than simulated inaccurately.
