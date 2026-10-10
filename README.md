# C30 Social Publisher — public update channel

이 저장소는 C30 Social Publisher의 **업데이트 정보와 설치 파일만** 공개합니다. 앱 소스 코드는 비공개 저장소에 있으며 여기에 없습니다.

- `stable/latest.json` — 현재 릴리스의 업데이트 정보(`c30-update/1` 형식). 앱의 설정 → 정보 → **지금 업데이트 확인**을 누를 때만 읽습니다.
- `test/*.json` — 업데이트 검증용 테스트 manifest(해시·크기 불일치, 형식 오류, 다운그레이드, 허용되지 않은 호스트). 앱이 모두 거부해야 합니다.
- Releases — 버전별 NSIS 설치 파일(현재 코드 서명 없음).

앱은 설치 파일을 자동으로 내려받거나 설치하지 않습니다. 설치 전에 SHA-256이 `stable/latest.json`의 값과 같은지 확인하세요:

```powershell
Get-FileHash .\C30-Social-Publisher_<version>_x64-setup.exe -Algorithm SHA256
```

This repository publishes only update metadata and installers for C30 Social Publisher. The application source is private and not included.