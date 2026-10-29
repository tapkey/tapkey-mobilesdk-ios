# Tapkey MobileSDK for iOS

The Tapkey Mobile SDK for iOS and watchOS as a Swift package. For the
integration, see the documentation at
[developers.tapkey.io](https://developers.tapkey.io/mobile/ios/getting_started/).

## Requirements

- iOS 15.6 or later, watchOS 9.0 or later.
- Add `-ObjC` to **Other Linker Flags** of every app target that uses the SDK.
  The SDK creates some of its classes by name. Without the flag, the linker
  leaves them out: the app builds and runs, but the SDK fails when it needs
  them, for example when it decodes keys after login.

For push notifications, also add the `tapkey-mobilesdk-fcm-ios` package.

## Known limitations

- In the watchOS Simulator, the SDK supports only Apple silicon (arm64). If
  your build also builds x86_64 for the watchOS Simulator, for example a build
  for "Any watchOS Simulator Device", exclude it in your app target:
  `EXCLUDED_ARCHS[sdk=watchsimulator*] = x86_64`.

## Versions

The tag is the SDK version without its fourth component: SDK `2.53.2.0` is
tag `2.53.2`.

## License

Copyright (c) Tapkey GmbH, see [LICENSE](LICENSE).
