---
layout: "default"
title: "PresentationKit: A SwiftUI Library for Alerts and Modals 🎉"
description: "Easily present alerts, sheets, and full-screen covers in SwiftUI with PresentationKit. Enhance your app's UI with simple, observable contexts. 🚀📦"
---
# PresentationKit: A SwiftUI Library for Alerts and Modals 🎉

![SwiftUI](https://img.shields.io/badge/SwiftUI-5B8C7A?style=for-the-badge&logo=swift&logoColor=white) ![iOS](https://img.shields.io/badge/iOS-000000?style=for-the-badge&logo=apple&logoColor=white) ![macOS](https://img.shields.io/badge/macOS-000000?style=for-the-badge&logo=apple&logoColor=white) ![tvOS](https://img.shields.io/badge/tvOS-000000?style=for-the-badge&logo=apple&logoColor=white) ![watchOS](https://img.shields.io/badge/watchOS-000000?style=for-the-badge&logo=apple&logoColor=white)

## Overview

PresentationKit is a SwiftUI library designed to simplify the presentation of alerts and modal content across multiple Apple platforms, including iOS, iPadOS, macOS, tvOS, visionOS, and watchOS. This library provides a straightforward API that helps developers create intuitive user interfaces with minimal effort.

### Features

- **Easy Alert Presentation**: Quickly show alerts with customizable options.
- **Modal Content**: Present full-screen covers and sheets seamlessly.
- **Cross-Platform Support**: Works on iOS, iPadOS, macOS, tvOS, visionOS, and watchOS.
- **Lightweight and Efficient**: Minimal overhead ensures smooth performance.
- **Customizable**: Tailor the appearance and behavior to fit your app's design.

## Installation

To get started with PresentationKit, you can add it to your project using Swift Package Manager. Open your Xcode project, navigate to the project settings, and add the following URL to your package dependencies:

```
https://github.com/kalyanijawalekar/PresentationKit
```

## Usage

### Importing the Library

Begin by importing PresentationKit into your SwiftUI view:

```swift
import PresentationKit
```

### Presenting an Alert

To present an alert, use the `AlertView` provided by the library. Here’s a simple example:

```swift
struct ContentView: View {
    @State private var showAlert = false

    var body: some View {
        Button("Show Alert") {
            showAlert = true
        }
        .alert(isPresented: $showAlert) {
            Alert(title: Text("Hello"), message: Text("This is an alert!"), dismissButton: .default(Text("OK")))
        }
    }
}
```

### Presenting a Modal

For presenting modal content, you can use the `FullScreenCover` or `Sheet`:

```swift
struct ContentView: View {
    @State private var showModal = false

    var body: some View {
        Button("Show Modal") {
            showModal = true
        }
        .fullScreenCover(isPresented: $showModal) {
            ModalView()
        }
    }
}

struct ModalView: View {
    var body: some View {
        VStack {
            Text("This is a full-screen modal!")
            Button("Dismiss") {
                // Dismiss logic here
            }
        }
    }
}
```

## Customization Options

### Alert Customization

You can customize alerts by modifying their title, message, and buttons. Here's an example of a customized alert:

```swift
.alert(isPresented: $showAlert) {
    Alert(title: Text("Warning"),
          message: Text("Are you sure you want to proceed?"),
          primaryButton: .destructive(Text("Delete")) {
              // Handle delete action
          },
          secondaryButton: .cancel())
}
```

### Modal Customization

For modals, you can control the presentation style and animations. You can also pass data to the modal view:

```swift
.fullScreenCover(isPresented: $showModal) {
    ModalView(data: someData)
}
```

## Documentation

Comprehensive documentation is available in the [Wiki](https://github.com/kalyanijawalekar/PresentationKit/wiki). This resource provides detailed information on all features, usage examples, and best practices.

## Examples

To see PresentationKit in action, check out the example projects in the `Examples` folder of this repository. These projects demonstrate various use cases and show how to implement the library effectively.

## Contributing

We welcome contributions to PresentationKit. If you want to help improve the library, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your branch and create a pull request.

For larger changes, consider opening an issue first to discuss your ideas.

## License

PresentationKit is released under the MIT License. See the [LICENSE](https://github.com/kalyanijawalekar/PresentationKit/blob/main/LICENSE) file for details.

## Releases

You can find the latest releases of PresentationKit [here](https://github.com/kalyanijawalekar/PresentationKit/releases). Download the latest version and integrate it into your project.

## Support

If you encounter any issues or have questions, please open an issue in the repository. We appreciate your feedback and are here to help.

## Acknowledgments

Thanks to the SwiftUI community for their contributions and support. Your input helps make this library better for everyone.

## Topics

- alert
- fullscreencover
- ios
- ipados
- macos
- sheet
- swift
- swiftui
- tvos
- visionos
- watchos

For further information, visit the [Releases](https://github.com/kalyanijawalekar/PresentationKit/releases) section for updates and new features.