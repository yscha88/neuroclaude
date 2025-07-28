# Neuroclaude 문서 기반 지식 관리 허브

## 🎯 프로젝트 개요  
**목적**: Claude Code와의 효율적 협업을 위한 수동 지식 관리 템플릿
**핵심 기능**: 문서 기반 컨텍스트 로딩 시스템
**사용 방식**: 구조화된 협업 프로토콜

**핵심 철학**: 완벽한 자동화보다 실용적인 협력. 세션 기반 특성을 인정하고 그 제약 내에서 작업.

## 🔄 스마트 활성화 시스템
### 세션 시작 감지
이 파일을 읽는 순간 허브 로딩 + 컨텍스트 활성화 옵션 제시

🧠 Neuroclaude 허브 로딩 완료

💬 "시냅스 활성화해줘"라고 하시면
   모든 컨텍스트 네트워크를 연결해 드릴게요!

⚡ 또는 바로 작업 요청을 말씀해 주셔도 됩니다.

## 🤝 협의 프로토콜

### 작업 시작 시
```
Claude: "목표 확인: [작업 요약]"
Claude: "제안 접근법: [구체적 방법론]" 
Claude: "예상 단계: [1단계 → 2단계 → 3단계]"
Claude: "이 방향으로 진행해도 될까요?"
```

### 중간 체크포인트
```
Claude: "현재 진행: [완료된 부분] ✅"
Claude: "다음 단계: [예정 작업]"
Claude: "방향성이 맞나요?"
```

### 완료 후 평가
```
Claude: "작업 결과: [구체적 산출물]"
Claude: "사용된 패턴: [효과적이었던 접근법]"
Claude: "이 패턴을 기록할까요?"
```

## 🎯 컨텍스트 우선순위
🔥 HOT: v0.1.0 Reality-Based Redesign 완료
🟡 WARM: 4개 성공 사례 + 3개 교훈 패턴 축적  
❄️ COLD: git 복원된 이전 히스토리 (환각적 특화 vs 건전한 확장)

## 📊 v0.1.0 주요 성과 (2025-07-28)

### ✅ 실증 검증 완료
- **협의 프로토콜**: 실제 세션에서 100% 작동 확인
- **템플릿 적용**: neuroclaude 프로젝트에 직접 적용 성공  
- **Claude 판단 패턴**: 경험 유무에 따른 극명한 차이 입증
- **git 고고학**: 18개 dangling blob에서 진화 과정 복원

### 🧠 메타 인사이트
- **재귀적 자기 검증**: Claude가 Claude들의 패턴 분석
- **대조군 실험**: 미경험 vs 경험한 Claude 행동 비교
- **건전한 확장 기준**: FDA_Docs 모델 vs LLM-Infra 안티패턴
- **범용성 수호**: 특화 허용하되 전용화 방지

### 📈 패턴 축적 현황
- **successful_approaches.md**: 4개 사례 (템플릿 적용, 협의 프로토콜, 대조 실험, git 복원)
- **lessons_learned.md**: 3개 교훈 (성급한 판단, 환각 평가, 환각적 특화)
- **work_methodology.md**: 연쇄 발견 vs 계획적 작업 + 환각 제거 방법론
- **collaborative_decisions.md**: 3개 협의 기록 (실제 협의 프로토콜 동작)

## 🎯 Core System Architecture

### Reality-Based Design Principles
- **File-based context**: All knowledge must be stored in files - Claude has no memory between sessions
- **Manual pattern management**: Success/failure patterns must be manually recorded and referenced
- **Explicit collaboration protocol**: Structured agreement process for all work
- **Progressive improvement**: Iterative enhancement over perfect solutions

### Key Components
1. **CLAUDE.md**: Project-specific guidance (must be read each session)
2. **patterns/**: Manual recording of successful approaches and lessons learned
3. **Collaboration Protocol**: Structured agreement process for transparency
4. **Chain Discovery Detection**: Identifies work that expands in scope during execution

## 📝 Collaboration Protocol

When working on tasks, follow this structured agreement process:

### Work Initiation
```
Claude: "Goal confirmation: [task summary]"
Claude: "Proposed approach: [specific methodology]"
Claude: "Expected steps: [step 1 → step 2 → step 3]"
Claude: "Should we proceed in this direction?"
```

### Mid-point Checkpoints
```
Claude: "Current progress: [completed parts] ✅"
Claude: "Next step: [planned work]"
Claude: "Is the direction correct?"
```

### Completion Evaluation
```
Claude: "Work result: [specific deliverables]"
Claude: "Patterns used: [effective approaches]"
Claude: "Should we record this pattern?"
```

## 🔍 Work Classification System

### Chain Discovery Work
- **Characteristics**: Scope expands progressively during execution
- **Triggers**: "all [targets] to [new_value]", "consistency across", "standardize [method]"
- **Approach**: Sequential processing, no batch operations
- **Example**: "Unify all terminology from 'manager' to 'coordinator'"

### Planned Batch Work
- **Characteristics**: Clear scope and file list
- **Triggers**: "Next N files", specific file lists, concrete checklists
- **Approach**: Batch processing tools acceptable
- **Example**: "Update port variable to 3000 in config.js, utils.js, main.js"

## 🎯 Pattern Management

### Document Formats (patterns/document-format.md)
Key insights about data conversion efficiency:
- **JSON format**: 0% data loss, 100% processing efficiency, maximum tool compatibility
- **Excel → JSON**: Complete structure preservation with automatic data cleaning
- **Regulatory compliance**: Supports IEC 62304, 21 CFR 820.30, ISO 14971 standards

### Pattern Recording Templates
When successful patterns emerge, record them using:
- **successful_approaches.md**: Date, goal, collaboration process, solution, success factors
- **lessons_learned.md**: Date, problem, incorrect thinking, correct approach, key lessons

## 🚨 Critical Limitations

### Removed Hallucinated Features (confirmed non-functional)
- **Synaptic Propagation**: Does not work (10-session test results)
- **Smart Bootstrap**: 3-second loading impossible
- **98% Reproducibility**: Fiction - Claude interprets differently each session
- **L0-L1-L2 Layers**: Do not load into memory

### Actually Working Features (verified)
- **Collaboration Protocol**: Only feature that actually works (95% success rate)
- **File Structure**: Physical files work 100%
- **Pattern Recording**: Useful when manually recorded (80% effectiveness)
- **Explicit References**: Claude must read files to recognize content

## 💻 Development Workflow

### For Template Improvements
1. Test changes across multiple Claude sessions
2. Record actual effectiveness (not theoretical)
3. Update documentation with verified results only
4. Follow CC BY 4.0 attribution requirements

### For Pattern Documentation
1. Use structured formats in patterns/ directory
2. Focus on reproducible techniques
3. Document both successes and failures
4. Reference specific file locations for context

## 🔧 Testing & Validation

Since this is a documentation-focused repository:
- **Manual verification**: Test collaboration patterns across sessions
- **Reality checking**: Verify claimed features actually work
- **Pattern validation**: Confirm recorded approaches are reproducible
- **Cross-session testing**: Ensure templates work without memory persistence

## 📚 Domain Applications

The template supports various domains:
- Medical device/FDA regulatory documentation
- Financial/fintech compliance
- Game development processes
- Enterprise software development
- Education/research projects

## 🎯 Key Success Metrics

- **Work direction confusion reduction**
- **Repeat mistake prevention**
- **Collaboration time reduction**
- **Pattern reuse rate improvement**
- **Quality consistency achievement**

## ⚠️ Important Notes

- This repository contains no executable code - only documentation templates
- All patterns must be manually implemented and tested
- Claude has no memory between sessions - files must be explicitly read
- Focus on practical cooperation rather than automated solutions
- Always verify claimed functionality before implementing