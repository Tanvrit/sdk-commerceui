# tanvrit-sdk · commerceui

> Compose Multiplatform UI screens for the full commerce experience: catalog, cart, checkout, orders, and more.

[![Maven](https://img.shields.io/badge/maven.tanvrit.com-1.0.12-blue)](https://maven.tanvrit.com)
![KMP](https://img.shields.io/badge/Kotlin_Multiplatform-7_targets-blueviolet)

## Install

### Option A — Tanvrit Gradle plugin _(recommended)_

```kotlin
// settings.gradle.kts
pluginManagement {
    repositories { maven { url = uri("https://maven.tanvrit.com") } }
}
```

```kotlin
// build.gradle.kts
plugins { id("com.tanvrit.sdk") version "1.0.12" }

tanvrit {
    version = "1.0.12"
    modules = listOf("commerceui")
}
```

### Option B — Direct dependency

```kotlin
// settings.gradle.kts
dependencyResolutionManagement {
    repositories { maven { url = uri("https://maven.tanvrit.com") } }
}
```

```kotlin
// build.gradle.kts  (KMP)
kotlin {
    sourceSets {
        commonMain.dependencies {
            implementation("com.tanvrit:commerceui:1.0.12")
        }
    }
}
```

## Targets

| Platform | Artifact |
|----------|----------|
| Android | `commerceui-android` |
| Iosarm64 | `commerceui-iosarm64` |
| Iossimulatorarm64 | `commerceui-iossimulatorarm64` |
| Iosx64 | `commerceui-iosx64` |
| Jvm | `commerceui-jvm` |
| Js | `commerceui-js` |
| Wasm Js | `commerceui-wasm-js` |

## Quick start

```kotlin
// Full commerce nav graph
CommerceNavGraph(navController = navController)

// Individual screens
ProductListScreen(businessId = "biz-001", storeId = "store-001")
CartScreen()
CheckoutScreen(orderId = "order-001")
```

## Resources

- **Full SDK source:** [tanvrit/sdk](https://github.com/tanvrit/sdk)
- **All modules:** [maven.tanvrit.com](https://maven.tanvrit.com)
- **Issues:** [tanvrit/sdk/issues](https://github.com/tanvrit/sdk/issues)
