# JARVIS 핵심 파일 목록 (Hotspots)
> 수정 요청 시 참고할 핵심 파일들

##  프론트엔드
| 파일 | 역할 |
|------|------|
| `src/App.tsx` | 메인 UI 컴포넌트 (1030줄) - 채팅, 음성, 카메라, 파일업로드 전체 |
| `src/index.css` | 전역 스타일 |
| `src/lib/utils.ts` | 유틸리티 함수 (cn 등) |
| `src/main.tsx` | React 앱 진입점 |

##  백엔드
| 파일 | 역할 |
|------|------|
| `server.js` | Express 서버 + Python 에이전트 IPC 관리 |
| `agent.py` | Python 로컬 에이전트 (PC 제어, 시스템 정보) |

##  설정
| 파일 | 역할 |
|------|------|
| `vite.config.ts` | Vite 빌드 설정 + 금고 env 로드 |
| `package.json` | 의존성 (React 19, Gemini SDK, Motion, Recharts 등) |
| `.env` | 금고 경로만 참조 (API키 없음) |

##  AI 설정 위치
- `src/App.tsx` Line 49: SYSTEM_INSTRUCTION (자비스 페르소나)
- `src/App.tsx` Line 40: Gemini 초기화
- `src/App.tsx` Line 452: AI 호출 + 함수 도구(Function Calling) 처리

##  보안
- 실제 API 키: `D:/My_project/Vault/.env` (중앙 금고, GitHub 비공개)
- 코드 레포(jarvis): Private
- 이 컨텍스트 레포(jarvis-context): Public (민감정보 없음)
