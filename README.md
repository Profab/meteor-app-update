# App Update for Meteor

Control Meteor Hotcode push and gracefully notify the user of an update.

## Current Version
**v1.0.0**

## Configuration

App Update uses the ``Meteor.settings.public.env`` variable to decide whether or not to intercept app updates.

The package uses the following ``env`` strings. ``production``, ``test``, and ``development``

Exmaple settings.json file:
```js
{
  "public": {
    "env": "production"
   }
}
```

Before initializing you can set any of the following settings:

* <b>AppUpdate.reload.settings.enabled</b>: ``true||false`` ``default: true``
* AppUpdate.reload.settings.environments.production: ``true||false`` ``default:true``
* AppUpdate.reload.settings.environments.development: ``true||false`` ``default:true``
* AppUpdate.reload.settings.environments.test: ``true||false`` ``default:false``

To initialize the AppUpdate package:

``AppUpdate.reload.preventReload()``.

## Usage

To notify the user when a new app update is available, simply add the template to your page:

``{{> appUpdatePrompt}}``

## Attribution and Acknowledgements

This package was inspired by the Meteor Package (internal to the WebApp package):

https://github.com/meteor/mobile-packages/tree/master/packages/mdg:reload-on-resume

## License

[MIT](http://choosealicense.com/licenses/mit/) -
Copyright (c) 2014 [Ars Nebula](http://www.arsnebula.com)
