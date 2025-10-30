---
source-git-commit: 08eaa7ae974c134ea2e920a1fa854dcf6a971e18
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---
# 🚀 커서 에이전트를 설치하는 중

커서 에이전트는 설명서를 보다 효율적으로 만들고 유지 관리하는 데 도움이 되는 공유 도구입니다.

## 최초 설정

이 작업은 저장소당 **한 번**&#x200B;만 수행하면 됩니다.

### 옵션 1: 커서 사용(권장 ⭐)

1. 커서 채팅 열기(`Cmd+L` 또는 `Ctrl+L`)
2. 유형:

   ```
   @setup-agents
   ```

3. 에이전트는 자동으로 다음을 수행합니다.
   - SSH 및 HTTPS 액세스 테스트
   - 작업 메서드 사용
   - 필요한 경우 설정 과정을 안내합니다.
4. 완료! ✨

**참고:** 에이전트가 `git.corp.adobe.com`에 대한 SSH 또는 HTTPS 액세스 권한이 있는지 자동으로 감지하여 적절한 메서드를 사용합니다. 둘 다 작동하지 않는 경우 안내식 설정을 제공합니다.

### 옵션 2: 터미널 사용

1. 저장소 루트에서 터미널 열기
2. 실행:

   ```bash
   ./setup-agents.sh
   ```

   스크립트는 자동으로
   - SSH 및 HTTPS 액세스 테스트
   - 작업 메서드 사용
   - 필요한 경우 설치 지침 표시

   또는 수동으로(git이 구성된 것을 알고 있는 경우):

   ```bash
   git submodule update --init --recursive
   ```

3. 완료! ✨

## 확인

설치 후 설치를 확인합니다.

```bash
ls .cursor-agents/agents/
```

다음이 표시됩니다.
- `draft-page-generator.md`
- `fix-grammar.md`
- 등

## 사용

설치가 완료되면 커서에서 에이전트를 사용할 수 있습니다.

```
@draft-page      # Generate a new documentation page
@fix-grammar     # Fix grammar in current file
```

사용 가능한 에이전트의 전체 목록은 [AGENTS.md](AGENTS.md)을(를) 참조하십시오.

## 에이전트 업데이트

모든 에이전트의 최신 버전을 다운로드하려면:

### 옵션 1: 커서 사용

```
@update-agents
```

### 옵션 2: 터미널 사용

```bash
git submodule update --remote
```

## 문제 해결

### &quot;에이전트를 찾을 수 없음&quot; 오류

이 오류가 표시되면 에이전트가 아직 설치되지 않은 것입니다. 실행:

```
@setup-agents
```

### 하위 모듈이 비어 있습니다.

`.cursor-agents/`이(가) 있지만 비어 있는 경우:

```bash
git submodule update --init --recursive --remote
```

### 권한 거부됨

설치 스크립트가 실행 가능한지 확인합니다.

```bash
chmod +x setup-agents.sh
```

### 네트워크/VPN 문제

- Adobe VPN에 연결되어 있는지 확인
- 네트워크 연결 확인
- Git 액세스 확인:

  ```bash
  git ls-remote https://git.corp.adobe.com/AdobeDocs/CursorAgents
  ```

## 작동 방법

커서 에이전트가 **git 하위 모듈**(으)로 배포됩니다.

```
your-repo/
  ├── .cursor-agents/          ← Git submodule
  │   ├── agents/
  │   │   ├── draft-page-generator.md
  │   │   └── fix-grammar.md
  │   └── AGENTS.md
  ├── setup-agents.sh          ← Setup script
  └── your-content/
```

하위 모듈은 다음을 가리킵니다.
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

이를 통해 모든 사용자가 동일한 최신 에이전트를 사용할 수 있습니다.

## 유지 관리용

### 새 저장소에 추가

1. 하위 모듈을 추가합니다.

   ```bash
   git submodule add https://git.corp.adobe.com/AdobeDocs/CursorAgents.git .cursor-agents
   ```

2. 설치 파일 복사:
   - `setup-agents.sh`
   - `setup-agent.md`(하위 모듈이 아니라 루트에 배치)
   - `INSTALL.md`

3. 커밋:

   ```bash
   git add .gitmodules .cursor-agents setup-agents.sh
   git commit -m "Add Cursor Agents submodule"
   ```

### 중앙 저장소 업데이트

에이전트에 대한 변경 내용은 다음 위치에서 이루어져야 합니다.
**https://git.corp.adobe.com/AdobeDocs/CursorAgents**

모든 리포지토리는 `git submodule update --remote`을(를) 통해 업데이트를 받습니다.

&#x200B;---

**도움이 필요하십니까?** 설명서 팀장에게 문의하거나 내부 wiki를 확인하십시오.
