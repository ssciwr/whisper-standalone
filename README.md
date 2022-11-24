# OpenAI Whisper standalone distribution

This is a stand-alone application that packages [OpenAI's Whisper](https://github.com/openai/whisper) into a distribution that does not require users to have Python installed. Additionally, it provides a minimalistic graphical user interface for transcription.

## Installation on Windows 10+

Please download the zipped distribution from one of the following sources and unpack it to a target location of your choice:

* T.b.d

## Usage on Windows

Running `run_whisper.exe` (e.g. by double clicking) will fire up the graphical user interface, allowing you to specify input and output files, a model and device to run on.

If you want to work with `whisper`'s command line interface instead, you can do so by providing arguments on the command_line:

```
run_whisper --help
```

## Linux

Currently, there is no (working) stand-alone packaging for Linux due to issues in [pyinstaller](https://github.com/pyinstaller/pyinstaller)'s handling of PySide6.
If you are still interested in using the GUI from Ubuntu/Debian, the following sequence of commands will install dependencies and run locally:

```
sudo apt install ffmpeg python3 python3-pip git
git clone https://github.com/ssciwr/whisper-standalone.git
cd whisper-standalone
python -m pip install -r requirements.txt
python run_whisper.py
```

## Licensing

The code provided in this project itself is covered by [the MIT license](LICENSE.md). The overall distribution is also licensed under the MIT license. For details about bundled components and their license, please check [LICENSE.md](LICENSE.md).
