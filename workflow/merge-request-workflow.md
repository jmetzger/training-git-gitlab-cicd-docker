# Merge-Request workflow 

## Definieren für job 

```
job1:
  script:
    - echo "This job runs in merge request pipelines"
  rules:
    - if: $CI_PIPELINE_SOURCE == 'merge_request_event'
```

## Definieren in workflow 

```
workflow:
  rules:
    - if: $CI_PIPELINE_SOURCE == 'merge_request_event'

job1:
  script:
    - echo "This job runs in merge request pipelines"

job2:
  script:
    - echo "This job also runs in merge request pipelines"

```

  * https://docs.gitlab.com/ee/ci/pipelines/merge_request_pipelines.html
