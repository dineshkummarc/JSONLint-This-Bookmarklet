# JSONLint This bookmarklet | Joss Crowcroft
Click this bookmarklet to reformat (pretty-print) and validate/debug a block of JSON code or unformatted JSON API response. If JSON is valid, it is pretty-printed into a readable format - if it's invalid, you get a handy console message telling you how to fix it. Hit 'escape' to exit/cancel.

Super handy for checking out API responses and large blocks of JSON data on-the-fly.

Uses [JSONLint.js](https://github.com/zaach/jsonlint) by Zach Carter and [Simple JavaScript DOM Inspector](https://github.com/josscrowcroft/Simple-JavaScript-DOM-Inspector) by Joss Crowcroft

No warranty; probably won't break the internet, this time. Improvements and comments welcome!

**NB:** In this repository, the bookmarklet code will always be the latest version of the unminified code.

## Example

Click the bookmarklet to select the element containing JSON data (needs to be `white-space:pre`, currently). Click it to turn something like this:

```
{"widget":{"debug":"on","window":{"title":"Sample Konfabulator Widget","name":"main_window","width":500,"height":500},"image":{"src":"Images/Sun.png","name":"sun1","hOffset":250,"vOffset":250,"alignment":"center"}}}
```

... into something like this:

```
{
    "widget": {
        "debug": "on",
        "window": {
            "title": "Sample Konfabulator Widget",
            "name": "main_window",
            "width": 500,
            "height": 500
        },
        "image": {
            "src": [...]
```

### Error/debug messages:

Debug messages for invalid JSON appear in the console like this:

```
Error: Parse error on line 1:
...lignment":"center"}}
-----------------------^
Expecting '}', ','
```

## Demo

Check out the **[JSONLint This bookmarklet demo](http://www.josscrowcroft.com/demos/jsonlint-this/)**

## Changes

### 0.2.1
* Uses `Error.toString()` so that Chrome doesn't show error debugging info in console
* Uses `console.warn` instead of `console.error` for validation errors

### 0.2
* Updated jsonlint.js to version 1.2.0

### 0.1
* First version