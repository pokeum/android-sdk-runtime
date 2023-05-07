# Android SDK Runtime

<img src="https://source.android.com/static/docs/setup/images/Android_symbol_green_RGB.png" width=200>

SDK Runtime
=========

- `Design proposals`: Click [here](https://developer.android.com/design-for-safety/privacy-sandbox/sdk-runtime)
- `Developer Guides`: Click [here](https://developer.android.com/design-for-safety/privacy-sandbox/guides/sdk-runtime)

<br/>

[![Generic badge](https://img.shields.io/badge/android-privacy_sandbox_samples-black.svg)](https://github.com/android/privacy-sandbox-samples)


# Table of content   

- [Before you begin](#before-you-begin)
- [RE (Runtime-Enabled) SDKs](#re-sdks)


## <a id="before-you-begin"> Before you begin

- `Download Android Studio Hedgehog | 2023.1.1 Canary 2`: Click [here](https://developer.android.com/studio/preview)

- `Virtual Device`

    <img src="./docs/img/privacy_sandbox_device_setup_1.png" width=1000>

    | Pixel 3 |
    | :--- |
    | <img src="./docs/img/privacy_sandbox_device_setup_2.png" width=800> |


## <a id="re-sdks"> RE (Runtime-Enabled) SDKs

```mermaid
flowchart LR
subgraph App Foreground Process
SdkCallingCode["SDK Calling Code"]
SdkInterface["SDK Interface"]
end
subgraph SDK Runtime Process
Sdk["SDK"]
end
SdkCallingCode --> SdkInterface
SdkInterface --> Sdk
```

```mermaid
flowchart LR
subgraph App["client-app"]
SdkCallingCode["SDK Calling Code"]
SdkInterface["example-aidl-library"]
end
subgraph SDK Runtime Process["example-sdk"]
Sdk["sdk-implementation"]
end
SdkCallingCode ------> SdkInterface
SdkInterface --> Sdk
```