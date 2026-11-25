# 쇼츠 만들기 (재현판) — 다운로드

주제 하나로 세로 쇼츠 영상(대본 → 목소리 → 그림 → 영상 → 검수 → 제목·썸네일)을 만드는 내 PC용 프로그램입니다.
대본은 내가 구독 중인 ChatGPT(Codex) 또는 Claude로 쓰고(API 키 불필요), 매일 정한 시각에 자동으로 만들 수도 있습니다.

이 저장소에는 **설치 파일만** 있습니다. 프로그램 소스는 공개하지 않습니다.

## 받기

**[최신 버전 받기 → Releases](https://github.com/ninestonelee/shorts-studio-rea-releases/releases/latest)**

| 컴퓨터 | 받을 파일 |
|---|---|
| 윈도우 10/11 (64비트) | `ShortsStudio-windows-x64-v버전.zip` — 파이썬 내장, 따로 설치할 것 없음 |
| 맥 (macOS 12 이상) | `ShortsStudio-macos-v버전.zip` |

받은 파일이 맞는지 확인하려면 같은 곳의 `SHA256SUMS.txt` 와 비교하세요.

## 윈도우 설치 (3단계)

1. zip을 **`C:\ShortsStudio`** 에 압축 풀기 (오른쪽 클릭 → 압축 풀기). 압축 파일 안에서 바로 열지 마세요.
2. **`start-windows.bat`** 두 번 누르기. "Windows의 PC 보호" 창이 뜨면 **추가 정보 → 실행**.
3. 처음 한 번 영상 도구(FFmpeg)를 받고 바탕화면에 **쇼츠만들기** 아이콘을 만듭니다. 브라우저에 프로그램이 열립니다.

## 맥 설치

zip을 풀어 `ShortsStudio` 폴더를 홈 폴더로 옮긴 뒤, 터미널에서:

    xattr -dr com.apple.quarantine ~/ShortsStudio; bash ~/ShortsStudio/쇼츠만들기.command

영상 도구는 홈브루(`brew install ffmpeg`)가 필요합니다.

## 대본용 AI 연결 (둘 중 하나)

| 구독 | 윈도우(PowerShell) | 맥(터미널) | 로그인 |
|---|---|---|---|
| ChatGPT | `powershell -ExecutionPolicy ByPass -c "irm chatgpt.com/codex/install.ps1 \| iex"` | `curl -fsSL https://chatgpt.com/codex/install.sh \| sh` | `codex login` |
| Claude | `irm claude.ai/install.ps1 \| iex` | `curl -fsSL https://claude.ai/install.sh \| bash` | `claude` → `/login` |

자세한 사용법은 zip 안의 `설치_안내.md` 를 보세요.

## 알아 둘 점

- 유튜브에는 자동으로 올리지 않습니다. 공개 시각을 잡고, 붙여 넣을 제목·설명·태그를 보여 줍니다.
- 그림은 AI 그림이 아니라 문장마다 고른 이모지와 도형 배경입니다.
- **윈도우 판은 아직 윈도우 PC 실기 검증 전입니다.** 문제가 있으면 프로그램 [점검] → [강사에게 보낼 내용 복사] 내용을 Issues에 남겨 주세요(키·토큰은 가려서 복사됩니다).
- 강의안에 공개된 사용법을 보고 새로 만든 독립 프로그램이며, 원본 상용 프로그램·제작사와 관계가 없습니다.
