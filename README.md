# CV6

## Aim

To perform **intensity-level slicing** on a grayscale image using OpenCV and NumPy, highlighting pixels whose intensity values fall within the selected range of **100 to 200**.

## Description

This project demonstrates a basic image-processing technique called intensity-level slicing. The input image is loaded in grayscale and examined pixel by pixel. Pixels with intensity values between `rmin = 100` and `rmax = 200` are selected and highlighted.

The program generates two processed images:

1. **Slice with Background** – pixels in the selected intensity range are retained, while pixels outside the range are set to black.
2. **Slice Without Background** – selected pixels are displayed in white on a black background, making the chosen intensity region easier to observe.

The original color image and both processed results are displayed together using Matplotlib.

## Technologies Used

- Python
- OpenCV (`cv2`)
- NumPy
- Matplotlib

## Input

The program expects an image named `images3.jpg` at the following location:

```text
/content/images3.jpg
```

The image is read in both grayscale and color formats. The grayscale version is used for intensity slicing, while the color version is used to display the original image.

## Output

The program displays a figure containing three panels:

1. **Original Image (Color)** – the input image in color.
2. **Slice with Background** – the selected intensity range is retained together with the processed background.
3. **Slice Without Background** – pixels with intensity values from 100 through 200 are shown in white, and all other pixels are shown in black.

The output helps identify and visualize the regions of the image whose grayscale intensities lie within the specified range.

## How to Run

1. Install the required libraries:

```bash
pip install opencv-python matplotlib numpy
```

2. Place the input image at `/content/images3.jpg`, or update the image path in `cv6.py`.
3. Run the program:

```bash
python cv6.py
```

## Conclusion

The project successfully demonstrates intensity-level slicing for grayscale images. By selecting the intensity range from 100 to 200, specific regions of the image can be isolated and visualized clearly. This technique is useful in computer vision applications such as object extraction, image enhancement, feature detection, and segmentation. The resulting three-panel visualization makes it easy to compare the original image with the processed images.
