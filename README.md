AppCache Extra
================

## Introduction

Meteor's appcache package with the ability to add a prompt when the appcache is reloaded as to avoid the awkward UX experience of having the app just reload out of no where. Also, added is the ability to manually add files to the application cache manifest if you want to serve them yourself.

![demo](http://cl.ly/image/3H2w3J0x3S29/Image%202014-07-07%20at%2011.38.37%20PM.png)

================

## Installation / Setup

##### Package Installation
````
mrt add appcache-extra
````
================

##### Meteor settings file (settings.json)
````
{
  "appcache": {
    "addedFiles": [
      "/cordova.js"
    ]
  },
  "public": {
    "appcache": "prompt"
  }
}
````
###### Options
* appcache.addedFiles: Array of files you want to manually add to application cache manifest
* public.appcache: either propt or doesn't matter.. if prompt it will render the appcache-prompt template instead of auto refreshing the app

================

##### Customization

You can overwrite the `appcache-prompt` template and styling however you would like!

================

## Final Notes

##### Running your app with settings
````
mrt --settings settings.json
````
================

If you want more features than this provides, file an issue. Feature requests/contributions are welcome.
