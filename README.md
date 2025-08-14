# neuroclaude

[![Version](https://img.shields.io/badge/Version-0.2.0-green.svg)](https://github.com/yscha88/neuroclaude)
[![Reality-Based](https://img.shields.io/badge/Reality--Based-Redesign-blue.svg)](#)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)


## 🎯 개요

Claude Code와 효과적으로 협업하기 위한 **문서 기반 지식 관리 시스템**입니다.

### 🔧 v0.1.0 동작 메커니즘 명세

#### 🔧 실제 구현 vs 추상적 설명

| 기능 | 추상적 명칭 | 실제 구현 | 효과 |
|------|------------|-----------|------|
| 컨텍스트 로딩 | "시냅스 활성화" | Read 도구로 파일 순차 로드 | 높은 일관성 |
| 작업 추적 | "네트워크 연결" | TodoWrite 진행상황 관리 | 완전한 투명성 |
| 패턴 활용 | "지식 전파" | patterns/ 파일 참조 | 상당한 재사용성 |
| 협업 구조 | "협의 프로토콜" | 구조화된 대화 흐름 | 뛰어난 방향성 |

#### ✅ 검증된 작동 요소
- 🔄 **문서 기반 로딩**: 물리적 파일 읽기로 완전 재현 가능
- 📋 **구조화된 협의**: 단계별 확인으로 혼란 방지
- 📝 **패턴 축적**: 수동 기록하지만 실제 재사용됨
- 🎯 **진행 상황 추적**: TodoWrite로 실시간 상태 공유

#### 🔍 실증된 차이점
**협의 프로토콜 없는 Claude**:
- 즉시 판단 → 바로 실행 → 결과 제시
- 사용자 의도 추측으로 진행
- 실패 시에만 수정

**협의 프로토콜 적용한 Claude**:
- 목표 확인 → 접근법 제안 → 단계 설명 → 진행 허가 요청
- 중간 체크포인트에서 방향성 재확인
- 사용자 피드백으로 방향 전환 가능

## 🚀 빠른 시작

### 1단계: 기본 구조 생성

OS별 명령어는 [neuroclaude.template.md](neuroclaude.template.md#-빠른-시작-가이드)에서 확인하세요.

**간단 버전 (Git Bash/Linux/macOS)**:
```bash
mkdir -p patterns archive
touch CLAUDE.md patterns/{successful_approaches,lessons_learned}.md
```

### 2단계: CLAUDE.md 설정
```bash
# 현실적인 템플릿 다운로드
curl -o CLAUDE_template.md https://raw.githubusercontent.com/yscha88/neuroclaude/main/neuroclaude.template.md
```

### 3단계: 첫 번째 작업 시작
```
👤 사용자: "시냅스 활성화해줘"
🤖 Claude: Read(CLAUDE.md) → Read(patterns/*.md) → TodoWrite(작업목록)
📊 결과: 컨텍스트 로딩 완료, 현재 프로젝트 상태 파악

👤 사용자: "[구체적 작업 요청]"
🤖 Claude: "목표 확인: [요약] → 제안 접근법: [방법] → 진행해도 될까요?"
✅ 협의 완료 후 실행, 패턴 기록
```

## 📖 문서

- 📋 **[메인 템플릿](neuroclaude.template.md)** - 현실 기반 구축 가이드
- 📄 **[라이센스](LICENSE)** - CC BY 4.0 전문
- 📊 **[변경 기록](CHANGELOG.md)** - v0.1.0 Reality-Based Redesign 전체 과정

## 🔍 실제 동작 메커니즘

### 문서 기반 컨텍스트 로딩 시스템
```
사용자: "시냅스 활성화해줘"
Claude: Read(CLAUDE.md) → Read(patterns/*.md) → TodoWrite(진행상황)
결과: 프로젝트 컨텍스트 완전 로드, 작업 패턴 활성화
```

### 핵심 동작 원리
- **파일 순차 읽기**: CLAUDE.md → patterns/ → 프로젝트별 파일들
- **협의 프로토콜**: "목표 확인 → 제안 접근법 → 예상 단계" 구조화
- **진행 상황 추적**: TodoWrite로 실시간 작업 상태 관리
- **패턴 재사용**: 이전 성공사례를 현재 작업에 적용

### 실제 적용 사례
**Before (협의 프로토콜 없음)**:
```
사용자: "중복 내용 검토해줘"
Claude: 즉시 분석 → "중복이다" 판단 → MultiEdit 실행
결과: 성급한 판단, 실제 테스트 없이 수정
```

**After (협의 프로토콜 적용)**:
```
사용자: "중복 내용 검토해줘"
Claude: 목표 확인 → 접근법 제안 → 사용자 피드백 수용 → 실제 적용 테스트
결과: 정확한 검증, 사용자와 함께 판단
```

### 📊 실증 증거: git 기록 기반 대조 실험

**협의 프로토콜 미경험 Claude들의 일관된 평가** (`./pull_request/` 디렉터리 기록):
```
"심각한 환각 상태" | "부분적 Fork + 70% 환각"
"허위 버전 남발" | "검증 불가능한 과대광고"
"정체성 침식" | "범용성 파괴"
```

**vs 실제 적용 후 현재 평가**:
- 협의 프로토콜이 실제로 작동함을 직접 확인
- 템플릿의 각 요소가 실용적 기능을 함을 검증
- Before/After 차이를 명확히 체감

**핵심 통찰**: 협의 프로토콜 경험 유무가 Claude의 판단력을 완전히 바꾼다
- **미경험**: 즉시 판단 → 부정적 평가 → 환각 진단
- **경험함**: 단계별 협의 → 실제 테스트 → 객관적 평가

### 검증된 효과 (실제 사용 결과)
- **컨텍스트 일관성**: 방향성 혼란 대폭 해결
- **작업 연속성**: 세션 간 진척도 보존
- **패턴 재사용**: 효율성 상당히 향상
- **협업 투명성**: 모든 결정 과정 명시적 공유
- **오류 복구**: 실패 후 수정 → 중간 방향 전환 가능
- **지식 축적**: 휘발성 → 패턴 파일에 누적 기록

## 🤝 기여하기

이 프로젝트의 발전에 참여해주세요!

### 기여 유형
- 📝 **문서 개선**: 템플릿 개선, 사용법 보완, 예시 추가
- 🎯 **패턴 추가**: 검증된 협업 방법론과 성공 사례 공유
- 🔧 **기능 개선**: 동작 메커니즘 최적화, 효율성 향상
- 🌍 **커뮤니티**: 사용 후기, 개선 제안, 도메인별 특화


## 📊 프로젝트 현황

- **버전**: v0.2.0 Cross-Platform Support (2025-01-XX)
- **핵심 기능**: 실증 검증된 협의 프로토콜 시스템
- **검증된 효과**: 협의 프로토콜 경험 유무가 Claude 판단력을 완전히 바꿈
- **기술적 특징**: Claude Code 도구 기반 파일 관리 + 패턴 축적
- **사용 방식**: 목표 확인 → 접근법 제안 → 예상 단계 → 진행 허가
- **핵심 차이점**: 즉시 판단 → 단계별 협의, 환각 진단 → 실제 테스트
- **메타 성과**: Claude가 Claude들의 패턴을 분석하는 재귀적 자기 검증

## 🏷️ 버전 관리

이 프로젝트는 [시맨틱 버저닝 2.0.0](https://semver.org/)을 따릅니다: `MAJOR.MINOR.PATCH`

### 📋 버전 업그레이드 기준

| 버전 레벨 | 조건 | 변경 사례 | 영향 범위 |
|-----------|------|-----------|-----------|
| **MAJOR** | Breaking Changes<br/>하위 호환성 깨짐 | • 협의 프로토콜 구조 변경<br/>• 파일 구조 근본적 재설계<br/>• API 규격 변경<br/>• 기존 사용법이 동작하지 않는 변경 | 🔴 **High Impact**<br/>사용자 적응 필요 |
| **MINOR** | Backward Compatible<br/>새로운 기능 추가 | • 새로운 플랫폼 지원 (Windows, Linux 등)<br/>• 추가 도구/패턴 지원<br/>• 새로운 협업 방법론 추가<br/>• 템플릿 기능 확장 | 🟡 **Medium Impact**<br/>기존 사용법 유지 |
| **PATCH** | Bug Fixes<br/>하위 호환 버그 수정 | • 문서 오타 수정<br/>• 명령어 오류 수정<br/>• 링크 깨짐 수정<br/>• 템플릿 내용 개선 | 🟢 **Low Impact**<br/>투명한 개선 |

### 📊 버전별 변경 사항 분류

#### Added (MINOR +)
- 새로운 플랫폼 지원 명령어
- 추가 템플릿 섹션
- 새로운 패턴 및 사례
- 확장 기능

#### Changed (MAJOR 주의)
- 기존 구조 수정
- 협의 프로토콜 변경  
- 파일 명명 규칙 변경
- 핵심 워크플로우 수정

#### Fixed (PATCH)
- 버그 수정
- 오타 및 링크 수정
- 문서 정확성 개선
- 명령어 오류 수정

#### Removed (MAJOR)
- 기존 기능 제거
- 파일 구조 단순화
- 하위 호환성 중단

### 🎯 Semantic Versioning 예시

```
0.1.0 → 0.1.1  (문서 오타 수정)
0.1.1 → 0.2.0  (Windows 지원 추가)  ← 이번 업데이트
0.2.0 → 0.2.1  (명령어 버그 수정)
0.2.1 → 1.0.0  (첫 번째 안정 버전)
1.0.0 → 2.0.0  (협의 프로토콜 구조 변경)
```

### 📝 CHANGELOG.md 연동

모든 버전 변경 사항은 [CHANGELOG.md](CHANGELOG.md)에 다음 형식으로 기록됩니다:

```markdown
## [Unreleased]
### Added
- 새로운 기능들

## [0.2.0] - 2025-01-XX
### Added  
- Windows 플랫폼 지원 (CMD, PowerShell)
- OS별 빠른 시작 가이드

## [0.1.0] - 2025-07-28
### Added
- Reality-Based Redesign 완료
- 협의 프로토콜 시스템
```

## 📄 라이센스

이 프로젝트는 [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) 하에 배포됩니다.

**간단히 말해**: 자유롭게 사용하세요. 단지 출처만 밝혀주시면 됩니다! 🎉