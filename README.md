# Device Independent Pixel (DIP) Calculator

This Dart class provides a utility for calculating device-independent pixels (DIP) in Flutter applications. Device-independent pixels are a unit of measurement used to ensure consistent UI layouts across different screen sizes and resolutions.

## Usage

To use the `Dip` class, follow these steps:

1. Import the necessary package:

    ```dart
    import 'dart:ui';
    ```

2. Instantiate the `Dip` class with the width and height of the design's viewport:

    ```dart
    Dip dipCalculator = Dip(designWidth: 375, designHeight: 812); // Example values
    ```

3. Call the `call` method of the `Dip` object to convert design pixels to device-independent pixels:

    ```dart
    double dipValue = dipCalculator(16); // Example: Convert 16 design pixels to DIP
    ```

## Constructor

### `Dip({required double designWidth, required double designHeight})`

- `designWidth`: The width of the design's viewport in pixels.
- `designHeight`: The height of the design's viewport in pixels.

## Methods

### `call(double designPixels)`

- `designPixels`: The length in pixels specified in the design.
- Returns: The calculated device-independent pixel value based on the current device's screen size and orientation.

## Properties

### `designLandscape`

- Type: `bool`
- Description: Indicates whether the design is in landscape orientation or not.

## Example

```dart
import 'dart:ui';

void main() {
  Dip dipCalculator = Dip(designWidth: 375, designHeight: 812);
  
  // Convert 16 design pixels to DIP
  double dipValue = dipCalculator(16);
  print('16 design pixels in DIP: $dipValue');
}
