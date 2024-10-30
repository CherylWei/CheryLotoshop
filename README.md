# 🏞️ CheryLotoshop - Remove Objects from Your Photos

## 📜 Description
cheryLotoshop is an innovative application designed to help users remove unwanted objects, such as bystanders, from your beautiful photos. By importing multiple images taken in the same location but with different people appearing in each, cheryLotoshop can generate a clean, unobstructed image without any intruding elements.

### Features
- ✨ **Object Removal**: Automatically removes unwanted objects and people from your photos.
- 📸 **Multiple Image Processing**: Processes several images of the same scene to generate a clean result.
- ⚡ **Color Distance Algorithm**: Utilizes a color distance algorithm to detect and remove outlier pixels.
- 🎨 **High-Quality Output**: Generates a clean, high-quality image by combining the best pixels from each input image.

## 🚀 Getting Started

### Prerequisites
- Python 3.x
- The `simpleimage` library.

### Installing
1. Clone the repository:
   ```sh
   git clone https://github.com/cherylwei/cheryLotoshop.git
   ```
2. Navigate to the project directory:
   ```sh
   cd cheryLotoshop
   ```

## 🎮 Usage

To run the program, navigate to the project directory and execute the following command:
```sh
python cheryltoshop.py <directory_path>
```
Replace `<directory_path>` with the path to the directory containing the images to be processed.

## 📚 Algorithm Explanation

The algorithm works as follows:
1. **Load Images**: Load all the images from the specified directory.
2. **Process Pixels**: For each pixel position `(x, y)`, gather the pixels from all the images.
3. **Calculate Average**: Compute the average RGB values for the pixels at `(x, y)`.
4. **Color Distance**: Calculate the color distance of each pixel from the average.
5. **Select Best Pixel**: Select the pixel with the smallest color distance (i.e., the pixel closest to the average).
6. **Generate Clean Image**: Place the selected pixel into the corresponding position in the output image.
7. **Display Result**: Show the final clean image with all unwanted objects removed.

## 🔧 Functions Explanation

Here are the key functions in `cheryltoshop.py`:

### `get_pixel_dist(pixel, red, green, blue)`
Calculates the "color distance" between a pixel and a target average RGB value.
- **Input**: Pixel object, and target `red`, `green`, `blue` values.
- **Returns**: The "color distance" as a float value.

### `get_average(pixels)`
Computes the average red, green, and blue values for a list of pixels.
- **Input**: List of Pixel objects.
- **Returns**: List with average `red`, `green`, `blue` values.

### `get_best_pixel(pixels)`
Identifies the pixel closest to the average color from a list of pixels.
- **Input**: List of Pixel objects.
- **Returns**: Pixel object with the smallest color distance to the average.

### `solve(images)`
Processes a list of images to generate the clean output image.
- **Input**: List of SimpleImage objects.
- **Displays**: The resultant image.

### `jpgs_in_dir(dir)`
Returns a list of the .jpg filenames within a directory.
- **Input**: Directory name as a string.
- **Returns**: List of jpg filenames.

### `load_images(dir)`
Loads all .jpg files in a directory into memory.
- **Input**: Directory name as a string.
- **Returns**: List of SimpleImage objects.

## 👨‍💻 Developer Information

For developers looking to extend or modify the program, here are some key points:
- **Main Execution**: The `main` function sets up the script to be run from the command line, loading images from a specified directory and then processing them with the `solve()` method.

### Key Methods:

- `get_pixel_dist(pixel, red, green, blue)`: Calculates the distance between a pixel and the target RGB values.
- `get_average(pixels)`: Computes the average RGB values for a list of pixels.
- `get_best_pixel(pixels)`: Returns the pixel closest to the calculated average.
- `solve(images)`: Constructs the final clean image by iterating through each pixel position and finding the best matching pixel from the input images.

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request for any features, bug fixes, or improvements.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- This project is inspired and adapted from Nick Parlante and Jerry Liao's Ghost assignment.

## 🧑‍💻 Author

- Cheryl Lin 我是雪兒 - [@Cheryl_Wei]
