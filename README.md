# NAMO for Home Assistant

![NAMO - Ain't Motion-Only.](brand/banner.webp)

[![HACS validation](https://github.com/David2766/NAMO-Home-Assistant/actions/workflows/hacs.yml/badge.svg)](https://github.com/David2766/NAMO-Home-Assistant/actions/workflows/hacs.yml)
[![Hassfest](https://github.com/David2766/NAMO-Home-Assistant/actions/workflows/hassfest.yml/badge.svg)](https://github.com/David2766/NAMO-Home-Assistant/actions/workflows/hassfest.yml)
[![Release](https://img.shields.io/github/v/release/David2766/NAMO-Home-Assistant?sort=semver)](https://github.com/David2766/NAMO-Home-Assistant/releases)
[![License](https://img.shields.io/badge/license-AGPL--3.0--or--later-blue)](LICENSE)

Home Assistant custom integration for the fully local
[NAMO](https://github.com/David2766/NAMO-aint-motion-only) mmWave spatial
presence platform.

> This integration is a public preview. Fresh HACS installation, upgrade,
> DHCP discovery, and physical leader-handover verification remain release
> validation work.

## Features

- One Home Assistant config entry per stable NAMO Site.
- One Home Assistant device per logical Space.
- Occupancy, motion, target count, fusion status, health, and device-count
  entities.
- Stable entity identities across Configuration Owner and Group Leader
  handovers.
- Canonical floorplan automation-area occupancy entities.
- Local polling only; no cloud service is required.
- Persistent Site problems reported through Home Assistant Repairs.

## Install with HACS

Until NAMO is included in the HACS default list, add this repository manually.

1. Open **HACS** in Home Assistant.
2. Open the menu in the upper-right corner and select **Custom repositories**.
3. Add `https://github.com/David2766/NAMO-Home-Assistant` as an
   **Integration** repository.
4. Install **NAMO** and restart Home Assistant.
5. Open **Settings > Devices & services > Add integration** and select
   **NAMO**.
6. Confirm the discovered Site or enter the address of any NAMO device in that
   Site, for example `192.168.1.25`.

Only one device address is needed for a Site. Do not add every physical NAMO
node separately.

## Manual installation

Copy the complete `custom_components/namo` directory into the Home Assistant
configuration directory:

```text
/config/custom_components/namo/
```

Restart Home Assistant, then add **NAMO** from **Settings > Devices & services**.

## Security

NAMO is designed for trusted local networks. Never expose a NAMO device or its
embedded dashboard directly to the public internet. Use a properly authenticated
VPN when remote access is required.

## Documentation and support

- [NAMO user wiki](https://github.com/David2766/NAMO-aint-motion-only/wiki)
- [Home Assistant guide](https://github.com/David2766/NAMO-aint-motion-only/wiki/Home-Assistant)
- [Integration issues](https://github.com/David2766/NAMO-Home-Assistant/issues)
- [Firmware and hardware repository](https://github.com/David2766/NAMO-aint-motion-only)

## License

AGPL-3.0-or-later. See [LICENSE](LICENSE).

---

# NAMO Home Assistant 연동

완전한 로컬 방식의 mmWave 공간 재실 플랫폼
[NAMO](https://github.com/David2766/NAMO-aint-motion-only)를 Home Assistant에
연결하는 사용자 정의 통합입니다.

> 이 연동은 공개 미리보기 상태입니다. HACS 신규 설치와 업데이트, DHCP 자동
> 발견 및 실제 기기 역할 승계 검증이 릴리스 검증 항목으로 남아 있습니다.

## 주요 기능

- 안정적인 NAMO Site 하나당 Home Assistant 설정 항목 하나를 생성합니다.
- 논리적인 Space마다 Home Assistant 기기 하나를 생성합니다.
- 재실, 움직임, 타깃 수, 융합 상태, 상태 진단 및 기기 수 엔티티를 제공합니다.
- Configuration Owner 또는 Group Leader가 승계되어도 엔티티 식별자를 유지합니다.
- 평면도에 저장된 공용 자동화 영역의 재실 엔티티를 제공합니다.
- 클라우드 없이 로컬 네트워크에서 상태를 읽습니다.
- Site의 비정상 상태가 지속되면 Home Assistant Repairs로 알립니다.

## HACS로 설치

HACS 기본 목록에 등록되기 전까지는 저장소를 직접 추가해야 합니다.

1. Home Assistant에서 **HACS**를 엽니다.
2. 오른쪽 위 메뉴에서 **Custom repositories**를 선택합니다.
3. `https://github.com/David2766/NAMO-Home-Assistant`를 입력하고 유형은
   **Integration**을 선택합니다.
4. **NAMO**를 설치하고 Home Assistant를 다시 시작합니다.
5. **설정 > 기기 및 서비스 > 통합 구성요소 추가**에서 **NAMO**를 선택합니다.
6. 자동 발견된 Site를 확인하거나 같은 Site에 연결된 NAMO 기기 하나의 주소를
   입력합니다. 예: `192.168.1.25`

Site 하나에는 기기 주소 하나만 입력하면 됩니다. 모든 물리 NAMO 기기를 각각
등록하지 마세요.

## 수동 설치

`custom_components/namo` 폴더 전체를 Home Assistant 설정 디렉터리의 다음
경로에 복사합니다.

```text
/config/custom_components/namo/
```

Home Assistant를 다시 시작한 뒤 **설정 > 기기 및 서비스**에서 NAMO를 추가합니다.

## 보안

NAMO는 신뢰할 수 있는 로컬 네트워크 사용을 전제로 합니다. NAMO 기기나 내장
대시보드를 공개 인터넷에 절대로 직접 노출하지 마세요. 외부 접속이 필요하다면
올바르게 인증된 VPN을 사용하세요.

## 문서와 지원

- [NAMO 사용자 위키](https://github.com/David2766/NAMO-aint-motion-only/wiki)
- [Home Assistant 안내](https://github.com/David2766/NAMO-aint-motion-only/wiki/Home-Assistant-ko)
- [Integration 문제 보고](https://github.com/David2766/NAMO-Home-Assistant/issues)
- [펌웨어 및 하드웨어 저장소](https://github.com/David2766/NAMO-aint-motion-only)

## 라이선스

AGPL-3.0-or-later. 자세한 내용은 [LICENSE](LICENSE)를 참고하세요.
