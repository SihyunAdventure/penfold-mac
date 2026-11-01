# Penfold — Mac 준비

Penfold iPhone 앱이 이 Mac의 코딩 에이전트(herdr)를 보고 조종하려면 Mac 쪽 준비가 필요해요. 터미널에 한 줄이면 돼요.

```sh
curl -fsSL https://raw.githubusercontent.com/SihyunAdventure/penfold-mac/main/setup | zsh
```

파일은 `~/.penfold` 에 받아지고, 아래를 하나씩 확인해요. 없는 건 그 자리에서 설치를 도와요(설치 전에는 항상 물어봐요).

1. 개발자 도구 (python3)
2. Tailscale — 설치·로그인·켜기
3. 원격 로그인 (SSH)
4. Herdr — herdr-core(`hc`)와 Herdr 앱
5. 알림 — 에이전트가 답을 기다리거나 끝나면 iPhone에 알려요 (penfold-relay 를 거쳐 Apple 푸시로)
6. iPhone 연결 — 터미널에 QR이 뜨면 iPhone 카메라로 찍어요

다시 실행해도 괜찮아요. 끝난 단계는 확인만 해요.

```sh
~/.penfold/setup            # 다시 실행
~/.penfold/setup --check    # 바꾸지 않고 상태만
~/.penfold/penfold-pair     # 준비된 Mac에서 QR만 다시
```

Homebrew는 필요 없어요. QR은 macOS 기본 기능(Core Image)으로 그려요.
