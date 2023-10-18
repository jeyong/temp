# PC에 개발 환경 설치하기
## 준비물
  * Intel/AMD 기반 PC/노트북
  * Ubuntu 22.04 설치
## 환경 설치
* 터미널 열고 개발환경 설치하기
```bash
mkdir ~/projects
cd ~/projects
git clone https://github.com/PX4/PX4-Autopilot.git --recursive
bash ./PX4-Autopilot/Tools/setup/ubuntu.sh  # 개발환경 설치됨 (설치 여부 'y' 입력)
```

* 설치가 종료되면 컴퓨터를 리부팅하기

## PX4 시뮬레이션 실행하기
* 터미널 열기
```bash
cd ~/projects/PX4-Autopilot
make px4_sitl jmavsim
```
* 시뮬레이션 화면이 보이면 성공

## Pixawk 빌드하기
```bash
cd ~/projects/PX4-Autopilot
make px4_fmu-v5_default
```
* 빌드가 완료되면 성공
