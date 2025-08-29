# Pixglyph

A Python-based terminal video player that converts videos to ASCII art and plays them directly in your terminal. This project transforms regular video files into text-based animations using ASCII characters.

## Preview
<video width="320" height="240" controls>
  <source src="./demo.mp4" type="video/mp4">
</video>

## Requirements

- Python 3.6+
- OpenCV (opencv-python)
- Pillow (PIL)

## Installation

1. Clone this repository or download the source code:

```bash
git clone https://github.com/Estifanos12/pixglyph.git
cd pixglyph
```

2. Install the required dependencies:

```bash
pip install -r requirements.txt
```

## Usage

Run the script with a video file as an argument:

```bash
python pixglyph.py [video_file]
```

If no video file is specified, it will default to `video.mp4` in the current directory.

### Examples

```bash
# Play the default video
python pixglyph.py

# Play a specific video
python pixglyph.py your_video.mp4
```

### Controls

- Press `Ctrl+C` to stop playback at any time

## How It Works

The ASCII Video Player works through several key steps:

1. **Video Loading**: Opens the video file using OpenCV
2. **Frame Processing**: Converts each frame to grayscale
3. **Resizing**: Resizes the frame to fit the terminal width while maintaining aspect ratio
4. **ASCII Conversion**: Maps pixel brightness values to ASCII characters
5. **Frame Interpolation**: Creates intermediate frames for smoother playback
6. **Terminal Display**: Clears the terminal and displays each ASCII frame

