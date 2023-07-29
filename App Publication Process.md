# App Publication Process

## Prerequisite

You need the following registered accounts, the same one used in development machine setup:
- Apple ID
- Google Account

Depending on which platform you want to publish, you will need to have an active Google Play Developer and/or an active Apple Developer Program membership.
You can also be a member of an organization with active memberships and publish under their behalf. If that is the case, make sure you have the necessary permission to create and publish a new application.

## Apple App Store Publication

If you have not experienced publishing a mobile app before, this process can be daunting.

### Register New Identifier

Follow this article (https://developer.apple.com/help/account/manage-identifiers/register-an-app-id/).
- Enable push notification capabilities

### Create New App Record
Follow this article (https://developer.apple.com/help/app-store-connect/create-an-app-record/add-a-new-app). The Apple developer portal has a lot of help panels/bubbles, it is highly recommended to read through them.
- Platform should only be `iOS`

To archive and upload the app to Apple, follow the relevant section at (https://github.com/opentourbuilder/guide/blob/main/README.md).

## Google Play Store Publication

If you have not experienced publishing a mobile app before, this process can be daunting. This article can help you understand the general process of publishing to Google Play Store (https://medium.com/@the_manifest/how-to-publish-an-app-on-google-play-a-step-by-step-guide-80f9f533e370). Note that you do not have to do anything regarding monetization since the app is free. Additionally, Google has an entire knowledgebase to guide you through step-by-step (https://support.google.com/googleplay/android-developer/answer/9859152?hl=en). You can proceed to the next article in the series via the right-side navbar.

The high-level overview of the process is as follows:
1. After you've created your Google Play developer account, you can create apps and set them up using Play Console.
2. After you create your app, you can start setting it up.
    - Your app’s dashboard will guide you through all the most important steps to get your app available on Google Play.
    - You’ll start by providing details about your app’s content, and entering information for your Google Play store listing.
3. After that, you can move onto app release; this guides you through pre-release management, and testing.
4. The final step is launching your app on Google Play.

During the publication process, you should follow these recommended options:
- New app should be `App` as opposed to `Game`
- App should be `Free`
- App category should be `Travel & Local`

To build a signed release bundle, follow the relevant section at (https://github.com/opentourbuilder/guide/blob/main/README.md).