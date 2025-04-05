# Audio Transcribe

A command-line tool for transcribing audio files using OpenAI's Whisper model.

## Features

- Transcribe individual audio files with customizable options
- Batch process multiple audio files in a directory
- Support for various audio formats (MP3, WAV, M4A, OGG, FLAC)
- Multiple Whisper model sizes (tiny, base, small, medium, large)
- Progress indicators with rich terminal output
- Optional JSON output with detailed transcription results

## Installation

```bash
# Clone the repository
git clone https://github.com/audio_transcribe/audio_transcribe.git
cd audio_transcribe

# Install the package
pip install -e .
```

## Usage

### Single File Transcription

```bash
# Basic usage
audio-transcribe transcribe path/to/audio.mp3

# Specify output directory
audio-transcribe transcribe path/to/audio.mp3 -o output/directory

# Use a different model size
audio-transcribe transcribe path/to/audio.mp3 -m large

# Specify language (auto-detects if not specified)
audio-transcribe transcribe path/to/audio.mp3 -l en

# Save detailed results in JSON format
audio-transcribe transcribe path/to/audio.mp3 -j

# Translate to English
audio-transcribe transcribe path/to/audio.mp3 -t translate
```

### Batch Processing

```bash
# Process all audio files in a directory
audio-transcribe batch path/to/audio/directory

# Specify output directory
audio-transcribe batch path/to/audio/directory -o output/directory

# Use a different model size
audio-transcribe batch path/to/audio/directory -m large

# Process specific file extensions
audio-transcribe batch path/to/audio/directory -e mp3 wav
```

## Configuration Options

### Model Sizes

- `tiny`: Fastest, lowest accuracy
- `base`: Good balance of speed and accuracy
- `small`: Better accuracy, slower than base
- `medium`: High accuracy, slower processing
- `large`: Best accuracy, slowest processing

### Supported Audio Formats

- MP3
- WAV
- M4A
- OGG
- FLAC

### Output Options

- Text file output (default)
- Optional JSON output with timestamps and confidence scores
- Custom output directory specification

## Requirements

- Python 3.7 or higher
- Dependencies:
  - openai-whisper
  - typer
  - rich

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.
