# 수정내역
`2023.08.03`
1. 영상에서 오디오를 분리 하여 작업 하도록 수정하였습니다.(디폴트:True)
2. 최초 모델을 medium으로 선택 하도록 하였습니다. 메모리 확인후 디폴트 설정 하는것이 좋아 보입니다.
3. 자막 생성시 공백이 생기는 현상을 제거 하였습니다.
4. transfer to english 관련 버튼을 medium 기준으로 하여 최초에는 보이지 않게 설정 하였습니다.(large에서만 보입니다.)


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

1. 설치경로로 이동하여 `Install.bat` 수행합니다.
2. 1번 설치후 `start-webui.bat`. 수행합니다. 최초 모델 다운로드 시간이 소요됩니다.(각각 모델별로.)
3. 브라우저에서 `http://localhost:7860` 으로 이동합니다.

( 다른 Web-UI를 실행 중인 경우 `localhost:7861`, `localhost:7862` 등과 같은 다른 포트에서 호스팅됩니다. )

# 사용가능한 모델 
The WebUI uses the Open AI Whisper model
|  Size  | Parameters | English-only model | Multilingual model | Required VRAM | Relative speed |
|:------:|:----------:|:------------------:|:------------------:|:-------------:|:--------------:|
|  tiny  |    39 M    |     `tiny.en`      |       `tiny`       |     ~1 GB     |      ~32x      |
|  base  |    74 M    |     `base.en`      |       `base`       |     ~1 GB     |      ~16x      |
| small  |   244 M    |     `small.en`     |      `small`       |     ~2 GB     |      ~6x       |
| medium |   769 M    |    `medium.en`     |      `medium`      |     ~5 GB     |      ~2x       |
| large  |   1550 M   |        N/A         |      `large`       |    ~10 GB     |       1x       |

`.en` models are for English only, and the cool thing is that you can use the `Translate to English` option from the `large` models!

# 참고사항
ex) C:\Users\{본인계정}\AppData\Local\Temp\gradio 아래 임시파일들이 생성이 됩니다.