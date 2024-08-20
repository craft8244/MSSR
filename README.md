# Multi Speaker Speech Recognition (MSSR)

## 개요
이 프로젝트는 **Multi Speaker Speech Recognition (MSSR)**을 [ESPnet](https://github.com/espnet/espnet) 툴을 사용하여 구현한 것입니다. 현재는 두 명의 음성이 섞인 경우 이를 분리하여 음성 인식하는 기능만 제공합니다. 앞으로 임의의 N명에 대해서도 구현할 예정입니다.

- 학습된 모델 링크: [모델 링크](#)
- 성능: (여기에 성능 정보를 추가하세요)
- 관련 논문 링크: [논문 링크](#)

## 설치 및 구동 방법
이 프로젝트는 기본적으로 ESPnet의 `egs2` 형식을 따릅니다. 아래의 단계를 따라서 설치하고 구동할 수 있습니다:

1. **ESPnet 설치**  
   ESPnet을 설치합니다. [ESPnet 설치 가이드](https://espnet.github.io/espnet/installation.html)를 참고하세요.

2. **path.sh 수정**  
   해당 프로젝트의 `path.sh` 파일에서 경로를 수정합니다.

3. **프로젝트 실행**  
   다음 명령어를 실행하여 프로젝트를 시작합니다:
   ```bash
   ./run.sh
