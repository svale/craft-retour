# Retour Changelog

## 3.1.10 - 2018.04.18
### Changed
* Make sure the URL we redirect to is a full URL, and is based on the defined `siteUrl`
* Migration for Retour widgets
* Added a **Dashboard Refresh Interval** control to let people choose the refresh interval (or disable it)
* Ensure the user has permission for a given site to be able to edit redirects for it

## 3.1.9 - 2018.04.09
### Changed
* Fixed an issue where an empty **Exclude Patterns** table and the use of Project Config on Craft 3.1 or later could cause an exception to be thrown when a 404 is thrown

## 3.1.8 - 2018.04.02
### Added
* Added the ability to exclude URIs from Retour completely via a series of RegEx

### Changed
* If Preserve Query String is on, make sure the path `p=` isn't part of it
* Don't log stats update errors, because it's pointless, and can report meaningless deadlock errors
* Ensure that a user has permission to access a site group to redirect something to it
* Fixed an issue where automatic redirects based on renamed entries didn't create the redirect for the right `siteId` in multi-site setups

## 3.1.7 - 2018.03.20
### Changed
* Fixed an issue with pagination of statistics and redirects when limiting them to a specific site
* Don't allow editing of the plugin settings if `allowAdminChanges` is false
* Record the user IP instead of Proxy IP
* Disable "Redirect To" link when there is a token in the destination url
* Display an error when a redirect is not saved because it'd create a redirect loop

## 3.1.6 - 2018.02.04
### Changed
* Reverted the semver on `league/csv` back to `^8.2` due to incompatible APIs
* Fixed an issue with a missing Dashboard icon

## 3.1.5 - 2018.01.23
### Changed
* Updated the semver on `league/csv` to `^8.2|^9.1`

## 3.1.4 - 2018.01.18
### Changed
* Fixed the breadcrumbs in the CP to respect the currently selected site

## 3.1.3 - 2018.01.10
### Changed
* Fixed an issue where the live reload of 404 data would cause the pagination to reset to viewing the first page

## 3.1.2 - 2018.01.03
### Changed
* Register cache options for every type of request
* Added `beforeSaveRedirect` and `beforeSaveRedirect` events for plugin/module or [Webhooks](https://github.com/craftcms/webhooks) plugin use

## 3.1.1 - 2018.12.19
### Changed
* For multi-site setups, auto-create slug redirects for the element's site only
* Fixed a minor JavaScript issue visible only in `webpack-dev-server`
* Updated the PostCSS build packages & config

## 3.1.0 - 2018.12.17
### Added
* Added the ability to have true multi-site capabilities, with redirects that only affect specific sites
* Added live refresh of the Dashboard data

## 3.0.18 - 2018.11.23
### Changed
* Fixed an issue with the charts controller for the Widget charts on Postgres
* Fixed an issue in Statistics.php with Postgres

## 3.0.17 - 2018.11.05
### Changed
* Fix missing welcome icon

## 3.0.16 - 2018.11.04
### Changed
* Fixed an issue with `trimStatistics()` if you're using Postgres
* Retooled the JavaScript build system to be more compatible with edge case server setups

## 3.0.15 - 2018.10.29
### Changed
* Handle a Retour return status > 400 to render the actual error template
* Fixed a console error in the Dashboard if no data was returned for a chart
* Updated the build system

## 3.0.14 - 2018-10-18
## Added
* Added the recording of the **User Agent**, **Message**, **File Name**, and **Line No.** for each 404 exception via hovering over the 404 URL
* Added a **Preserve Query String** option to the Settings to allow the query string be preserved and passed along to the redirected URL
* Added the ability to set whether redirects are **Enabled** or not, without deleting them

## 3.0.13 - 2018-10-17
### Changed
* Fixed an issue where the charts wouldn't generate properly if you were using MySQL 5.7 or later
* Fixed an issue with the charts not generating properly if you were using Postgres
* Fixed a padding issue with the widget chart

## 3.0.12 - 2018-10-14
### Added
* Added the ability to redirect based on **Path Only** or **Full URL**, to allow for site-specific redirects
* Added **Legacy URL Match Type** and **Remote IP** to the import and export fields

### Changed
* Trimmed the database tables to be more storage space efficient

## 3.0.11 - 2018-10-13
### Added
* Added **Remote IP** to the Dashboard statistics, with a link to look up a geo-location
* Added config setting for **Record Remote IP**

### Changed
* Fixed an issue where the search function wouldn't work in the Control Panel if you were using Postgres
* Fixed incorrect links to the documentation
* Fixed an issue where a user with the proper permissions could not save a new redirect
* Fixed the build process so it will no longer look for `devServer` on installs

## 3.0.10 - 2018-10-05
### Changed
* Updated build process

## 3.0.9 - 2018-09-24
### Changed
* Modernized package.json and webpack build

## 3.0.8 - 2018-09-20
### Changed
* Fixed a regression that caused you to be unable to click on a redirect to edit it
* Added automatic manifest cache invalidation

## 3.0.7 - 2018-09-19
### Added
* Added a `retour/stats/trim` console command to manually trim the statistics table

### Changed
* Added an **Automatically Trim Statistics** option (defaults to `true`) in Settings and `config.php`

## 3.0.6 - 2018-09-18
### Changed
* Fixed an issue when creating new redirects on a Postgres database
* Fixed a cosmetic issue where RegEx's with a `|` in them were not displayed correctly in the table
* Fixed an issue where the `+` add button didn't work right on some configurations

## 3.0.5 - 2018-09-14
### Changed
* Fixed an error with multi-site when an element existed on one site, but not the main site

## 3.0.4 - 2018-09-13
### Changed
* Fixed an issue where RegEx redirects would have the Destination URL overwritten by the parsed result after a hit
* Fixed an issue where cached resolved redirects would not increment statistics

## 3.0.3 - 2018-09-13
### Added
* Added documentation for User Group based Permissions in Retour

### Changed
* Fixed an issue with line endings for CSV files that were generated by Mac computers

## 3.0.2 - 2018-09-12
### Changed
* Fixed issues with the `+` and `x` URLs in the Control Panel not working as intended

## 3.0.1 - 2018-09-12
### Changed
* Fixed the CSV importer to it imports more than just the first entry in the CSV

## 3.0.0 - 2018-09-12
### Added
* Initial release
