# 개요
prometheus metric를 어떻게 노출시키는지 연습

# 실행방법
```shell
pip install requirements.txt
uvicorn main:app --reload
```

# 메트릭 접속 방법
* http://127.0.0.1:8090/metrics로 접속

# 도커 빌드 방법
```shell
DOCKER_REGISTRY="choisunguk"

nerdctl -n k8s.io build \
-f ./deploy/Dockerfile \
-t ${DOCKER_REGISTRY}/prometheus-python-deo:0.1 \
--platform=amd64 \
./
```
