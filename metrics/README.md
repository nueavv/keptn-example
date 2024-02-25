# Metric 확인
```sh
kubectl get keptnmetrics.metrics.keptn.sh -n <namespace> <metric-name>
```

## 예제  확인
```sh
kubectl get keptnmetrics.metrics.keptn.sh -n sample-app available-cpus
```

# 값 확인하기
```sh
kubectl get --raw "/apis/custom.metrics.k8s.io/v1beta2/namespaces/<namespace>/keptnmetrics.metrics.sh/<metric-name>/<metric-name>"
```

## 예제로 확인하기
```sh
kubectl get --raw "/apis/custom.metrics.k8s.io/v1beta2/namespaces/sample-app/keptnmetrics.metrics.sh/available-cpus/available-cpus"

```

# 여기 값을 HPA로 적용할 수 있음.