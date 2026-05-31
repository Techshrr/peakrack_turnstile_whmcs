# Changelog

All notable changes to this project are documented in this file.

This project follows Semantic Versioning where practical.

## [1.4.8] - 2026-06-01

### Added

- Added a WHMCS admin-area GitHub shortcut and browser-side update notice for published GitHub releases or tags.

### Changed

- Load the Turnstile API with an explicit onload callback and a Cloudflare Rocket Loader bypass.
- Reduce client-side refreshes caused by Turnstile iframe DOM mutations.

### Fixed

- Added limited widget reset recovery for Turnstile timeout and error callbacks.
- Stopped rendering the saved Turnstile Secret Key back into the WHMCS addon settings form.
- Preserved the existing Secret Key when the settings form is saved with that field left blank.
- Replaced the admin GitHub shortcut icon with inline SVG and adjusted the header actions so the version, repository, and language controls stay inside the panel.

## [1.4.7] - 2026-05-21

### Fixed

- Improved Turnstile placement across Lagom, Nexus, Six, Twenty-One, Standard Cart, Nexus Cart, and Lagom checkout layouts.
- Added DOM mutation handling for dynamically rendered cart and checkout forms.
- Improved token synchronization and removed reliance on deprecated jQuery trim helpers.

## [1.4.6] - 2026-05-21

### Fixed

- Added `cf-turnstile-response` to checkout-page existing customer login AJAX requests.
- Returned JSON for `/login/cart` captcha failures instead of redirecting to `login.php?error=captcha`.
- Prevented hidden checkout login containers from placing a widget in the complete-order area.

## [1.4.5] - 2026-05-21

### Fixed

- Fixed the WHMCS addon title to `PeakRack Turnstile Manager`.
- Stabilized the top-right version badge and language switch layout.

## [1.4.4] - 2026-05-21

### Added

- Added a Chinese and English admin language switch.
- Localized the main manager UI text.

## [1.4.1] - 2026-05-21

### Added

- Added global frontend alignment options for center or left placement.

### Fixed

- Improved placement consistency across Nexus, Six, Twenty-One, and Lagom/Lagom2 pages.

## [1.0.0] - 2026-05-21

### Added

- Initial release.
- Added Turnstile injection and server-side validation for selected WHMCS client-area forms.
