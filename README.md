# Video Subtitles Detector

## Overview

The Video Subtitles Detector is a program designed to detect and highlight subtitles within a video. It identifies the area containing the subtitles by drawing bounding boxes around them and further detects the location of each word within the subtitles. The program processes the video using basic filters and morphological operations, without relying on deep learning, machine learning, or OCR techniques.

## Features

- Detect and highlight subtitles in a video using image processing techniques.
- Draw red bounding boxes around each line of subtitles.
- Draw green bounding boxes around each word within the subtitles.
- Process and apply bounding boxes to all subtitles in the video.

## Requirements

- Python 3.x
- OpenCV
- numpy


## Usage

1. Place the video file you want to process in the `input` directory.

2. Run the subtitles detector script:
    ```bash
    python detect_subtitles.py --input input/your_video.mp4 --output output/processed_video.mp4
    ```

3. The processed video with bounding boxes will be saved in the `output` directory.

## Arguments

- `--input` : Path to the input video file.   (https://drive.google.com/file/d/1mUOdZbcvRS_UTIoi4wGdfp9i8pNl3fYM/view video used in project)
- `--output` : Path to save the processed video file.

## Example

To run the program on an example video:
```bash
python detect_subtitles.py --input input/example_video.mp4 --output output/processed_example_video.mp4
```

## Expected Output

- **Red Bounding Box**: Represents the bounding box of the subtitles (a separate bounding box for each line if the subtitles span across multiple lines).
- **Green Bounding Box**: Represents the bounding box of each word within the subtitles.

## Methodology

This program uses basic image processing techniques such as:
- Grayscale conversion
- Thresholding
- Morphological operations (e.g., dilation and erosion)
- Contour detection

These techniques help in identifying the regions containing subtitles and distinguishing individual words within the subtitles.

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.


Thank you for using the Video Subtitles Detector! I hope it helps you with your project.
