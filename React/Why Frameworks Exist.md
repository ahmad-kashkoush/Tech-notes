# Web Evolution phases

## Server-side Rendering

- Client requests server for website
- Browser paints server code on screen

## Single Page, Client Rendering

> [!error] ISSUE
> is keeping Server data in sync with displayed data

- Pages rendered on the client not server
- No reloading of the page
- [Front End Application Job](Front%20End%20Application%20Job.png)
- Why Can't with JS :dev_javascript_original:?
    - Requires a lot of DOM Manipulation `Spaghetti code`
    - State is Stored in the DOM, Shared Across the app
        - [Race Condition](../../Database/CS50%20SQL/Race%20Condition.md): Multiple functions may change the same data
        - Hard to keep syncing state in all places
- Why Use Frameworks?
    - Keeping UI and state in Sync away from us
    - Well consistent Structure codebase

# Sources

- Udemy |Jonas-Section3| Why Frameworks exist
