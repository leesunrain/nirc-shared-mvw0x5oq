화목 훈련 페이스 신규 앱 v1.0
신규 앱이며 기존 Vercel 프로젝트를 변경하지 않습니다.
배포 방법: Vercel에서 신규 프로젝트를 1회 생성하고 이 폴더의 파일을 루트에 배포하세요.
기존 앱 업데이트가 아닙니다. 실제 서버 배포는 수행하지 않았습니다.
사용자 입력은 각 기기의 localStorage에 저장됩니다.
입력: 3930 또는 39:30. 파트 + 추가 / - 삭제, 최소 1개, 최대 30개.
공유: 브라우저 지원 시 공유 시트, 아니면 PNG 다운로드.

[v1.1] 4930 / 49:30 / 49분30초 입력 지원. Enter 확정 후 다음 PART로 포커스 이동.
기존 앱 업데이트 시 기존 Vercel projectId와 Production URL 확인 후 동일 프로젝트 Production에 배포하세요. 새 프로젝트 생성 금지. 기존 PWA 및 localStorage 데이터 유지.

[v1.2] VO₂max 90% / LT 인터벌 모두 400m, 200m, 100m 각각 원래 계산값에서 정수 반올림하여 표시. 이미지도 동일. 계산 단계에서 미리 반올림하지 않음.
배포 전 확인: 기존 projectId, Production URL, Production 대상, PWA manifest, 사용자 데이터 저장(localStorage key: nirc-tue-thu-pace-v1).
배포 후 확인: 기존 URL 최신 버전, 페이스 표시 및 이미지, 홈 화면 바로가기, 기존 기록 보존. 이 ZIP은 배포가 아님.

[v1.3] 거리별 독립 계산 확정: 10K 총 초 / 10 + (VO₂max -10 또는 LT +10) = 1km 목표 초. 400/200/100m 각각 비례 계산 후 Math.round로 정수 반올림. 100m 반올림값을 배수로 곱하지 않음. 기존 localStorage 키 및 PWA manifest 유지.
기존 Vercel projectId 및 Production URL은 이 파일만으로 확인할 수 없으므로 배포 전에 기존 프로젝트에서 확인 필요. Production 배포 후 기존 URL에서 검증 필요.

[v1.3] 확인된 계산 방식 유지: 10K 기록에서 1km 훈련 페이스를 구한 뒤 400m/200m/100m 각각 독립 계산 및 정수 반올림. 100m 반올림 결과를 배수로 사용하지 않음.
기존 Vercel projectId 및 Production URL은 ZIP만으로 확인할 수 없으므로 배포 전 확인 필요.

[v1.4] PART별 입력 옆에 기본 10K/km 페이스, 훈련 보정(±10초/km), 훈련 페이스 표시. 이미지 공유 대상은 PART별 체크박스로 1개 이상 자유 선택(예: PART 2·3만). 기존 로컬 저장 키, PWA manifest/start_url/scope 유지.
기존 프로젝트 업데이트 전 Vercel projectId 및 Production URL 확인 필요. ZIP 생성은 배포가 아니며 기존 URL/홈 화면/데이터 검증은 배포 후 별도 수행.

[v1.5] 기존 v1.4 업데이트: 목요일 LT 페이스만 변경.
35~60분의 지정 예시 9개를 정확히 재현하도록 기준점 사이를 선형 보간함.
기준점 (10K 기록 → LT 보정): 35:+7, 38:+9, 40:+10, 42:+11, 45:+13, 48:+15, 50:+16, 55:+19, 60:+22 (초/km).
이것은 사용자 제공 기준표에 맞춘 경험적 보간이며 Jack Daniels 공식 VDOT T-pace 또는 측정 LT2가 아님.
35분 미만 또는 60분 초과는 기존 +10초/km 사용하고 별도 검토 안내.
화요일 VO2max -10초/km, 거리별 독립 반올림, PART, Enter, 이미지 선택 공유는 변경하지 않음.
localStorage 키 nirc-tue-thu-pace-v1 및 manifest/start_url/scope/icon 유지. 서비스워커 캐시 v1.5.
Vercel 프로젝트 정보: 미확인. 검색된 pace-lap-calculator 및 nirc-6min-pace는 본 앱으로 확정할 근거가 없어 연결하지 않음.
배포 절차: 1) 기존 앱의 정확한 Vercel projectId와 Production URL 확인 2) 동일 프로젝트 Production에 이 ZIP 루트 파일 업데이트 3) 기존 URL에서 버전 v1.5, 9개 기준값, 공유 이미지, 기존 데이터와 홈 화면 바로가기 검증.
이 ZIP 파일은 배포 완료를 뜻하지 않음. 실제 배포 및 운영 URL 검증 미실시.
