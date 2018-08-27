# General for information.

Here are listed changes for (1) Javascript API, (2) Browser extension and (3) native chromehost installation. 

## 1/3 Javascript API changes :

2.0 Added/changed the following
* Added typescript definitions `jabra.browser.integration-2.0.d.ts` of API for detailed documentation, static checking and better IDE support. *Tip: Use the typescript file with a [reference path comment](https://www.typescriptlang.org/docs/handbook/triple-slash-directives.html) on top of your javascript files to get code completion for the Jabra API in many development tools.* 
* Modern ES5+ promisified Javascript API - All methods now return values using [Javascript promises](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise) rather than callbacks in order to enabled streamlined testing and API usage. This means for instance, the `init()` method now returns a JS promise that user should use then()/catch() on to react on initialization **(breaking change)**.
* Individual subscription to event(s) using `addEventListener(nameSpec, callback)` and `removeEventListenernameSpec, callback)` **(breaking change)**.
* Removed requestEnum. Use of individual subscription event handlers (see above) abolish the need for this enumeration **(breaking change)**.
* `getDevices()` now return a JS map with key/values rather than a simple string **(breaking change)**.
* Added `getInstallInfo()` that checks and details the current installation.    
* Added shutdown method (for use in testing).
* Fixed various bugs, incl. a race-condition where incorrect results would be given.
* Added more events including offline, online.
* Added logging to API, browser extension and chromehost executable.
* Added API test example, updated existing examples for new API version.
* All internals are now hidden away so they can't be accessed by accident.

1.2 Added jabra device autodetection.

1.1 Internal release.

1.0 Orginal version with call control support.

## 2/3 Browser extension changes:

2.0 Added the following
* Support for passing complex input/output as needed by new JS API.
* Fixed various bugs, incl. a race-condition where incorrect results would be given.
* Support for new getInstallInfo command.
* Added logging support, configurable using new UI.

0.5 Orginal version with call control support.

## 3/3 Chome host changes:
2.0 Added the following:
* Logging to files similar to native SDK.
* Support for more complex input/output needed by new JS API.
* Support for new getInstallInfo command.
* Fixed various bugs, incl. a race-condition where incorrect results would be given.
* Beta support

0.5 Orginal version with call control support.