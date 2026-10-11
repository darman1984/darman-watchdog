# darman-watchdog

다르만 스튜디오 바깥 감시와 Azure DR 손잡이(GitHub Actions).

- `watch` — 15분마다 공개 주소 확인, 10분 넘게 응답이 없으면 메일, 살아나면 메일. **15분 실행은 Cloudflare Worker `darman-cron` 이 workflow_dispatch 로 깨운다**(GitHub 예약 실행이 이 계정에서 몇 시간씩 밀려서, 2026-10-11). 아래 schedule 은 예비.
- `DR 전환` — 사람이 실행: status / failover / drill.

설정 값은 모두 저장소 Secrets 에 있습니다.
