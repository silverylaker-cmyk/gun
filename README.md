# Finger Gun: Dead Alley

핸드폰 카메라로 손을 인식해 플레이하는 웹 레일슈터(버추어 캅 / 하우스 오브 더 데드 스타일).

## 조작
- **조준**: 한 손으로 총 모양(검지 펴기)을 만들면 검지 끝이 조준점이 됩니다.
- **발사**: 반대손 검지(또는 엄지)로 총 손을 터치하면 한 발 발사됩니다. (터치할 때마다 1발)
- **재장전**: 손을 카메라 범위 밖으로 내리면 약 0.5초 후 자동 재장전됩니다. 탄창 6발.

## 실행
정적 파일 하나(`index.html`)입니다. 카메라 API 때문에 **HTTPS**(또는 localhost)에서 열어야 합니다.

- GitHub Pages로 배포하거나
- 로컬: `npx serve .` 후 같은 Wi-Fi의 폰에서 접속 (HTTPS 필요 시 `npx serve --ssl-cert ...` 또는 ngrok 사용)

## 기술
- [MediaPipe Hand Landmarker](https://ai.google.dev/edge/mediapipe/solutions/vision/hand_landmarker) (CDN, 브라우저 내 추론, 서버 불필요)
- Canvas 2D 렌더링, Web Audio 합성 효과음 (외부 에셋 없음)
