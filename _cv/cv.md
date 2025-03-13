---
title: SunnyShin CV
---
# SunnyShin

## Contents
- [UpdateDate](#about)
- [Features](#features)
- [Examples](#examples)
- [Installation](#installation)
- [Customising](#customising)
- [Configuration](#configuration)
  - [Gem dependency settings](#gem-dependency-settings)
  - [Site settings](#site-settings)
  - [Site performance settings](#site-performance-settings)
  - [Site navigation](#site-navigation)
  - [Custom fonts](#custom-fonts)
- [Using includes](#using-includes)
- [Page layouts](#page-layouts)
- [Page and Post options](#page-and-post-options)
- [Credits](#credits)

## UpdateDate

- 2025-03-11

## 기본 정보

- 이름: 신선우
- 최종 학력: UNIST 컴퓨터공학 (전공) / 기계공학 (부전공)

## 참여 프로젝트

- King Arthur: Legends Rise
    - 플랫폼 : Android, iOS, Steam, Windows(넷마블 런쳐)
    - 언리얼5 실사풍 턴 기반 수집형 RPG
    - Timeline
        - 2023년 6월 30일 소프트 런칭
        - 2024년 10월 30일 얼리 액세스 런칭
        - 2024년 11월 27일 글로벌 오픈

## 경력

- 구로발게임즈 언리얼 엔진 5 클라이언트 개발자
    - 넷마블 2021년 공개 채용 입사 (2021_01_04)
    - 클라이언트 팀원 (2021_01~2023_01)
    - 엔진/플랫폼 팀원 (2023_01~2024_01)
    - 클라이언트 팀원 (2024_01~현재)

## 자기소개

- 구로발게임즈에서 4년 2개월 동안 언리얼 엔진 5 클라이언트 개발자로 근무하면서, SDK 적용부터 에셋 다운로드 및 패치 시스템, 인게임 네트워크 유지보수, 그리고 CI/CD 시스템 개선 등 다양한 핵심 개발에 주도적으로 참여하였습니다.
- 특히, 캐나다와 한국 서로 다른 국가의 퍼블리셔 변경에 따른 두 차례의 SDK 적용 작업과 협업 개발 경험은 차별화된 강점으로, 새로운 환경에서도 빠르게 적응하고 안정적인 서비스 환경 구축을 위하여 노력하였습니다.
- 새로운 기술 및 트랜드에 관심이 많습니다. 최근에는 개인적으로 AI에 관심을 가지고 트랜드 트래킹 및 로컬 LLM 사용을 진행하였습니다. 이 추세는 앞으로의 개발 환경에도 많은 영향을 끼칠 것으로 생각되어 관심을 가지고 공부를 진행하고 있습니다.
- 여러 장르의 게임들을 많이 플레이하는 코어 게이머로써 각종 컨텐츠들을 개발할 때 많은 의견들을 제시하고 게이머의 시선으로 누락된 부분들을 캐치하려고 노력합니다.
- 플레이 해온 게임들은 AOS, FPS, 수집형RPG, 로그라이크, 턴제, 액션, 오픈월드, 리듬게임, 4x 등 다양한 장르의 게임들을 즐기고 있습니다. 서브컬처쪽을 좋아하는 편 이지만 편식하지 않습니다.

## 기술 스택

- 언리얼 엔진 5
- 언어 : C++, Python
- VCS : SVN, Perforce
- VisualStudio, Rider, VSCode

## 구로발게임즈 주요 경력

- 멀티플랫폼 환경 개발:
    - Android, iOS, Steam, Windows의 멀티플랫폼 출시를 위한 각종 개발 및 트러블 슈팅
- 인증, 구매, 로깅 SDK 개발 및 통합: (기여도 50%)
    - Kabam SDK: 퍼블리셔의 Unreal SDK 초기 개발 단계부터 공동으로 SDK를 논의/적용하며 프로젝트와 퍼블리셔의 니즈에 맞춰 개발/개선 과정을 진행함
    - 넷마블 SDK: 퍼블리셔의 신규 인증규약을 적용/테스트하고 구현
    - 유료구매 상품 정보를 인게임에서 업데이트하여 점검없이 상품 변경/추가 가능한 구조 구현
    - 마케팅 지표분석을 위한 Facebook Android, iOS unreal SDK플러그인 개발 및 유지보수
- 게임 에셋 분할 다운로드 및 패치 시스템: (기여도 60%)
    - 인게임 백그라운드 다운로드/업데이트 시스템 개발
    - 에셋 분할 패키징 개발
    - 라이브서비스 CDN버저닝 계획 수립 및 Jenkins 적용
    - 인게임 진행도에 따라 에셋을 분할하여 다운로드/업데이트 가능하도록 구현
- 클라이언트 네트워크 모듈 개선 유지보수: (기여도 30%)
    - 실시간 Socket통신, 비동기 시스템으로 작동하는 클라이언트의 네트워크 패킷 처리 로직을 개선 및 유지보수.
    - 네트워크 순단 및 리커버리 로직 개발 및 코어 로직에 적용
    - Packet Loss환경을 재현하는 툴 개발로 테스트 편의성 제공
- 각종 인게임 컨텐츠 및 시스템 개발 및 유지보수
    - Python을 활용하여 개인 로컬환경에서의 쉽게 빌드를 낼 수 있도록 개발, 빌드가이드 문서 작성 (기여도 80%)
    - 레벨 로딩 시스템 개발 (기여도 50%)
    - 각종 인게임 컨텐츠 및 시스템 개발