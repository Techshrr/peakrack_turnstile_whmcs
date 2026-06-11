# Upgrade Guide

This guide explains how to upgrade this module from an older version.

## Before upgrading

1. Back up the WHMCS files.
2. Back up the WHMCS database.
3. Make a copy of `modules/addons/peakrack_turnstile/`.
4. Review [CHANGELOG.md](CHANGELOG.md).
5. Check whether the upgrade includes configuration changes.

## Upgrade steps

1. Download the latest release from the official repository:

   https://github.com/Techshrr/whmcs_peakrack_turnstile

2. Replace the addon files in:

   `modules/addons/peakrack_turnstile/`

3. Keep the existing Cloudflare Site Key and Secret Key in WHMCS addon settings.
4. Log in to the WHMCS admin area.
5. Open **Addons > PeakRack Turnstile Manager** and verify all options.
6. Clear the WHMCS template cache if client-area output does not update.

## Database migrations

This version does not require manual database migration.

## Version-specific notes

### Upgrade from 1.4.8 to 1.4.9

- No breaking changes.
- No manual database migration is required.
- Existing Site Key, Secret Key, page toggles, theme, alignment, and custom selectors are preserved.
- This release fixes a validation issue where WHMCS admin-area client profile saves could be blocked by Turnstile registration validation.
- After upload, test saving a client profile in the WHMCS admin area and test the public registration page if registration protection is enabled.

### Upgrade from 1.4.7 to 1.4.8

- No breaking changes.
- No manual database migration is required.
- Existing keys, page toggles, theme, alignment, and custom selectors are preserved.
- When saving settings, leaving the Secret Key field blank keeps the existing saved key.
- The addon admin page now includes a GitHub shortcut and a browser-side update notice. No server-side migration is required for this admin display.
- If the client-area widget does not update immediately after upload, clear the WHMCS template cache and browser cache before retesting.

### Upgrade from 1.4.x to 1.4.7

- No breaking changes.
- Existing keys, page toggles, theme, alignment, and custom selectors are preserved.

## Rollback

To roll back:

1. Restore the previous `modules/addons/peakrack_turnstile/` directory.
2. Restore the database backup if WHMCS settings were changed.
3. Clear the WHMCS template cache.
4. Check the WHMCS activity log for errors.

## Notes

Do not overwrite production credentials, local configuration files, custom templates, callback secrets, or payment credentials unless the upgrade notes explicitly require it.
