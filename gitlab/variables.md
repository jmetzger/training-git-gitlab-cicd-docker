#  Variablen definieren 

## Settings Variable definieren (Settings -> CI/CD -> Variables) 

```
TEST_URL
```

## Variable verwenden 

```
stages:
  - build 
  - test
  
show_env:
  stage: build 
  script:
  - echo $TEST_URL
  - echo $TEST_URL > /tmp/urltest.txt
  - echo $TEST_PASS
  - echo $TEST_PASS > /tmp/testpass
  - cat /tmp/testpass

test_env:
  stage: test 

  script:
  - echo $TEST_URL
```

## Beispiele: (Global) 

```
# gitlab-ci.yml
variables:
  TEST_URL: http://schulung.t3isp.de # globalen Scope - in der gesamten Pipeline
                                     # Überschreibt NICHT -> ... Settings -> CI/CD -> Variables   
  TEST_VERSION: "1.0" # global 
  TEST_VAR: "overwrite?" 

stages:
  - build 
  - test
  
show_env:
  stage: build 

  variables:
    TEST_JOB: lowrunner # variable mit lokalem Scope - nur in Job 
    TEST_VAR: "neu ueberschrieben"

  script:
  - echo $TEST_URL 
  - echo $TEST_VERSION
  - echo $TEST_JOB # nur lokal 
  - echo $TEST_VAR

test_env:
  stage: test 

  script:
  - echo "TESTJOB" 
  - echo $TEST_JOB

```

## Reihenfolge, welche Variablen welche überschreien (Ebenene) 

  * https://docs.gitlab.com/ee/ci/variables/#cicd-variable-precedence
