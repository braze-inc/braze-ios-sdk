## 3.32.0

##### Added
- Adds Mac Catalyst support for apps integrating with Swift Package Manager (SPM).
  - Please follow [the instructions here](https://www.braze.com/docs/developer_guide/platform_integration_guides/ios/initial_sdk_setup/swift_package_manager/) to import the SDK with SPM. The SDK does not currently support Mac Catalyst when integrated through Cocoapods or Carthage.
  - To add Mac Catalyst support, update the `Run Script Action` described in the [3.31.0 section of the Changelog](#3310).
    - Replace the existing script with the following:
      ```
      # iOS
      bash "$BUILT_PRODUCTS_DIR/Appboy_iOS_SDK_AppboyKit.bundle/Appboy.bundle/appboy-spm-cleanup.sh"
      # macOS
      bash "$BUILT_PRODUCTS_DIR/Appboy_iOS_SDK_AppboyKit.bundle/Contents/Resources/Appboy.bundle/appboy-spm-cleanup.sh"
      ```

## For all versions before 3.32.0, please reference the repo below:
https://github.com/Appboy/Appboy-ios-sdk
