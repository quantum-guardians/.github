# Metropolitan Ring Road System

[website](https://qi4uinpnu.vercel.app/)

## 1. 프로젝트 소개

이 프로젝트는 Quantum Annealing을 기반으로 군중 밀집 공간의 흐름을 최적화하여 압사 사고를 예방하는 솔루션입니다.

### Strategy
- 다중 밀집 사고가 군중의 이동 흐름이 충돌으로 인해 일어나는 점을 고려하여, 각 군중의 이동 흐름을 최적화 하는 전략
  - 각 길의 방향을 상태로 설정, 각 교차로에서 교차로까지의 거리의 합을 최소화하는 방식으로 최적화
- Small World Approach

![small-word.png](https://s3.yunseong.dev/website/28a2b69d-3834-47cb-8b2b-91c8b748e15e.png)

- Naoto Approach

![naoto.png](https://s3.yunseong.dev/website/c6f709ff-bc7b-4e1c-ae13-46c9452be429.png)

## 2. 기술 스택

-   **Backend**: `Python`, `FastAPI`, `NetworkX`
-   **Frontend**: `React`, `TypeScript`, `Vite`, `vis.js` (for graph visualization)
-   **Infra**: `Vercel`

## 3. 프로젝트 실행 방법

### Backend

1.  `backend`를 클록하고 이동합니다.
    ```bash
    git clone https://github.com/quantum-guardians/mr2s-backend.git
    cd mr2s-backend
    ```
2.  필요한 Python 패키지를 설치합니다.
    ```bash
    pip install -r requirements.txt
    ```
3.  FastAPI 개발 서버를 실행합니다.
    ```bash
    uvicorn main:app --host 0.0.0.0 --port 8000 --reload
    ```
    서버는 `http://localhost:8000`에서 실행됩니다.

### Frontend

1.  `frontend`를 클론하고 이동합니다.
    ```bash
    git clone https://github.com/quantum-guardians/mr2s-frontend.git
    cd mr2s-frontend
    ```
2.  필요한 Node.js 패키지를 설치합니다.
    ```bash
    npm install
    ```
3.  Vite 개발 서버를 실행합니다.
    ```bash
    npm run dev
    ```
    애플리케이션은 `http://localhost:5173` 또는 다른 지정된 포트에서 실행됩니다.
