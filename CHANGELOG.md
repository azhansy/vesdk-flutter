## [2.3.0]

### Changed

* [imgly_sdk] Removed `WRITE_EXTERNAL_STORAGE` permission request when opening the editor on Android.
* [imgly_sdk] Aligned emoji support for iOS and Android. Emoji support is not optimized for cross-platform use and disabled by default. Added option `TextOptions.allowEmojis`.
* [imgly_sdk] Updated documentation for remote resources used in the editor. Remote resources are usable but not optimized and therefore should be downloaded in advance and then passed to the editor as local resources.

### Added

* [imgly_sdk] Added integration and documentation for custom watermark. Use `Configuration.watermark` to add a custom watermark to the image/video.

### Fixed

* Fixed unexpected behavior when invoking multiple requests.
* [imgly_sdk] Fixed `CompositionOptions.personalVideoClips` would not be resolved correctly on Android.

## [2.2.0]

### Changed

* The img.ly maven repository is no longer automatically added to your Android project by the plugin. Please refer to the new step 3 in the [getting started](https://github.com/imgly/vesdk-flutter#android) section of the README for instructions on how to add it.
* Added support for PhotoEditor SDK and VideoEditor SDK for Android version 9.

### Added

* [video_editor_sdk] Added integration and documentation for force trim.
* [imgly_sdk] Added `TrimOptions.forceMode`, `TrimOptions.minimumDuration` and `TrimOptions.maximumDuration` to configure the force-trimming behavior. 

### Fixed

* [imgly_sdk] Fixed `TrimOptions` not being exposed for `Configuration.trim`.
* [imgly_sdk] Fixed `CompositionOptions.clipTrimOptions` using `TrimOptions` instead of `ClipTrimOptions`.

## [2.1.0]

### Added

* [imgly_sdk] Added `ExportOptions.forceExport` which will force the photo/video to be rendered and exported in the defined output format even if no changes have been applied. Otherwise, the input asset will be passed through and might not match the defined output format.
* [imgly_sdk] Added an interface for native customization on iOS. Set `FlutterIMGLY.configureWithBuilder` to modify the `Configuration` after it has been retrieved from the plugin.
* [photo_editor_sdk] Added support to replace the `PhotoEditViewController` with custom subclasses on iOS.
* [photo_editor_sdk] Added `FlutterPESDK.willPresentPhotoEditViewController` allowing access to the `PhotoEditViewController` before it is presented on iOS.
* [video_editor_sdk] Added support to replace the `VideoEditViewController` with custom subclasses on iOS.
* [video_editor_sdk] Added `FlutterVESDK.willPresentVideoEditViewController` allowing access to the `VideoEditViewController` before it is presented on iOS.

### Changed

* [video_editor_sdk] Changed the example to use the default `Video` constructor since `Video.composition` is only available when having a valid license for the video composition feature.

## [2.0.0]

### Added

* Added null safety support for all three plugins.
* [imgly_sdk] Added integration and documentation for new video composition, video library and audio library tools.
* [imgly_sdk] Added missing code examples in the API documentation.
* [video_editor_sdk] Added integration and documentation for new video composition, video library and audio library tools.

### Changed

* [imgly_sdk] Updated identifier documentation for replaced and new fonts.
* [video_editor_sdk] The named parameter `video` of the `VESDK.openEditor` method now expects a `Video` instead of a `String`.

### Fixed

* Fixed crash when integrating all three plugins in the same project on Android.
* [imgly_sdk] Fixed some custom assets would not be resolved correctly on Android.
* [imgly_sdk] Fixed code examples in API documentation for using existing assets that are provided by the SDK.
* [imgly_sdk] Fixed thumbnail would not be loaded for a custom `Overlay` on iOS.

## [1.0.1]

### Added

* [photo_editor_sdk] Initial release.
* [video_editor_sdk] Initial release.

### Fixed

* [imgly_sdk] Fixed custom stickers and filters would not be resolved.

## [1.0.0]

### Added

* [imgly_sdk] Initial release.
