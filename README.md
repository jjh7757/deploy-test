# deploy-test

AWS 배포 파이프라인(GitHub OIDC → ECR → SSM → EC2) 검증용 최소 앱.

`git push` 하면 Actions가 arm64로 빌드해 ECR에 올리고, SSM으로 EC2에서 교체한다.

접속하면 배포된 커밋 SHA가 보인다. **이 값이 방금 push한 커밋과 일치해야 배포가 실제로 된 것이다.**

```
deploy-test OK
host=...
sha=<커밋 SHA>
time=...
```

구축 기록: [jjh7757/TIL — AWS배포환경](https://github.com/jjh7757/TIL)
