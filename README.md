
# Binary Image Generator

A Flutter package that converts binary strings into a visual image with customizable colors for the background and squares.

## Installation

To use the `binary_image_generator` package, add it to your `pubspec.yaml` file:

```yaml
dependencies:
  binary_image_generator: ^1.0.0
```

Then run `flutter pub get` to install the package.

## Usage

Use the `BinaryImageGenerator` widget to generate an image from a binary string.

Example:

```dart
import 'package:binary_image_generator/binary_image_generator.dart';

BinaryImageGenerator(
  binaryString: '101010101010101', 
  backgroundColor: Colors.blue, 
  squareColor: Colors.green,
  onImageReady: (imageBytes) {
    // Handle the generated image (e.g., save or display)
  },
)
```

### Parameters:
- `binaryString`: The binary string (must be exactly 15 bits).
- `backgroundColor`: The color for the background (default: `Colors.purple`).
- `squareColor`: The color for the filled squares (default: `Colors.white`).
- `onImageReady`: A callback function that receives the generated image as a PNG byte array (`Uint8List`).

## Features

- **Customizable Colors**: Choose your background and square colors.
- **Binary to Image Conversion**: Visualizes binary strings as a grid of squares.
- **Mirrored Design**: The right side of the grid mirrors the left (excluding the middle column).
- **Callback for Image Data**: Retrieve the generated image as PNG bytes.

## Example Output

Given a binary string like `'111110000000011'`, the widget will generate a 5x5 grid where:
- "1" will represent a filled square.
- "0" will represent an empty square.
- You can customize the background and square colors.

![Example Output](https://i.imgur.com/NbWfqJH.png)

## License

This package is licensed under the MIT License. See the LICENSE file for details.

## Contact

For support or questions, feel free to contact me at [nadersakr.dev@gmail.com].
