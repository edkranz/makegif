# makegif
Simple shell script to generate gifs from videos using ffmpeg.

## Description
`makegif` is a shell script that converts video files into GIFs using `ffmpeg`. By default, it outputs a GIF at 720p resolution and 15 frames per second.

## Installation

If using `bash` or `zsh`, simply enter this command in your terminal:
```sh
curl -O https://raw.githubusercontent.com/yourusername/yourrepository/main/makegif && \
chmod +x makegif && \
sudo mv makegif /usr/local/bin/ && \
echo "alias makegif='/usr/local/bin/makegif'" >> ~/.bashrc && \
echo "alias makegif='/usr/local/bin/makegif'" >> ~/.zshrc && \
source ~/.bashrc && \
source ~/.zshrc
```

1. **Download the Script**:
    ```sh
    curl -O https://raw.githubusercontent.com/yourusername/yourrepository/main/makegif
    chmod +x makegif
    ```

2. **Move the Script to `/usr/local/bin`**:
    ```sh
    sudo mv makegif /usr/local/bin/
    ```

3. **Add Alias to `.bashrc` or `.zshrc`**:
    Add the following line to your `.bashrc` or `.zshrc` file to make the `makegif` command available in your terminal:
    ```sh
    alias makegif='/usr/local/bin/makegif'
    ```

## Usage

### Basic Usage
To convert a video to a GIF at 720p resolution and 15fps:
```sh
makegif video.mp4
```

### Custom Resolution Options
You can specify a custom resolution by passing the `-r` flag followed by the desired resolution:
```sh
makegif -l video.mp4
```
- Outputs a gif at 360p resolution.
```sh
makegif -m video.mp4
```
- Outputs a gif at 720p resolution.
```sh
makegif -h video.mp4
```
- Outputs a gif at 1080p resolution.
```sh
makegif -max video.mp4
```
- Outputs a gif at the original resolution of the input video.

### Custom Output Filename
You can also specify a custom output filename by entering it as the second argument:
```sh
makegif video.mp4 custom.gif
```

### Dependencies
- `ffmpeg`, which can be installed via Homebrew on macOS:
    ```sh
    brew install ffmpeg
    ```
    Or on Ubuntu/Debian-based systems:
    ```sh
    sudo apt-get install ffmpeg
    ```