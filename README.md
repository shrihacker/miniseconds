# miniseconds

Welcome to `miniseconds`, the tool designed to transform long YouTube videos such as podcasts, interviews, and lectures into short, engaging clips. Leveraging AI models like WhisperX hosted on Replicate and OpenAI, `miniseconds` is adept at identifying the most captivating moments in lengthy videos, offering a new way to experience and share content.

## Features

`miniseconds` automates the process of condensing extensive videos into digestible, shareable clips. Its functionality includes:
- **Transcription:** Extracting the audio transcript from YouTube videos.
- **Clip Identification:** Utilizing AI to determine segments of the video that can stand alone as engaging content.
- **Video Clipping:** Precisely clipping the video file to generate these short, engaging clips.

## Requirements

Apple Silicon is required since we use the mlx library

To use `miniseconds`, you'll need access to the following APIs and services:
- **OpenAI API:** For natural language processing capabilities.
- **Replicate API:** For accessing and utilizing the WhisperX model.
- **Google Cloud Storage:** For storing video & audio data. Please create a bucket that is publicly accessible

You will also need installed:
-  **ffmpeg:** For video editing capabilities

## Getting Started

Follow these steps to set up `miniseconds` in your environment:

1. **Clone the Repository:**

`git clone [repository URL]`

2. **Set up Services:**
- Set up OpenAI and obtain an API key
- Set up Replicate and obtain an API key
- Set up a google cloud storage bucket with public permissions for all objects in that bucket

3. **Set Up Virtual Environment:**

```
python3 -m venv venv
source venv/bin/activate # For Unix or MacOS
venv\Scripts\activate # For Windows
pip install -r requirements.txt
```

4. **Configure Environment Variables:**
- Create a `.env` file in the root directory.
- Follow the structure provided in `env.example` to add your API keys and Storage bucket.
- Create a `data` dir in the root directory.

5. **Launch Jupyter Notebook:**

`jupyter notebook`

- Open the notebook titled `miniseconds.ipynb`
- Navigate to the cell titled **"Start Here"**.
- Enter your YouTube link in the cell right below it.

6. **Execute the Notebook:**
- Run all cells to process the video and generate clips.

## Contribution

Contributions to `miniseconds` are welcome! Whether it's improving the algorithm, enhancing the user interface, or fixing bugs, your input is valuable.

## License

`miniseconds` is distributed under MIT License, which permits use, modification, and distribution under certain conditions. Refer to the LICENSE file for more details.
