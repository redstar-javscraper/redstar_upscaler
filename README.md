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

다운로드 : [Release](https://github.com/redstar-javscraper/redstar_upscaler/releases)


## Table of Contents
  
  * [<g-emoji class="g-emoji" alias="thinking" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f914.png">🤔</g-emoji> 준비사항](#-준비사항)  
  * [<g-emoji class="g-emoji" alias="eyes" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f440.png">👀</g-emoji> 환경구성](#-환경구성)
  * [<g-emoji class="g-emoji" alias="books" fallback-src="https://github.githubassets.com/images/icons/emoji/unicode/1f4da.png">능

v 0.1.8
 > 버전 체크 시 신규 버전 확인 오류 수정
 > flowframes가 기본 경로에 설치되었을 경우(ex. C:\Users\Administrator\AppData\Local\Flowframes\) 해당 경로를 기본으로 설정 후 시작
 > 여러개 파일 선택 추가 시 오류로 인해 강제 종료되는 문제 
 > 다중 파일을 추가한 후 작업 시작 시 오류 발생하는 부분 수정

v 0.1.7
 > 1. 프로그램 크기 변경 가능
 > 2. 음성이 없는 파일 작업 시 오류 발생하는 문제 해결
 > 3. 전체 UI 구성 변경(크기 변경에 맞게 재 구성함)

v 0.1.6
 > 1. 화면 해상도에 따라 글자 크기가 다른 문제 해결
 > 2. 프로그램 타이틀에 버전 정보가 신규 버전으로 보이지 않는 문제 해결
 > 3. config.ini파일이 다른 경로에 저장되는 문제 해결
 > 4. realesrgan 업스케일링 배수 변경 시 업스케일링 모델 콤보박스도 같이 변경
 > 5. 업데이트 체크 기능 추가
 > 6. 일부 로직 수정
 > 7. 해상도 및 fps등 테이블 표기 컬러 변경
 > 8. 해상도(전) 사용자 수정 가능(반드시 1024x768 형태로 입력해야 함)

v 0.1.5
 > 1. flowframes 보간 ai 선택 시 ai 모델이 자동 변경되지 않는 문제 해결
 > 2. flowframes 보간 시 선택된 옵션대로 보간되지 않는 문제 해결
 > 3. 일부 동영상의 FPS 계산 시 잘못된 FPS로 계산되는 경우를 방지하기 위해 "FPS 계산방식" 콤보박스 추가
        -> r_frame_rate / avg_frame_rate 중 선택 가능하며, 기본은 r_frame_rate로 계산합니다
 > 4. 동영상 파일을 선택했을 때 동영상 정보 가져오는 진행 현황을 표기 
 > 5. 파일 연 후 다시 파일 선택 시 마지막 선택한 폴더를 기본으로 열도록 변경

v 0.1.4
 > 1. config.ini 파일 읽기 방식 변경
 > 2. 동영상 정보 가저오는 방식을 파이썬 AV에서 ffmpeg로 변경
 > 3. 작업 종료 시 윈도우 종료기능 추가
 > 4. 작업 리스트에서 마우스 오버 시 전체 파일명을 툴팁으로 표시
 > 5. 작업 리스트에 각 파일별 해상도(전) / 해상도(후) / FPS(전) / FPS(후) 표기
 > 6. FPS 입력 상자 제거(위 각 파일별 표기로 인한 제거)
 > 7. 출력 FPS 예상 크기 제거(위 각 파일별 표기로 인한 제거)
 > 8. 진행 상태를 전체파일/작업별 두개의 Progressbar로 표기

v 0.1.3
 > 1. 파일 불러올 때 일부 FPS 정보가 틀린 파일 FPS 계산 오류 수정

v 0.1.2
 > 1. UI 구성 변경   
 > 2. 내부 로직 변경  
 > 3. realesrgan 모델 중 아래 두개 모델 선택 시 실행되지 않는 문제 해결  
 > 4. realesrgan 모델 사용방식 변경   
 >    -> realesrgan 설치폴더 내 models 폴더에 신규 모델 파일(*.param)을 복사하면 사용 가능합니다  
 > 5. 작업 대상 영상의 마지막 파일의 width, height 정보 및 예상 업스케일 크기 표시  
 > 6. config.ini 파일 마이그레이션 코드 작성  
 > 7. ffmpeg 분해 이미지 aac -> flac로 변경  
 > 8. 기타 버그 수정

v 0.1.1
 > 1. 최초 작성, ffmepg, realesrgan, flowframes를 연동한 동영상 업스케일링 프로그램 작성   

# 🙏 Thank You

수정 및 건의사항은 Issue 탭에서 등록해 주시기 바랍니다.
