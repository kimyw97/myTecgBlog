### 날짜와 시간

- 날짜: 2024-01-24
- 시간: 10:27

### 주제 또는 키워드
- [[Angular]]
- [[service-worker]]
- 서비스 워커 통신

### 간단한 내용
- SwUpdate 서비스
	- 서버에 새 버전을 확인 했을때 로컬에 설치하고 준비되었을 때, 설치 실패했을 때 알림을 보냄
	- 서버에 새 버전이 있는지 확인할 수 있음
	- 현재 탭에서 실행중인 애플리케이션을 최신 버전으로 갱신할 수 있음

1. 버전 업데이트

|이벤트 타입|설명|
|:--|:--|
|`[VersionDetectedEvent]` |서비스 워커가 서버에 새로운 앱 버전이 있다는 것을 확인했고 내려받기 시작할 때 보내는 이벤트입니다.|
|`[NoNewVersionDetectedEvent]` |서비스 워커가 서버를 확인했고 새로운 버전이 존재하지 않을 때 보내는 이벤트입니다.|
|`[VersionReadyEvent]` |클라이언트에서 앱을 새로운 버전으로 재시작할 수 있을 때 보내는 이벤트입니다. 사용자에게 화면을 갱신하도록 요청하는 용도로 사용합니다.|
|`[VersionInstallationFailedEvent]` |새 버전 앱 설치를 실패했을 때 보내는 이벤트입니다. 모니터링, 로그 용도로 사용합니다.|
```typescript
@Injectable({providedIn: 'root'})
export class LogUpdateService {

  constructor(updates: SwUpdate) {
    updates.versionUpdates.subscribe(evt => {
      switch (evt.type) {
        case 'VERSION_DETECTED':
          console.log(`Downloading new app version: ${evt.version.hash}`);
          break;
        case 'VERSION_READY':
          console.log(`Current app version: ${evt.currentVersion.hash}`);
          console.log(`New app version ready for use: ${evt.latestVersion.hash}`);
          break;
        case 'VERSION_INSTALLATION_FAILED':
          console.log(`Failed to install app version '${evt.version.hash}': ${evt.error}`);
          break;
      }
    });
  }
}
```

2. 업데이트 확인하기
- 서버에 새로운 애플리케이션이 배포 되었는지 서비스 워커로 확인
- 서비스 워커가 초기화 될때, 사용자가 앱안에서 다른 주소로 이동할 때 확인, 개발자가 원하는 주기로 업데이트 되었는지 확인  가능
- `checkForUpdate()`함수로 확인 가능

3. 최신 버전으로 업데이트하기
4. 복구할 수 없는 상태 처리하기

### 코드 스니펫 (선택)

```typescript
```
