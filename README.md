<!-- logo -->
<p align="center">
    <a href="https://github.com/redstar-javscraper/redstar_upscaler" alt="redstar upscaler Logo">
    <img src="https://github.com/redstar-javscraper/redstar_upscaler/assets/72743692/deebb21a-9c12-4cb1-8b94-f59fb64a26cb" height="173"/></a>
</p>

<h1 align="center"> redstar upscaler </h1>

<h4 align="center">
    ffmpeg, realesrgan, flowframe을 활용한 동영상 업스케일링 도구
</h4>

<br></br>


## Table of Contents

  * [<g-emoji class="g-emoji" alias="thinking" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f914.png">🤔</g-emoji> 준비사항](#-준비사항)
  * [<g-emoji class="g-emoji" alias="eyes" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f440.png">👀</g-emoji> 환경구성](#-환경구성)
  * [<g-emoji class="g-emoji" alias="books" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4da.png">📚</g-emoji> 사용법](#-사용법)
* [<g-emoji class="g-emoji" alias="pray" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f64f.png">🙏</g-emoji> Thank You](#-thank-you)

## 🤔 redstar upscaler?

[redstar upscaler](https://github.com/redstar-javscraper/redstar_upscaler)는 동영상 업스케일링을 한번에 수행하기 위해 파이썬으로 개발된 도구입니다. 
파이썬으로 개발되었으므로 다중 플랫폼에서 실행은 가능하나, 윈도우 환경에서만 테스트 되었으므로 이슈 발생 시 issue 탭에 등록해 주시면 검토해 보겠습니다.

아래는 간단한 사용 데모화면입니다.
[![Video Label](https://youtu.be/Aipen-xxyW4)]

## 👀 준비사항

프로그램을 실행하기 전에 아래의 사항을 확인한 후 준비하십시오<br>

1. ffmpeg 다운로드 및 설치 [Download](https://www.ffmpeg.org/download.html)
2. realesrgan 다운로드 및 설치 [Download](https://www.ffmpeg.org/download.html) 본문의 Portable Windows 버전 추천
3. flowframe 다운로드 및 설치 [Download](https://github.com/n00mkrad/flowframes)

## 👀 환경구성

1. ffmpeg, realesrgan의 경우 cmd 환경에서 바로 수행될 수 있도록 시작>설정>정보>고급 시스템 설정>환경변수> path에 실행파일 경로를 등록한 후 재 시작 합니다.

* ffmpeg: C:\upscale\ffmpeg\bin
* realesrgan: C:\upscale\realesrgan-ncnn-vulkan-20220424-windows

2. flowframes은 설치형 프로그램으로 redstar upscaler 실행 후 설치된 파일의 위치를 직접 지정합니다. 일반적으로 아래와 같은 경로에 설치됩니다

* flowframes: C:\Users\ [본인 계정] \AppData\Local\Flowframes

## 📚 사용법

ffmpeg, realesrgan, flowframes 환경구성이 완료되고 redstar upscaler에서 설정이 완료되면 아래와 같은 창을 볼 수 있습니다.

![mainwindow](https://github.com/redstar-javscraper/redstar_upscaler/assets/72743692/d7afe97f-ad7f-41d7-81d4-4cd94ddd8f00)

작업 순서는 다음과 같습니다.

1. 작업할 동영상 파일 선택<br>
    A. 다중 파일 선택이 가능하며, MP4, MKV, AVI 파일만 선택 가능합니다.<br>
2. 작업을 수행할 폴더 선택<br>
    A. 1에서 선택한 파일의 위치를 가져옵니다.<br>
    B. 다른 위치를 선택했을 경우 선택한 위치에서 작업을 수행합니다.<br>
    C. 작업 시 많은 공간이 필요하므로 여유있는 드라이브를 선택합니다.<br>
3. 영상의 프레임 정보 입력<br>
    A. 선택한 파일의 마지막 파일의 프레임 정보가 자동 입력됩니다.<br>
    <font color=red>※ 주의: 선택된 동영상은 반드시 프레임 정보가 같은 파일로 등록해야 합니다. 다른 프레임일 경우 결과물에서 음성 Sync가 틀어질 수 있습니다.</font><br>
4. realesrgan의 업스케일링 방법을 선택합니다.<br>
    A. 3가지 옵션이 있으며, 1, 3번은 4배, 2번은 2배 크기로 업스케일 합니다.
5. realesrgan의 이미지 추출 확장자를 선택합니다.<br>
    A. PNG의 경우 JPG보다 이미지 크기가 크므로 드라이브 여유공간을 고려하여 선택합니다.<br>
    B. WEBP의 경우 다중 이미지가 아닌 단일 파일로 만들어지므로 현재 버전에서는 지원하지 않습니다.<br>
6. 병행작업 옵션 입력    
    A. CPU, Memory에 따라 조절 가능<br>
    B. load : process : save 순서<br>
7. 영상 인코딩 퀄리티 옵션<br>
    A. 값이 낮을수록 높은 퀄리티를 나타내지만 용량은 그만큼 증가합니다.<br>
8. codec 선택<br>
    A. 원본 영상의 오디오 옵션에 따라 MP3/AAC 중 한가지를 선택합니다.<br>
9. Bitrate 설정<br>
    A. 출력할 영상에 적용할 오디오 bitrate를 입력합니다.<br>
10. flowframes를 사용한 프레임 보간 설정<br>
    A. 실행여부: 프레임 보간을 사용하지 않을 경우 체크 해제합니다.<br>
    B. 출력 FPS 배수: 프레임 보간 배수를 설정합니다.<br>
    C. 보간 AI: 보간에 사용할 AI를 선택합니다.<br>
    D. AI 모델: 보간에 사용할 AI 모델을 선택합니다.<br>
    E. 파일 형식: 최종 결과파일의 확장자 형식을 선택합니다.<br>

※ 작업이 완료된 파일은 접두사 [REDSTAR]를 붙인 파일명으로 저장됩니다


# 🙏 Thank You

수정 및 건의사항은 Issue 탭에서 등록해 주시기 바랍니다.
