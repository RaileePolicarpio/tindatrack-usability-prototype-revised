# TindaTrack Final Prototype Changelog

## Baseline
- Academic stage: **2nd Revision Prototype**
- Internal development version: **Usability Revision 7**
- Preserved Git commit: `f3dab6ecb3089a6475e52720b7cbb071e00f5f6a`

The Final Prototype was created from a separate working copy. The evaluated Revision 7 baseline was not overwritten.

## Final changes

### Mobile UI
- Added real-phone top-bar compaction.
- Removed unintended whole-page horizontal overflow at tested 360 px and 390 px widths.
- Converted the Inventory table into labeled mobile cards at narrow widths.

### Dashboard
- Extended Simple View to the Owner Dashboard.
- Kept essential daily information visible first.
- Hid secondary monthly/specialized information in Simple View.
- Added an immediate Simple/Full Dashboard switch.

### First-use and demo clarity
- Added Demo workspace notice for preloaded sample data.
- Retained and updated the guided first-time tour.
- Updated the Simple View explanation to cover both Dashboard and Inventory.

### Interaction consistency
- Replaced the icon-only desktop theme shortcut with a labeled Dark/Light control.
- Replaced arbitrary product image/icon selection with category-controlled illustrations.

### Landing page and research integrity
- Replaced free-trial/commercial wording with prototype/demo wording.
- Added business-context chips to strengthen TindaTrack's small-store identity.
- Removed fictional-looking testimonial names and quotations.
- Replaced them with a truthful usability-testing/design-direction section.
- Changed the former Pricing section into a Demo section.


### Contextual guided onboarding
- Replaced the text-only tour with a spotlight-based guided walkthrough of the real interface.
- Added a 12-step Owner tour and 10-step Reseller tour.
- Tour steps automatically navigate to the relevant screen and highlight the feature being explained.
- Added short practical tips, progress indicators, Back/Next/Exit controls, and replay from Settings.
- Added an explicit demo-data tutorial step to reduce confusion caused by preloaded records.
- Kept each step short to avoid replacing one form of information overload with another.

### Additional information-density refinement
- Simple Dashboard now shows at most the top three Needs Attention alerts; the full list remains available through View all.

### Landing identity and restrained effects
- Added subtle low-opacity store-management motifs to the landing hero.
- Added restrained hover/focus transitions and a short tutorial spotlight pulse only where motion communicates interactivity or attention.
- Added `prefers-reduced-motion` support so optional motion is minimized for users who request it.

## Deliberately retained
The Final Prototype does not redesign validated navigation or remove specialized workflows that were useful to particular target users. Owner/Reseller operations, FIFO/expiration support, Customer Credit, Reports, Archive/restore, expenses, and optional module behavior remain intact.

## Deferred beyond the prototype
- Real server authentication
- Cloud synchronization
- Full offline transaction synchronization
- Production audit identities/signatures
- Production-grade security, performance, and scalability validation


## Finalization
- The final pre-submission build was promoted to the official Final Prototype after the complete tutorial, responsive, workflow, and regression QA suites passed.
- Development-only Candidate wording was removed from the submission build.
- A fresh browser-local storage namespace is used for the official build so older prototype data cannot conflict with the submission version.
