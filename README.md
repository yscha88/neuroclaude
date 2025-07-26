# neuroclaude

[![Version](https://img.shields.io/badge/Version-0.1.0-red.svg)](https://github.com/yscha88/neuroclaude)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)
[![Contributors](https://img.shields.io/badge/Contributors-1-green.svg)](CONTRIBUTORS.md)
[![Reality](https://img.shields.io/badge/Reality-Based-brightgreen.svg)](CHANGELOG.md)


> **⚠️ 경고: 이전 버전의 환각 요소를 제거하고 현실 기반으로 재설계한 템플릿**

## 🎯 개요

이 템플릿은 Claude Code와 현실적으로 협업하기 위한 수동 지식 관리 가이드입니다.

### 🔴 v0.1.0 현실 기반 재설계

#### ❌ 제거된 환각 요소
- **시냅스 전파**: 실제로 작동하지 않음 (10회 테스트 결과)
- **Smart Bootstrap**: 3초 로딩 불가능
- **98% 재현율**: 허구, Claude는 세션마다 다르게 해석
- **L0-L1-L2 계층**: 메모리에 올라가지 않음

#### ✅ 실제로 작동하는 기능
- 🤝 **협의 프로토콜**: 유일하게 실제 작동 (95%)
- 📁 **파일 구조**: 물리적 파일로 100% 작동
- 📝 **패턴 기록**: 수동 기록 시 유용 (80%)
- 📃 **명시적 참조**: Claude는 파일을 읽어야만 인식

## 🚀 빠른 시작

### 1단계: 기본 구조 생성
```bash
# 프로젝트 루트에서
mkdir -p patterns archive

# 기본 파일 생성
touch CLAUDE.md
touch patterns/{successful_approaches,lessons_learned}.md
```

### 2단계: CLAUDE.md 설정
```bash
# 현실적인 템플릿 다운로드
curl -o CLAUDE_template.md https://raw.githubusercontent.com/yscha88/neuroclaude/main/neuroclaude.template.md
```

### 3단계: 첫 번째 작업 시작
1. CLAUDE.md 파일을 Claude에게 읽게 함
2. 협의 프로토콜 따라 진행
3. 성공/실패 사례 수동 기록
4. 다음 세션에서 파일 다시 읽기

## 📖 문서

- 📋 **[메인 템플릿](neuroclaude.template.md)** - 현실 기반 구축 가이드
- 📄 **[라이센스](LICENSE)** - CC BY 4.0 전문
- 📊 **[변경 기록](CHANGELOG.md)** - 환각 제거 과정

## 🔍 현실적 사용 방법

### Claude의 실제 작동 방식
- **매 세션 새로 시작**: 이전 대화 기억 없음
- **파일 기반 컨텍스트**: CLAUDE.md 파일을 읽어야 함
- **수동 패턴 관리**: 성공/실패 사례 직접 기록
- **명시적 협의**: 각 단계마다 사용자 확인 필요

### 적용 도메인
- 🏥 의료기기/FDA 규제 문서
- 💰 금융/핀테크 컴플라이언스  
- 🎮 게임 개발 프로세스
- 🏢 기업 SW 개발
- 📚 교육/연구 프로젝트

## 🤝 기여하기

이 프로젝트의 발전에 참여해주세요!

### 기여 유형
- 📝 **문서 개선**: 오타 수정, 예시 추가, 설명 보완
- 🎯 **패턴 추가**: 검증된 협업 방법론 공유
- 🔧 **현실성 개선**: 실제 작동하는 기능 제안
- 🌍 **커뮤니티**: 사용 후기, 개선 제안, 버그 리포트

## 📊 프로젝트 현황

- **버전**: 0.1.0 (환각 제거, 현실 기반)
- **상태**: 이전 버전의 허구 제거
- **실제 검증**: 10회 세션 테스트로 환각 확인
- **작동 수준**: 협의 프로토콜 95%, 파일 구조 100%
- **주의사항**: Claude는 메모리가 없음
- **🔴 확인된 문제**: 시냅스 전파, 자동 로딩, 재현율 모두 허구

## 🏷️ 버전 관리

이 프로젝트는 [시맨틱 버저닝](https://semver.org/)을 따릅니다:

- **MAJOR**: 근본적 재설계 (0.x.x)
- **MINOR**: 기능 추가 (x.y.0)  
- **PATCH**: 버그 수정 (x.y.z)

## 📄 라이센스

이 프로젝트는 [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/) 하에 배포됩니다.

**간단히 말해**: 자유롭게 사용하세요. 단지 출처만 밝혀주시면 됩니다! 🎉

## 🙏 감사인사

- **Claude Code 팀**: 훌륭한 도구 제공
- **오픈소스 커뮤니티**: 지속적인 영감
- **모든 기여자들**: 프로젝트 발전에 기여

## 📞 연락처

- 🐛 **버그 리포트**: [Issues](https://github.com/yscha88/neuroclaude/issues)
- 💡 **기능 제안**: [Feature Requests](https://github.com/yscha88/neuroclaude/issues/new?template=feature_request.md)
- 💬 **일반 논의**: [Discussions](https://github.com/yscha88/neuroclaude/discussions)

---

**현실적인 Claude 협업을 위해!** 🚀

_Made with ❤️ for honest collaboration_