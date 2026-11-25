# 쇼츠 만들기 (재현판) — 맥 설치

macOS 12 이상(애플 실리콘·인텔).

## 1. 설치
1. 받은 zip을 두 번 눌러 풀고, 나온 `ShortsStudio` 폴더를 **홈 폴더**로 옮깁니다(바탕화면·문서 폴더는 자동 운영이 막힐 수 있음).
2. 터미널(⌘+Space → "터미널")에 붙여 넣고 Enter:

       xattr -dr com.apple.quarantine ~/ShortsStudio; bash ~/ShortsStudio/쇼츠만들기.command

3. 처음 한 번 파이썬 3.12 환경과 그림 도구를 준비합니다. 영상 도구 FFmpeg는 홈브루(`brew install ffmpeg`)로 설치됩니다. 홈브루가 없으면 https://brew.sh 에서 먼저 설치하세요.
4. 다음부터는 `ShortsStudio/쇼츠만들기.command` 를 두 번 누르면 됩니다.

## 2. AI 연결 (대본용, 둘 중 하나)
| 구독 | 설치 | 로그인 |
|---|---|---|
| ChatGPT | `curl -fsSL https://chatgpt.com/codex/install.sh \| sh` | `codex login` |
| Claude | `curl -fsSL https://claude.ai/install.sh \| bash` | `claude` → `/login` |

## 3. 목소리
맥 기본 한국어 음성(유나 등, 무료) 또는 구글 AI 목소리(키 필요).

## 4. 매일 자동 운영
[내 채널] → [자동 만들기]에서 켜고 저장하면, 저장 창에 나오는 `launchctl` 두 줄을 터미널에서 한 번 실행합니다.

## 5. 업데이트
새 버전 zip의 내용을 같은 폴더에 덮어쓰면 됩니다. `data` 폴더(내 채널·영상)는 그대로 둡니다.
