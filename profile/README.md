# Quantum Guardians

Quantum Guardians는 양자 어닐링(Quantum Annealing)을 활용하여 군중 압착 사고(Crowd Crush)를 예방하기 위한 보행자 동선 최적화 솔루션을 연구·개발하는 팀입니다.

# Metropolitan Ring Road System

[simulation page](https://mr2s.vercel.app/)

이 프로젝트는 Quantum Annealing을 기반으로 군중 밀집 공간의 흐름을 최적화하여 압사 사고를 예방하는 솔루션입니다.

보행자 네트워크를 그래프로 모델링하고, QUBO(Quadratic Unconstrained Binary Optimization) 기반 최적화를 통해 보행 흐름 충돌을 줄이고 이동 효율성을 높이는 방향성을 탐색합니다.  
프로젝트는 APSP(All-Pairs Shortest Paths) 최소화, 유량 보존(Flow Conservation), 연결성 유지(Connectivity Preservation) 등을 핵심 목표로 하며, 실제 도시 환경과 군중 시뮬레이션에 적용 가능한 시스템 구축을 목표로 합니다.

## Repositories

### [mr2s-module](/quantum-guardians/mr2s-module)
MR2S 솔루션의 핵심 최적화 알고리즘을 다루는 저장소입니다.  
그래프 전처리, QUBO 모델링, APSP 최적화, 유량 보존 전략, 양자 어닐링 기반 솔버 등을 구현합니다.

### [mr2s-frontend](/quantum-guardians/mr2s-frontend)
MR2S 최적화 결과를 시각화하고 조작하기 위한 프론트엔드 저장소입니다.  
그래프 입력, 최적화 실행, 결과 시각화, 벤치마크 확인 등의 기능을 제공합니다.

### [mr2s-backend](/quantum-guardians/mr2s-backend)
`mr2s-module`을 기반으로 최적화 요청을 처리하는 백엔드 서버 저장소입니다.  
프론트엔드와 알고리즘 모듈을 연결하고, 그래프 처리 API와 실험 실행 흐름을 관리합니다.

### [approach-analysis](/quantum-guardians/approach-analysis)
MR2S의 다양한 최적화 접근 방식을 분석하고 비교하기 위한 연구용 저장소입니다.  
APSP 상관관계 분석, 벤치마크, 하이퍼파라미터 실험, QUBO 전략 비교 등을 다룹니다.

### [documents](/quantum-guardians/documents)
Quantum Guardians 프로젝트의 문서 자료를 관리하는 저장소입니다.  
논문 초안, 발표 자료, 포스터, 연구 설명 문서, 실험 기록 등을 보관합니다.

### [mr2s_simulation](/quantum-guardians/mr2s_simulation)
Unity 기반 3D 군중 시뮬레이션 저장소입니다.  
최적화된 동선이 실제 보행 흐름, 혼잡도, 충돌 감소, 도착 시간 등에 어떤 영향을 주는지 검증합니다.
