# fftools-sh

A collection of auxiliary FFmpeg scripts. Currently, it includes a script for
two-pass encoding of a video targeting a specific file size.

## Script: `ff-fsize`

### Description

`ff-fsize` reduces a video file to a specified size using two-pass encoding with
FFmpeg.

### Usage

```sh
ff-fsize [options] input_file [output_file]
```

### Options

- `-v, --video-codec` : Set the video codec (default: `libx265`)
- `-a, --audio-codec` : Set the audio codec (default: `copy`)
- `-s, --size` : Target file size in bytes (default: `96000`)
- `-p, --preset` : Set the FFmpeg preset (default: `medium`)
- `-b, --bitrate` : Set the video bitrate
- `--audio-bitrate` : Set the audio bitrate
- `-V, --verbose` : Enable verbose output
- `-x, --trace` : Enable trace mode

### Dependencies

- `ffmpeg`
- `ffprobe`
- `util-linux` (for `getopt`)

### Example

```sh
ff-fsize -s 5000000 input.mp4 output.mp4
```

# License

This project is licensed under the [ISC License](LICENSE).

---

Feel free to contribute or report issues on the GitHub repository.
