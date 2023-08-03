# Whisper-WebUI-Kr
자동으로 자막을 생성을 쉽게 제공 해주는 UI입니다.
% 추가적으로 요구사항을 수용 해보려고 fork하였습니다.

![Whisper WebUI](https://github.com/samuggi/Whisper-WebUI-Kr/blob/master/screenshot.png)

## Notebook
If you wish to try this on Colab, you can do it in [here](https://colab.research.google.com/github/samuggi/Whisper-WebUI-Kr/blob/master/notebook/whisper-webui.ipynb)!

# Feature
- 생성가능한 소스입니다. :
  - Files
  - Youtube
  - Microphone
- 결과물 제공 하는 자막 포맷 : 
  - SRT
  - WebVTT
- Speech to Text Translation
  - From other languages to English.

# Installation and Running
## Prerequisite
To run Whisper, you need to have `git`, `python` version 3.8 ~ 3.10 and `FFmpeg`.

필요한 소프트웨어를 설치하려면 아래 링크를 따르십시오.: (존재 할 경우 패스가능)
- git : [https://git-scm.com/downloads](https://git-scm.com/downloads)
- python : [https://www.python.org/downloads/](https://www.python.org/downloads/)
- FFmpeg :  [https://ffmpeg.org/download.html](https://ffmpeg.org/download.html)

FFmpeg설치후 **반드시 `FFmpeg/bin` folder to your PATH설정!!**

## Automatic Installation
If you have satisfied the prerequisites listed above, you are now ready to start Whisper-WebUI-Kr.

1. Run `Install.bat` from Windows Explorer as a regular, non-administrator user.
2. After installation, run the `start-webui.bat`. (It will automatically download the model if it is not already installed.)
3. Open your web browser and go to `http://localhost:7860`

( If you're running another Web-UI, it will be hosted on a different port , such as `localhost:7861`, `localhost:7862`, and so on )

# Available models

The WebUI uses the Open AI Whisper model

|  Size  | Parameters | English-only model | Multilingual model | Required VRAM | Relative speed |
|:------:|:----------:|:------------------:|:------------------:|:-------------:|:--------------:|
|  tiny  |    39 M    |     `tiny.en`      |       `tiny`       |     ~1 GB     |      ~32x      |
|  base  |    74 M    |     `base.en`      |       `base`       |     ~1 GB     |      ~16x      |
| small  |   244 M    |     `small.en`     |      `small`       |     ~2 GB     |      ~6x       |
| medium |   769 M    |    `medium.en`     |      `medium`      |     ~5 GB     |      ~2x       |
| large  |   1550 M   |        N/A         |      `large`       |    ~10 GB     |       1x       |


`.en` models are for English only, and the cool thing is that you can use the `Translate to English` option from the "large" models!

