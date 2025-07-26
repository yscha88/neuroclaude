# 문서 포맷 효율성 패턴
---

## 🎯 핵심 발견: JSON 포맷의 압도적 효율성

### **포맷별 변환 효율성 비교**

| 변환 방식 | 데이터 손실률 | 처리 시간 | 후처리 복잡도 | 도구 호환성 |
|----------|-------------|---------|-------------|-----------|
| **Excel → JSON** | **0%** | **100%** | **최소** | **최고** |
| Excel → CSV | 15-20% | 150% | 중간 | 중간 |
| Excel → MD | 25-30% | 200% | 높음 | 낮음 |

---

## 🔧 JSON 변환의 핵심 이점

### 1. **완전한 구조 보존**
```json
{
  "metadata": {
    "source_file": "규제_문서.xlsx",
    "extraction_time": "2025-07-23T10:30:00Z",
    "sheet_name": "Test_Cases",
    "total_rows": 159
  },
  "header_mapping": {
    "row_2": ["Test_Case_ID", "Category", "Requirements_ID", ...]
  },
  "test_cases": [
    {
      "Test_Case_ID": "{ID_패턴}",
      "Category": "FR|NFR",
      "Requirements_ID": "{요구사항_패턴}",
      "Test_Title_KR": "{테스트_설명}",
      "Test_Steps_KR": "{실행_절차}",
      "Expected_Result_KR": "{예상_결과}",
      "Precondition_KR": "{초기_상태}"
    }
  ]
}
```

### 2. **자동 데이터 정제**
- **빈 컬럼 자동 제거**: 빈 "Column_*" 키 자동 식별 및 제거
- **헤더 행 자동 탐지**: 복잡한 Excel 구조 자동 파싱
- **데이터 타입 보존**: 숫자, 날짜, 텍스트 형식 원본 그대로 유지

### 3. **API 도구 직접 연동**
```python
# JSON → 모든 API 도구 (TestRail, Jira, Azure DevOps)
def json_to_api_tool(json_data, tool_mapping):
    for record in json_data['records']:
        api_data = {}
        for json_field, api_field in tool_mapping.items():
            api_data[api_field] = record.get(json_field, '')
        api_tool.create_item(api_data)
```

---

## JSON 표준 구조

### **테스트케이스 문서**
```json
{
  "regulatory_metadata": {
    "standard_compliance": ["IEC 62304", "21 CFR 820.30", "ISO 14971"],
    "document_type": "Software_Verification_Test_Cases",
    "life_cycle_phase": "Verification_and_Validation"
  },
  "traceability": {
    "requirements_link": "requirements_id_field",
    "design_link": "design_reference_field", 
    "risk_link": "risk_control_id_field"
  },
  "test_structure": {
    "id_field": "Test_Case_ID",
    "category_field": "Category", // FR/NFR
    "priority_field": "Priority", // High/Medium/Low
    "title_fields": {
      "korean": "Test_Title_KR",
      "english": "Test_Title_EN"
    },
    "execution_fields": {
      "steps": "Test_Steps_KR",
      "precondition": "Precondition_KR", 
      "expected_result": "Expected_Result_KR",
      "actual_result": "Test_Result"
    }
  }
}
```

### **요구사항 문서**
```json
{
  "regulatory_metadata": {
    "standard_compliance": ["IEC 62304", "ISO 14971"],
    "document_type": "Software_Requirements_Specification",
    "life_cycle_phase": "Requirements_Analysis"
  },
  "requirement_structure": {
    "id_field": "Requirements_ID", // S[F|N]R-XX-001
    "category_field": "Category", // Functional/Non-Functional
    "description_field": "Requirement_Description",
    "rationale_field": "Rationale",
    "verification_method": "Verification_Method" // Test/Inspection/Analysis
  },
  "traceability_links": {
    "parent_requirements": "Parent_Req_ID",
    "test_cases": "Linked_Test_Cases",
    "design_elements": "Design_Reference",
    "risk_controls": "Risk_Control_ID"
  }
}
```

### **위험 관리 문서**
```json
{
  "regulatory_metadata": {
    "standard_compliance": ["ISO 14971"],
    "document_type": "Risk_Management_File",
    "life_cycle_phase": "Risk_Analysis"
  },
  "risk_structure": {
    "id_field": "Risk_ID",
    "hazard_field": "Hazard_Description",
    "harm_field": "Potential_Harm",
    "severity_field": "Severity", // Catastrophic/Critical/Marginal/Negligible
    "probability_field": "Probability", // Frequent/Probable/Occasional/Remote/Improbable
    "risk_level_field": "Risk_Level", // High/Medium/Low
    "control_measures": "Risk_Control_Measures",
    "residual_risk": "Residual_Risk_Level"
  }
}
```

---

## ⚠️ 구현 시 고려사항

### **데이터 품질 관리**
1. **인코딩**: UTF-8-BOM 처리 필요
2. **특수문자**: 줄바꿈(\n), 탭(\t) 문자 보존
3. **빈 값 처리**: null vs 빈 문자열 구분
4. **숫자 형식**: Excel 수식 결과값 vs 원본 수식

### **대용량 파일 처리**
1. **메모리 최적화**: 스트리밍 방식 JSON 생성
2. **배치 처리**: API 호출 횟수 제한 고려
3. **에러 처리**: 부분 실패 시 재시도 메커니즘

### **규제 준수**
1. **감사 추적**: 변환 과정 로그 보관
2. **데이터 무결성**: 원본과 변환 결과 검증
3. **접근 제어**: 민감 정보 처리 시 권한 관리