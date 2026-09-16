Video Restoration Toolkit

A Python-based toolkit for video denoising, inpainting, lighting enhancement, and object removal.

Features

- Video noise reduction using OpenCV
- Mask-based image and video inpainting
- Lighting and local contrast enhancement
- Basic object removal using manually supplied masks
- Command-line interface
- Modular architecture for future AI integration

Installation

Requirements:

- Python 3.10+
- FFmpeg
- pip

Clone the repository:

git clone https://github.com/YOUR_USERNAME/video-restoration-toolkit.git
cd video-restoration-toolkit

Create and activate a virtual environment, then install:

python -m pip install -e ".[dev]"

Usage

Denoise:

video-restore denoise input/clip.mp4 output/clean.mp4

Enhance lighting:

video-restore lighting input/clip.mp4 output/bright.mp4

Inpaint a masked area:

video-restore inpaint input/clip.mp4 output/repaired.mp4 --mask masks/repair.png

Remove a masked object:

video-restore remove-object input/clip.mp4 output/removed.mp4 --mask masks/object.png

Limitations

The initial implementation uses frame-by-frame OpenCV processing. Large-object removal, moving-object tracking, temporal consistency, and advanced reconstruction require additional models and development.

The basic video writer does not preserve original audio. Use FFmpeg for audio remuxing and validate synchronization.

Roadmap

- [ ] Add mask drawing interface
- [ ] Add audio-preserving export
- [ ] Add object segmentation and tracking
- [ ] Integrate video inpainting models
- [ ] Add GPU acceleration
- [ ] Add a graphical user interface
- [ ] Add automated quality evaluation

Contributing

Contributions are welcome. Please open an issue before major changes and include tests for new functionality.

License

MIT License.