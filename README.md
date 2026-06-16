# Universal Theme 26.1 Reference

This is a custom version of the Original Oracle APEX App which I have modified to:
- Implement as features from the APEX Advisor Scanner as possible
- Adjusted components with the upgrade feature
- Changed the theme to Iris
- Run the APEX Object dependencies for errors
- Add help and accessibility markers

Universal Theme 26.1 Reference is an Oracle APEX sample application that demonstrates how to build, style, and inspect applications using Oracle APEX Universal Theme. Its goal is to provide a runnable reference for theme capabilities, page templates, regions, reports, lists, navigation patterns, utility classes, icons, JavaScript APIs, and migration guidance.

This application is built for Oracle APEX 26.1 and Universal Theme 26.1. It runs in an Oracle APEX workspace on an Oracle Database version supported by APEX 26.1, and the parsing schema must be able to create tables, triggers, views, and procedures. The supporting-object installer expects at least 100 KB of free schema space and creates sample data used by charts, cards, and map pages.

## What Does the App Do?

The app acts as a live Universal Theme catalog. The Getting Started area introduces Universal Theme and links into the main topic areas, while the Design section explains layout, colors, theme styles, navigation, mobile patterns, and page template choices.

The Components section demonstrates APEX UI building blocks in working pages. It includes examples for regions, reports, lists, forms, buttons, calendars, charts, maps, dialogs, drawers, tabs, cards, media lists, timelines, comments, badges, avatars, and other common interface patterns.

Many pages include configuration, instructions, sample SQL, and preview regions so developers can compare template behavior and template options directly in the browser. Supporting demo tables provide realistic sample data for charts, task timelines, card layouts, and airport map visualizations.

The Reference area collects developer-oriented utilities, including the Button Builder, JavaScript event and API references, CSS utility classes, CSS variables, content and layout modifiers, template directives, and a change log for Universal Theme releases.

The app is also configured as an installable Progressive Web App and includes application shortcuts for Getting Started, Design, Components, Icons, and Reference.

## Page Map

- Page 0: Page Zero
- Page 100: Redirect
- Page 300: Grid Layout
- Page 400: Design
- Page 401: Design Overview
- Page 402: Colors
- Page 405: Theme Styles
- Page 407: Navigation
- Page 421: Navigation
- Page 422: Headers and Footers
- Page 423: Data Entry
- Page 424: Touch Gestures
- Page 425: jQuery Mobile Components
- Page 500: Getting Started
- Page 700: Layout
- Page 1100: Pages
- Page 1101: Standard Page Template with Side Navigation
- Page 1102: Standard Page Template with Top Navigation
- Page 1103: Left Column Page with Side Navigation
- Page 1104: Left Column Page with Top Navigation
- Page 1105: Right Column Page with Side Navigation
- Page 1106: Right Column Page with Top Navigation
- Page 1107: Marquee Detail Page with Side Navigation
- Page 1108: Marquee Detail Page with Top Navigation
- Page 1109: Side Columns Page with Side Navigation
- Page 1110: Side Columns Page with Top Navigation
- Page 1111: Standard Dialog Page
- Page 1112: Wizard Dialog Page
- Page 1113: Minimal Page Template
- Page 1114: Login Page Template
- Page 1115: Standard Page Template with Tabs Navigation
- Page 1116: Sticky Mobile Header
- Page 1117: Sticky Mobile Footer
- Page 1120: Navigation Menu - Menu Bar Preview
- Page 1121: Navigation Menu - Tabs Preview
- Page 1122: Navigation Menu - Mega Menu Preview
- Page 1123: Navigation Menu - Side Tree Navigation Preview
- Page 1124: Navigation Menu - Mega Menu Preview 2
- Page 1201: Regions - Standard
- Page 1202: Region - Alert
- Page 1203: Region - Hero
- Page 1204: Region - Button Container
- Page 1205: Region - Carousel
- Page 1206: Region - Collapsible
- Page 1207: Region - Title Bar
- Page 1208: Region - Wizard
- Page 1209: Content Block
- Page 1210: Region Image
- Page 1250: Button Container
- Page 1301: Lists - Media List
- Page 1303: Lists - Links
- Page 1304: List - Badges
- Page 1305: List - Menu Bar
- Page 1306: Menu Popup
- Page 1307: Contextual Info
- Page 1401: Reports - Standard
- Page 1402: Reports - Interactive Report
- Page 1403: Value Attribute Pairs
- Page 1405: Reports - Comments
- Page 1406: Reports - Timeline
- Page 1407: Reports - Content Row
- Page 1410: Interactive Grid
- Page 1411: Reports - Faceted Search
- Page 1412: Reports - Smart Filters
- Page 1413: Reports - Search Region
- Page 1500: Buttons
- Page 1600: Forms
- Page 1601: Form Item Types
- Page 1700: List View
- Page 1701: Region - List View Mobile Example
- Page 1710: Reflow Report
- Page 1711: Reflow Report - Mobile Examples
- Page 1720: Column Toggle Report
- Page 1721: Column Toggle Report - Mobile Examples
- Page 1800: Calendars
- Page 1901: Tree
- Page 1902: Charts
- Page 1903: Help Text
- Page 1905: Static Content
- Page 1906: Map
- Page 1907: Tabs
- Page 1908: Dynamic Content Region
- Page 1909: Redirect
- Page 1910: Page Dialog
- Page 1911: Inline Dialog
- Page 1912: Modal Dialog Demo
- Page 1913: Modal Dialog Demo - Fixed Size
- Page 1914: Modal Dialog Demo - Fit Window
- Page 1915: Inline Popup
- Page 1916: Inline Drawer
- Page 1917: Page Drawer
- Page 1918: Drawer Demo
- Page 1919: Drawer Demo - Fixed Size
- Page 1920: Step 1
- Page 1921: Step 2
- Page 1922: Step 3
- Page 1923: Region Display Selector
- Page 2000: Migration Guide
- Page 3000: Components
- Page 3001: Components - Avatar
- Page 3002: Components - Badge
- Page 3003: Components - Comments
- Page 3004: Components - Content Row
- Page 3005: Components - Media List
- Page 3006: Components - Timeline
- Page 3007: Components: Metric Card
- Page 3008: Components - Flexbox Container
- Page 3100: Card Templates
- Page 3110: Card Regions
- Page 3810: Breadcrumb
- Page 4000: Icons
- Page 6000: Reference
- Page 6100: Button Builder
- Page 6200: JavaScript Events
- Page 6201: JavaScript APIs
- Page 6302: Color and Status Modifiers
- Page 6303: Layout Modifiers
- Page 6304: Content Modifiers
- Page 6305: Change Log
- Page 6307: CSS Variables
- Page 6400: Template Directives
- Page 9999: Login Page

## Supporting Objects

### Installed Objects

- `EBA_UT_CHART_PROJECTS`
- `EBA_UT_CHART_TASKS`
- `EBA_UT_DEMO_CARDS`
- `EBA_UT_MAP_AIRPORTS`
- Triggers for generated IDs and audit-style metadata on the chart and card demo tables
- Seed data for chart projects/tasks, demo cards, and airport map points

### Install Scripts

- `supporting-objects/install-scripts/create-tables.sql`: creates `EBA_UT_CHART_PROJECTS`, `EBA_UT_CHART_TASKS`, `EBA_UT_DEMO_CARDS`, related triggers, indexes, and sample chart/card data.
- `supporting-objects/install-scripts/create-airports-table.sql`: creates `EBA_UT_MAP_AIRPORTS` and loads airport location data using `MDSYS.SDO_GEOMETRY`.

### Upgrade Scripts

- `supporting-objects/upgrade-scripts/add-cards-demo-table-and-data.sql`: adds `EBA_UT_DEMO_CARDS` and seed data when the table does not already exist.
- `supporting-objects/upgrade-scripts/add-map-airports.sql`: adds `EBA_UT_MAP_AIRPORTS` and airport map data when the table does not already exist.

### Deinstall

- `supporting-objects/deinstall-script.sql`: drops `EBA_UT_CHART_PROJECTS`, `EBA_UT_CHART_TASKS`, `EBA_UT_DEMO_CARDS`, and `EBA_UT_MAP_AIRPORTS` with cascade constraints.
