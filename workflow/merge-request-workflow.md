# Merge-Request workflow 

## Voraussetzung

  * Definiert durch wert: merge_request_event

## Wichtig: 

  * Das passiert vor dem Mergen und testet nur den Quellbranch (Source)  

## Läuft wann ? 

   * When ich einen Merge-Request von einem Quellbranch erstelle (source),
     * der mehr als 1 commit hat. 
   * Ich einen source branch für einen merge request pushe.
   * Starten über die Pipieline tab in einem Merge-Request und ich dort starte
     
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
