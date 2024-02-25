# 네임스페이스에 annotations 추가하기
```yaml
apiVersion: v1
kind: Namespace
metadata:
  name: < 네임스페이스 이름 >
  annotations:
    keptn.sh/lifecycle-toolkit: "enabled"
```

# 워크로드 및 앱 생성에 필요한 라벨 
[워크로드 및 앱 이해하기](https://keptn.sh/stable/docs/components/lifecycle-operator/keptn-apps/)
아래의 라벨을 추가하면 자동으로 keptnworkload와 keptnapp이 생성됨

## keptn.sh
```yaml
keptn.sh/workload: myAwesomeWorkload
keptn.sh/version: myAwesomeWorkloadVersion
keptn.sh/app: myAwesomeAppName
keptn.sh/container: myAwesomeContainer
```

## kubernetes
```yaml
app.kubernetes.io/name: myAwesomeWorkload
app.kubernetes.io/version: myAwesomeWorkloadVersion
app.kubernetes.io/part-of: myAwesomeAppName
```


# 쿠버네티스에서 실행되지 않는 배포와도 상호작용 가능
## KeptnTaskDefinition/KeptnTask

## keptn analysis
1. KeptnMetricProvider 생성
2. AnalysisValueTemplate 생성
3. AnalysisDefinition 생성
4. Analysis 생성
