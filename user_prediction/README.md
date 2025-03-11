기존에 만들었던 기계 학습 기반 유저 매칭 확률 모델 예측 모델을 리팩토링 하고 있습니다.

[변경 전]

(1) conda 가상 환경으로 개발 /n
(2) formatter 없이 그냥 작성되어 있던 코드들

- 데이터 분석을 위해 흩어져 있던 jupyter file
- 보안 및 주요한 설정이 있는 env 로드가 main에 있음
- 마구잡이로 짜여있던 코드들
- 그냥 서빙하던 ML 모델



[변경 후]

(1) poetry 프로젝트 의존성을 관리해서 프로젝트의 팀원들이 동일한 Poetry 환경을 사용할 수 있게끔 수정
(2) .pre-commit-config.yaml 파일을 통해서 pre-commit 시에 black, isort formatter로 포맷팅하도록 수정
