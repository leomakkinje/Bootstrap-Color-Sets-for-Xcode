# Bootstrap Color Sets for Xcode

<p>
    <img src="https://img.shields.io/badge/Swift-3+-orange" />
    <img src="https://img.shields.io/badge/Xcode-9+-orange" />
    <img src="https://img.shields.io/badge/Platform-iOS_11%2B_%7C_iPadOS_13%2B_%7C_macOS_10.13%2B_%7C_tvOS%2011%2B_%7C_visionOS_1%2B_%7C_watchOS_4%2B-orange" />
</p>

Bootstrap Color Sets is an Xcode Assets library containing the entire [Bootstrap](https://getbootstrap.com/) color palette.

Adding this library to the Assets folder in your Swift project enables instant availability of all Bootstrap colors.

## Color palette

- **Theme**
  - `Color.bsDanger`
  - `Color.bsDark`
  - `Color.bsInfo`
  - `Color.bsLight`
  - `Color.bsPrimary`
  - `Color.bsSecondary`
  - `Color.bsSuccess`
  - `Color.bsWarning`

- **Color**
  - `Color.bsBlue`
  - `Color.bsCyan`
  - `Color.bsGreen`
  - `Color.bsIndigo`
  - `Color.bsOrange`
  - `Color.bsPink`
  - `Color.bsPurple`
  - `Color.bsRed`
  - `Color.bsTeal`
  - `Color.bsYellow`
  - *Note: each color is available in 9 tints, e.g. `Color.bsBlue100`, `Color.bsBlue200` ... `Color.bsBlue900`*

- **Monochrome**
  - `Color.bsBlack`
  - `Color.bsGray`
  - `Color.bsGrayDark`
  - `Color.bsWhite`
  - *Note: bsGray is available in 9 tints, e.g. `Color.bsGray100`, `Color.bsGray200` ... `Color.bsGray900`*

- **Body**
  - `Color.bsBodyBackground`
  - `Color.bsBodyForeground`
  - *Note: both colors adapt to Light/Dark Mode*

## Installation

1. Prepare your Xcode project:
    1. Open your project in Xcode
    1. Select Assets in the Project Navigator
1. Download the Bootstrap Color Sets library:
    1. Download the latest release from [the Releases page](https://github.com/leomakkinje/Bootstrap-Color-Sets-for-Xcode/releases) or by clicking [this link](https://github.com/leomakkinje/Bootstrap-Color-Sets-for-Xcode/archive/refs/tags/1.0.0.zip)
    1. Open the Downloads folder on your computer
    1. Double-click file `Bootstrap-Color-Sets-for-Xcode-1.0.0.zip` to unzip it
    1. Double-click folder `Bootstrap-Color-Sets-for-Xcode-1.0.0` to open it
1. Add the Bootstrap Color Sets library to your Xcode project:
    1. Drag folder `Bootstrap Color Sets` into the `Assets` column in Xcode

## Usage

Bootstrap colors are used the same way you would use any other color in Swift. Simply refer to the color's name, e.g. `Color.bsBlue` or `.bsBlue`.

```swift
struct ContentView: View {
    var body: some View {
        VStack {
            Text("Little Green Bag")
                .foregroundStyle(.bsGreen)
            Text("Red Right Hand")
                .foregroundStyle(.bsRed)
        }
        .background(.bsYellow200)
    }
}
```

## Dark mode

`Color.bsBodyBackground` and `Color.bsBodyForeground` can be used to define a background color or foreground color that adapts to the Light/Dark Mode setting of a device.

```swift
struct ContentView: View {
    var body: some View {
        ZStack {
            Color.bsBodyBackground
                .ignoresSafeArea(.all)

            Text("You Want It Darker")
                .foregroundStyle(.bsBodyForeground)
        }
    }
}
```

```swift
struct ContentView: View {
    var body: some View {
        List {
            Group {
                Text("Blinded By The Light")
                Text("Dancing In The Dark")
            }
            .listRowBackground(Color.clear)
            .listRowSeparatorTint(.bsBodyForeground)
        }
        .listStyle(.plain)
        .background(.bsBodyBackground)
        .foregroundStyle(.bsBodyForeground)
    }
}
```

## License

This project is open source and available under the MIT license. For more information, see the [LICENSE](https://github.com/leomakkinje/Bootstrap-Color-Sets-for-Xcode/blob/main/LICENSE) file.

## Disclaimer

This project is not affiliated with, sponsored by, or endorsed by [Bootstrap](https://getbootstrap.com/).
