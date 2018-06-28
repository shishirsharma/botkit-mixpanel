# Botkit Mixpanel Analytics

This module enables the basic Mixpanel analytics.

```
npm install --save botkit-mixpanel
```

Add the following to your code AFTER you initialize your Botkit controller:

```
var controller = Botkit.slackbot();
require('botkit-mixpanel')(controller,  {mixpanel_api_key: process.env.MIXPANEL_API_KEY, debug: true, always_update: true});
```

## Options

Enable debug output:

```
require('botkit-mixpanel')(controller,  {mixpanel_api_key: process.env.MIXPANEL_API_KEY, debug: true, always_update: true});
```

By default, this module will only send user profile and bot instance information
the _first time_ an event is received.  To update this information _every time_ an event is received, include the `always_update` option:

```
require('botkit-mixpanel')(controller,  {mixpanel_api_key: process.env.MIXPANEL_API_KEY, debug: true, always_update: true});
```

## Data collection

With this module installed and enabled, your Botkit application will automatically
send a copy of any message your bot receives to Mixpanel's analytics
API, as well as user profile information.

Where applicable, ensure that your terms of service and privacy policy reflect this data collection.
