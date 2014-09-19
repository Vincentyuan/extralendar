extralendar
===========

Google app script for automatic export of the extranet calendar to google calendar.

# Disclaimer
> This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY expressed or implied. **Use it at your own risk**.

> You can only use this program with valid credentials.

# Installation

To make this script run, you must go through some really basic steps:

1. Create a google calendar
2. Create the Google script
3. Add an execution trigger


## Google calendar

1. Go to your [Google Calendar ](https://www.google.com/calendar/render)
2. Create a new calendar
3. Get its id  

[Looking for help about Google Calendar ?](https://support.google.com/calendar/?hl=fr#topic=3417969)

## Script

1. Copy the content of the script: [Script.gs](https://github.com/nobe4/extralendar/blob/master/Script.gs)
2. Paste it in a Google Script: [here](https://www.google.com/script/start/)
3. Complete these fields:
  * ADDRESS: the extranet front page address
  * USERNAME: your extranet username
  * PASSWORD: your extranet password
  * CALENDAR: your calendar id (check Google Calendar Step)
4. Test if the script is working by executing the main function
5. Authorize the script to access your calendars

[Looking for help about Google Script ?](https://developers.google.com/apps-script/overview)

## Time Trigger

1. Go to Resources > Current project's triggers
2. Add one trigger
3. Execute *main* every 30 minutes

[Looking for help setting the trigger ?](https://developers.google.com/apps-script/guides/triggers/installable?hl=de#managing_triggers_manually).

## Contact us

You followed this guide and you still need help, or you find a bug ?
Just submit an issue on this repo !

# Parameters

All the parameters can be found in the const part.
``` javascript
// -------------------------- CONST ----------------------------
var LOG_LEVEL = 1;
var ADDRESS = "";
var USERNAME = "";
var PASSWORD = "";
var CALENDAR = "";
var STEP = 14;
```

* LOG_LEVEL: define the verbosity of the script
 * 1: Only fatal errors
 * 2: Basic function return
 * 3: High verbosity, debug only
 * 
* ADDRESS: extranet front page address
* USERNAME: your username
* PASSWORD: your password
* CALENDAR: your calendar
* STEP: the number of days you want to fetch in one time

# How does it work ?

``` javascript
function doLogin(){
  // fetch user informations used to get calendar infos
  // 1/ get a session id
  // 2/ use it with the payload to get the db_extranet cookie
  // 3/ return the two cookies
}
```

``` javascript
function fetchExtranet(){
  // use previously fetched cookie info to query the extranet and get the calendar bewteen the two dates
  // 1/ insert all infos into a request
  // 2/ return the request response
}
```
