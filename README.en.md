# neuroclaude

[![Version](https://img.shields.io/badge/Version-0.2.0-green.svg)](https://github.com/yscha88/neuroclaude)
[![Reality-Based](https://img.shields.io/badge/Reality--Based-Redesign-blue.svg)](#)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](http://creativecommons.org/licenses/by/4.0/)

## 🎯 Overview

A **document-based knowledge management system** for effective collaboration with Claude Code.

**Core Philosophy**: Practical cooperation over perfect automation

**Reality-Based Design**: Only features that have been actually tested and verified are included.

### 🔧 v0.1.0 Reality-Based Redesign Achievements

| Feature | Abstract Name | Actual Implementation | Effectiveness |
|---------|---------------|----------------------|---------------|
| Context Loading | "Synapse Activation" | Sequential file loading with Read tool | High consistency |
| Progress Tracking | "Network Connection" | TodoWrite progress management | Complete transparency |
| Pattern Reuse | "Knowledge Propagation" | Manual recording in patterns/ files | Significant reusability |
| Collaboration Structure | "Negotiation Protocol" | Structured conversation flow | Excellent directionality |

#### ✅ Verified Working Elements
- 🔄 **Document-based Loading**: 100% reproducible through physical file reading
- 📋 **Structured Negotiation**: Step-by-step confirmation prevents confusion
- 📝 **Pattern Accumulation**: Manual recording but actually reused
- 🎯 **Progress Tracking**: Real-time status sharing via TodoWrite

#### 🔍 Proven Differences
**Claude without Negotiation Protocol**:
- Immediate judgment → direct execution → result presentation
- Proceeds based on user intent guessing
- Correction only after failure

**Claude with Negotiation Protocol Applied**:
- Goal confirmation → approach proposal → step explanation → proceed permission
- Direction reconfirmation at checkpoints
- Can change direction based on user feedback

## 🚀 Quick Start

### Step 1: Create Basic Structure

For OS-specific commands, see [neuroclaude.template.md](neuroclaude.template.md#-quick-start-guide).

**Simple version (Git Bash/Linux/macOS)**:
```bash
mkdir -p .neuroclaude/{patterns,tools,archive,logs}
touch CLAUDE.md
touch .neuroclaude/patterns/{successful_approaches,lessons_learned,work_methodology,collaborative_decisions}.md
```

### Step 2: Setup CLAUDE.md
```bash
# Download realistic template
curl -o CLAUDE_template.md https://raw.githubusercontent.com/yscha88/neuroclaude/main/neuroclaude.template.md
```

### Step 3: Start First Task
```
👤 User: "Activate synapses"
🤖 Claude: Read(CLAUDE.md) → Read(patterns/*.md) → TodoWrite(task list)
📊 Result: Context loading complete, current project status understood

👤 User: "[Specific task request]"
🤖 Claude: "Goal confirmation: [summary] → Proposed approach: [method] → Should we proceed?"
✅ After negotiation completion, execute and record patterns
```

## 🔍 Real Operation Mechanism

### Document-based Context Loading System
```
User: "Activate synapses"
Claude: Read(CLAUDE.md) → Read(patterns/*.md) → TodoWrite(progress)
Result: Complete project context loading, work pattern activation
```

### Core Operating Principles
- **Sequential File Reading**: CLAUDE.md → patterns/ → project-specific files
- **Negotiation Protocol**: "Goal confirmation → Proposed approach → Expected steps" structured
- **Progress Tracking**: Real-time work status management via TodoWrite
- **Pattern Reuse**: Apply previous success cases to current work

### Real Application Case Study
**Before (No Negotiation Protocol)**:
```
User: "Review duplicate content"
Claude: Immediate analysis → "It's duplicate" judgment → MultiEdit execution
Result: Hasty judgment, modification without actual testing
```

**After (Negotiation Protocol Applied)**:
```
User: "Review duplicate content"
Claude: Goal confirmation → Approach proposal → User feedback acceptance → Actual application test
Result: Accurate verification, judgment together with user
```

### 📊 Empirical Evidence: Git Record-based Controlled Experiment

**Consistent Evaluation by Claude Sessions Without Negotiation Protocol Experience** (`./pull_request/` directory records):
```
"Serious hallucination state" | "Partial Fork + 70% hallucination"
"False version proliferation" | "Unverifiable exaggerated claims"
"Identity erosion" | "Universality destruction"
```

**vs Current Evaluation After Actual Application**:
- Confirmed that negotiation protocol actually works through direct experience
- Verified that each element of the template has practical functionality
- Clearly felt the Before/After difference

**Core Insight**: Whether Claude has experience with negotiation protocol completely changes Claude's judgment ability
- **Inexperienced**: Immediate judgment → negative evaluation → hallucination diagnosis
- **Experienced**: Step-by-step negotiation → actual testing → objective evaluation

### Verified Effects (Real Usage Results)
- **Context Consistency**: Major reduction in directional confusion
- **Work Continuity**: Progress preservation between sessions
- **Pattern Reuse**: Significant efficiency improvement
- **Collaboration Transparency**: Explicit sharing of all decision processes
- **Error Recovery**: Failure correction → Mid-course direction change possible
- **Knowledge Accumulation**: From volatile → Pattern file accumulation

## 📖 Documentation

- 📋 **[Main Template](neuroclaude.template.md)** - Reality-based construction guide
- 📄 **[License](LICENSE)** - CC BY 4.0 full text
- 📊 **[Change Log](CHANGELOG.md)** - Complete v0.1.0 Reality-Based Redesign process

## 🤝 Contributing

We welcome your participation in the development of this project!

### Contribution Types
- 📝 **Documentation Improvement**: Template enhancement, usage supplementation, example addition
- 🎯 **Pattern Addition**: Sharing verified collaboration methodologies and success cases
- 🔧 **Feature Improvement**: Operating mechanism optimization, efficiency enhancement
- 🌍 **Community**: Usage reviews, improvement suggestions, domain-specific specialization

### How to Contribute
1. Fork this repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Apply the negotiation protocol in your actual work
4. Record patterns in `ai_docs/patterns/`
5. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
6. Push to the branch (`git push origin feature/AmazingFeature`)
7. Open a Pull Request

## 📊 Project Status

- **Version**: v0.2.0 Cross-Platform Support (2025-01-XX)
- **Core Function**: Empirically verified negotiation protocol system
- **Verified Effect**: Negotiation protocol experience completely changes Claude's judgment ability
- **Technical Features**: Claude Code tool-based file management + pattern accumulation
- **Usage Method**: Goal confirmation → Approach proposal → Expected steps → Proceed permission
- **Core Difference**: Immediate judgment → Step-by-step negotiation, hallucination diagnosis → actual testing
- **Meta Achievement**: Recursive self-verification where Claude analyzes patterns of Claudes

## 🏷️ Version Management

This project follows [Semantic Versioning 2.0.0](https://semver.org/): `MAJOR.MINOR.PATCH`

### 📋 Version Upgrade Criteria

| Version Level | Condition | Change Examples | Impact Scope |
|---------------|-----------|-----------------|-------------|
| **MAJOR** | Breaking Changes<br/>Backward incompatibility | • Negotiation protocol structure changes<br/>• Fundamental file structure redesign<br/>• API specification changes<br/>• Changes that break existing usage | 🔴 **High Impact**<br/>User adaptation required |
| **MINOR** | Backward Compatible<br/>New feature addition | • New platform support (Windows, Linux, etc.)<br/>• Additional tool/pattern support<br/>• New collaboration methodology<br/>• Template feature expansion | 🟡 **Medium Impact**<br/>Existing usage maintained |
| **PATCH** | Bug Fixes<br/>Backward compatible fixes | • Documentation typo fixes<br/>• Command error corrections<br/>• Broken link fixes<br/>• Template content improvements | 🟢 **Low Impact**<br/>Transparent improvements |

### 📊 Change Classification by Version

#### Added (MINOR +)
- New platform support commands
- Additional template sections
- New patterns and cases
- Extended features

#### Changed (MAJOR Alert)
- Existing structure modifications
- Negotiation protocol changes  
- File naming convention changes
- Core workflow modifications

#### Fixed (PATCH)
- Bug fixes
- Typos and link fixes
- Documentation accuracy improvements
- Command error corrections

#### Removed (MAJOR)
- Existing feature removal
- File structure simplification
- Backward compatibility breaks

### 🎯 Semantic Versioning Examples

```
0.1.0 → 0.1.1  (Documentation typo fix)
0.1.1 → 0.2.0  (Windows support added)  ← This update
0.2.0 → 0.2.1  (Command bug fix)
0.2.1 → 1.0.0  (First stable version)
1.0.0 → 2.0.0  (Negotiation protocol structure change)
```

### 📝 CHANGELOG.md Integration

All version changes are recorded in [CHANGELOG.md](CHANGELOG.md) in the following format:

```markdown
## [Unreleased]
### Added
- New features

## [0.2.0] - 2025-01-XX
### Added  
- Windows platform support (CMD, PowerShell)
- OS-specific quick start guide

## [0.1.0] - 2025-07-28
### Added
- Reality-Based Redesign completion
- Negotiation protocol system
```

## 📄 License

This project is distributed under the [Creative Commons Attribution 4.0 International License](http://creativecommons.org/licenses/by/4.0/).

**Simply put**: Feel free to use it. Just credit the source! 🎉

## 🙏 Acknowledgments

- **Claude Code Team**: For providing excellent tools
- **Open Source Community**: For continuous inspiration
- **All Contributors**: For contributing to project development

## 📞 Contact

- 🐛 **Bug Reports**: [Issues](https://github.com/yscha88/neuroclaude/issues)
- 💡 **Feature Requests**: [Feature Requests](https://github.com/yscha88/neuroclaude/issues/new?template=feature_request.md)
- 💬 **General Discussion**: [Discussions](https://github.com/yscha88/neuroclaude/discussions)

---

**For effective Claude collaboration!** 🚀

_Made with ❤️ for structured collaboration_