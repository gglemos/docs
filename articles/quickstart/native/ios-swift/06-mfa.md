---
title: Multifactor Authentication
description: This tutorial will show you how to configure Multi Factor Authentication (MFA) via Google Authenticator in your app.
budicon: 243
---

<%= include('../../../_includes/_package', {
  org: 'auth0-samples',
  repo: 'auth0-ios-swift-v2-sample',
  path: '06-MFA',
  requirements: [
    'CocoaPods 1.1.1',
    'Version 8.2 (8C38)',
    'iPhone 6 - iOS 10.2 (14C89)'
  ]
}) %>

## Enable Multifactor Authentication In Your Account

Multifactor authentication can be enabled with the flip of a switch with Auth0. Go to the [MFA section](${manage_url}/#/multifactor) of your dashboard and flip the switch on for **Google Authenticator** under the *Choose a Provider* section.

You must specify which clients you want to enable MFA for. This can be done by editing the snippet that appears below, replacing the placeholder with your actual client IDs.

![MFA Rule Screenshot](/media/articles/mfa/mfa-native/mfa-native-02.png)

If you want to use MFA in **all** of your clients, the easiest you can do is disabling this conditional in the script:

```javascript
if (CLIENTS_WITH_MFA.indexOf(context.clientID) !== -1)
```

> For more information on how to configure Lock in your app, take a look at the [login tutorial](01-login).
