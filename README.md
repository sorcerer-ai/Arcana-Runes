# Arcana Runes — Skill Marketplace Registry

Arcana 데스크톱 앱의 스킬 마켓플레이스 레지스트리입니다.

## 구조

```
registry.json              # 전체 스킬 목록 (메타데이터)
skills/
  {skill-id}/
    manifest.json          # 완전한 스킬 정의 (prompt 포함)
```

## 스킬 목록

| ID | 이름 | 설명 | 카테고리 |
|---|------|------|----------|
| `code-review-kr` | 코드 리뷰 | 코드 품질, 보안, 모범 사례 검토 | 개발 |
| `bug-fix-helper` | 버그 수정 도우미 | 에러 분석 → 수정 방안 제시 | 개발 |
| `api-docs-gen` | API 문서 생성기 | 코드에서 API 문서 자동 생성 | 문서 |
| `test-writer-kr` | 테스트 작성기 | 단위 테스트 코드 생성 | 개발 |
| `refactor-guide` | 리팩토링 가이드 | 코드 개선점 분석 + 제안 | 개발 |
| `commit-msg-kr` | 커밋 메시지 작성 | Conventional Commits 생성 | 도구 |
| `data-insight` | 데이터 분석 | CSV/JSON 분석 + 인사이트 | 분석 |
| `doc-summary-kr` | 문서 요약기 | 문서 핵심 요점 압축 | 문서 |

## 스킬 추가 방법

1. `skills/{skill-id}/manifest.json` 파일 생성
2. `registry.json`에 메타데이터 추가
3. Pull Request 제출

## manifest.json 형식

```json
{
  "id": "my-skill",
  "name": "스킬 이름",
  "description": "스킬 설명",
  "prompt": "프롬프트 템플릿. {{input}} 플레이스홀더 사용.",
  "icon": "LucideIconName",
  "is_custom": false,
  "tags": ["tag1", "tag2"],
  "version": "1.0.0"
}
```

## 라이선스

MIT
