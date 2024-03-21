# Training: Von git über gitlab (ci/cd) zum Docker-Image

## Agenda 

  1. Was haben wir vor ?
     * [Überblick über unsere 3-Tages-Reise](/training/3-tages-reise.md)
    
  1. GIT - Geschichte / Grundlagen
     * [GIT Pdf](http://schulung.t3isp.de/documents/pdfs/git/git-training.pdf)

  1. git - kommandos (Tipps & Tricks) 
     * [git alias ](alias.md) 
     * [git add + Tipps & Tricks](add.md)
     * [git commit](commit.md)
     * [git log](log.md)
     * [git config](config.md) 
     * [git show](show.md)
     * [Needed commands for starters](started-commands.md)
     * [git branch](branch.md)
     * [git checkout](checkout.md)
     * [git merge](merge.md)
     * [git tag](tag.md)
     * [git rm (Dateien löschen aus git)](rm.md)
    
  1. git - Tipps & Tricks
     * [Schöne logausgabe](beautify-log.md)
    
  1. git - exercises (merging)
     * [merge-conflict](merge-conflict.md)

  1. git - mergetool
     * [git mergetool](mergetools.md)
    
  1. gitlab ci/cd (Überblick)
     * [Architecture](/gitlab/architecture.md)
    
  1. gitlab
     * [Exercise merge-request single-teams](merge-request.md)
     * [Exercise merge-request with conflict in group](group-merge-request-conflict.md)

  1. Docker-Grundlagen 
     * [Übersicht Architektur](architektur.md)
     * [Was ist ein Container ?](container.md)
     * [Was sind container images](container-images.md) 
     * [Container vs. Virtuelle Maschine](container-vs-vm.md)
     * [Was ist ein Dockerfile](dockerfile.md)
    
  1. Docker Installation
     * [Installation Docker unter Ubuntu mit Docker Repo](install-docker-ubuntu-apt.md)

  1. Docker-Befehle 
     * [Die wichtigsten Befehle](docker-befehle.md)
     * [Logs anschauen - docker logs - mit Beispiel nginx](docker-logs-nginx.md)
     * [docker run](docker-run.md)
     * [Docker container/image stoppen/löschen](container-image-delete.md)
     * [Docker containerliste anzeigen](container-liste.md)
     * [Docker nicht verwendete Images/Container löschen](delete-everything.md)
     * [Docker container analysieren](docker-inspect.md)
     * [Docker container in den Vordergrund bringen - attach](/docker/docker-attach.md) 
     * [Aufräumen - container und images löschen](prune-container-images.md)
     * [Nginx mit portfreigabe laufen lassen](docker-example-nginx.md)    
  
  1. Dockerfile - Examples 
     * [Ubuntu mit hello world](ubuntu-hello-world.md)
     * [Ubuntu mit ping](ubuntu-ping.md) 
     * [Nginx mit content aus html-ordner](nginx-html-content.md)
  
  1. Docker-Netzwerk 
     * [Netzwerk](network.md)
  
  1. Docker-Container Examples 
     * [2 Container mit Netzwerk anpingen](2-containers-with-network-ping.md)
     * [Container mit eigenem privatem Netz erstellen](container-with-own-bridge.md)  
  
  1. Docker-Daten persistent machen / Shared Volumes 
     * [Überblick](storage-overview.md) 
     * [Volumes](storage-volumes.md) 
     * [bind-mounts](docker-bind-mount.md)
     * [bind-mounts-permissions](docker-bind-mount-permissions.md)
     
  1. Docker Compose
     * [yaml-format](yaml-format.md)
     * [Ist docker-compose installiert?](docker-compose-installed.md) 
     * [Example with Wordpress / MySQL](example-wordpress-mysql.md)
     * [Example with Wordpress / Nginx / MariadB](example-wnm-docker-compose.md)
     * [Example with Ubuntu and Dockerfile](example-docker-compose-ubuntu-build.md)
     * [Logs in docker - compose](docker-compose-logs.md)
     * [docker-compose und replicas](docker-compose-replicas.md)
     * [docker compose Reference](https://docs.docker.com/compose/compose-file/compose-file-v3/)

  1. gitlab ci/cd (Praxis I) 
     * [Using the test - template](/gitlab/02-example-testtemplate.md)
     * [Examples running stages](/gitlab/03-example-running-stages.md) 
     * [Predefined Vars](/gitlab/04-predefined-vars.md)
     * [Variablen definieren](/gitlab/variables.md)
     * [Variablen überschreiben/leeren](gitlab/cases/variablen-ueberschreiben-leeren.md)
     * [Rules](/gitlab/05-rules.md)
     * [Example Defining and using artifacts](/gitlab/07-example-defining-and-using-artifacts.md)

  1. gitlab ci/cd docker
     * [Docker image automatisiert bauen - gitlab registry](/gitlab/09-use-gitlab-registry.md)

  1. gitlab ci/cd (Praxis II)
     * [Mehrzeile Kommandos in gitlab ci-cd ausführen](/gitlab/jobs/script/multiline.md)
     * [Kommandos auf Zielsystem mit ssh ausführen (auch multiline)](gitlab/jobs/script/ssh-multiline.md)

  1. gitlab-ci/cd - Workflows
     * [Workflows + only start by starting pipeline](/gitlab/global/workflow.md)
     * [Templates for branch and merge request workflow](workflow/templates-branch-merge-request-pipeline.md)
    
  1. gitlab ci/cd docker compose
     * [Docker compose local testen](gitlab/docker-compose/01-docker-compose-local-testen.md)
     * [Docker compose über ssh](gitlab/docker-compose/02-docker-compose-ssh.md)
     * [Docker compose classic über scp](gitlab/docker-compose/03-docker-compose-rollout-classic.md)

  1. gitlab - ci/cd - Pipelines strukturieren / Templates 
     * [Includes mit untertemplates](gitlab/include/pipeline-with-includes.md)
     * [Parent/Child Pipeline](/gitlab/parent-child-pipeline.md)
     * [Multiproject Pipeline / Downstream](/gitlab/multiproject-pipeline.md)
     * [Vorgefertigte Templates verwenden](gitlab/include/templates.md)
     * [Arbeiten mit extend und anchor - Dinge wiederverwenden](gitlab/cases/extend-and-anchor.md)
      
  1. Documentation (git)
     * [Suche in git](https://docs.gitlab.com/ee/user/search/)
    
  1. Documentation (gitlab)
     * [gitlab ci/cd predefined variables](https://docs.gitlab.com/ee/ci/variables/predefined_variables.html)
     * [.gitlab-ci.yml Reference](https://docs.gitlab.com/ee/ci/yaml/)
     * [Referenz: global -> workflow](https://docs.gitlab.com/ee/ci/yaml/#workflow)
     * [Referenz: global -> default](https://docs.gitlab.com/ee/ci/yaml/#default)
    
  1. Security
     * [Container Scanning](gitlab/cases/container-scanning.md)

  1. Documentation - Includes
     * [includes](https://docs.gitlab.com/ee/ci/yaml/includes.html)
     * [includes -> rules](https://docs.gitlab.com/ee/ci/yaml/includes.html#use-rules-with-include)
     * [includes -> rules -> variables](https://docs.gitlab.com/ee/ci/yaml/#rulesvariables)
     * [includes -> templates -> override-configuration](https://docs.gitlab.com/ee/ci/yaml/includes.html#override-included-configuration-values)
     * [includes -> defaults](https://docs.gitlab.com/ee/ci/yaml/includes.html#use-default-configuration-from-an-included-configuration-file)
    
  1. Documentation - Instances Limits
     * [applicaton limits](https://docs.gitlab.com/ee/administration/instance_limits.html)

## Backlog 

  1. Docker Security 
     * [Docker Security](docker/security/overview.md)
     * [Scanning docker image with docker scan/snyx](docker/security/docker-scan-snyk.md) 

  1. Docker - Dokumentation 
     * [Vulnerability Scanner with docker](https://docs.docker.com/engine/scan/#prerequisites)
     * [Vulnerability Scanner mit snyk](https://snyk.io/plans/)
     * [Parent/Base - Image bauen für Docker](https://docs.docker.com/develop/develop-images/baseimages/)

  1. gitlab ci/cd (Überblick)
     * [Architecture](/gitlab/architecture.md)
     * [Overview/Pipelines](/gitlab/01-ci-cd-overview.md)
     * [SaaS vs. On-Premise (Self Hosted)](gitlab/overview/saas-vs-on-premise.md)

  1. Hintergründe
     * [Warum before_script ?](/gitlab/why-before-script.md)
     * [GIT_STRATEGY usw.](gitlab/git_strategy.md)

  1. gitlab-ci/cd - Workflows
     * [Workflows + only start by starting pipeline](/gitlab/global/workflow.md)
     * [Templates for branch and merge request workflow](workflow/templates-branch-merge-request-pipeline.md)
    
  1. gitlab-ci/cd - Variables
     * [Variablen in Pipelines Web-Dialog anzeigen](variables/variables-in-pipeline-formular-anzeigen.md)

  1. gitlab - ci/cd - Pipelines strukturieren / Templates 
     * [Includes mit untertemplates](gitlab/include/pipeline-with-includes.md)
     * [Parent/Child Pipeline](/gitlab/parent-child-pipeline.md)
     * [Multiproject Pipeline / Downstream](/gitlab/multiproject-pipeline.md)
     * [Vorgefertigte Templates verwenden](gitlab/include/templates.md)
     * [Arbeiten mit extend und anchor - Dinge wiederverwenden](gitlab/cases/extend-and-anchor.md)
    
  1. gitlab - wann laufen jobs ? 
     * [Job nur händisch über Pipelines starten](gitlab/rules/only-web.md)
     * [Auch weiterlaufen, wenn Job fehlschlägt](gitlab/jobs/allow_failure.md)
    
  1. gitlab ci/cd docker compose
     * [Docker compose local testen](gitlab/docker-compose/01-docker-compose-local-testen.md)
     * [Docker compose über ssh](gitlab/docker-compose/02-docker-compose-ssh.md)
     * [Docker compose classic über scp](gitlab/docker-compose/03-docker-compose-rollout-classic.md)

  1. Performance / Caching 
     * [Wann ist eine Pipeline langsam ?](performance/when-is-pipeline-slow.md)
     * [Caching->cache in gitlab](gitlab/caching/cache.md)
    
  1. Matrix = Loops
     * [Matrix=Loops, Jobs mehrmals ausführen](gitlab/matrix.md)
    
  1. Monitoring gitlab
     * [Monitoring gitlab good or bad ?](monitoring/overview.md)
    
  1. Security
     * [Container Scanning](gitlab/cases/container-scanning.md)
    
  1. Environments
     * [Environments](gitlab/environments.md)

  1. Documentation 
     * [gitlab ci/cd predefined variables](https://docs.gitlab.com/ee/ci/variables/predefined_variables.html)
     * [.gitlab-ci.yml Reference](https://docs.gitlab.com/ee/ci/yaml/)
     * [Referenz: global -> workflow](https://docs.gitlab.com/ee/ci/yaml/#workflow)
     * [Referenz: global -> default](https://docs.gitlab.com/ee/ci/yaml/#default)

  1. Documentation - Includes
     * [includes](https://docs.gitlab.com/ee/ci/yaml/includes.html)
     * [includes -> rules](https://docs.gitlab.com/ee/ci/yaml/includes.html#use-rules-with-include)
     * [includes -> rules -> variables](https://docs.gitlab.com/ee/ci/yaml/#rulesvariables)
     * [includes -> templates -> override-configuration](https://docs.gitlab.com/ee/ci/yaml/includes.html#override-included-configuration-values)
     * [includes -> defaults](https://docs.gitlab.com/ee/ci/yaml/includes.html#use-default-configuration-from-an-included-configuration-file)
    
  1. Documentation - Instances Limits
     * [applicaton limits](https://docs.gitlab.com/ee/administration/instance_limits.html)
     
## Backlog I 

  1. gitlab ci/cd (Überblick)
     * [Jenkins mit Gitlab vs. gitlab ci/cd](gitlab/overview/jenkins-gitlab-vs-gitlab-cicd.md) 
    
  1. gitlab - setzen von Variablen
     * [Variablen für angepasste Builds verwenden und scheduled pipeline](gitlab/cases/variables-built-change.md)
    
  1. Exercises
     * [build with maven and using artifacts](https://github.com/jmetzger/training-gitlab-ci-cd/blob/main/gitlab/11-build-war-with-maven.md)
    
  1. gitlab ci/cd - docker
     * [Docker image automatisiert bauen - docker hub](/gitlab/09a-docker-build-use-docker-hub.md)
     * [Selbst gebauten Container manuell ausführen](/gitlab/docker/docker-image-manuell-ausfuehren.md)
     * [Neues Image in gitlab ci/cd aus gitlab registry verwenden](gitlab/global/default/image.md)
    
  1. Tipps&Tricks 
     * [Image/Container debuggen in mit gitlab ci/cd](gitlab/debug/container-kennenlernen.md)
     

## Backlog II

  1. Kubernetes (Refresher) 
     * [Aufbau von Kubernetes](kubernetes/architecture.md) 

  1. gitlab / Kubernetes CI/CD - old.old.schol with kubectl without agent)
     * [gitlab kubectl without agent](/gitlab/10-using-kubectl-old-style.md)

  1. gitlab / Kubernetes (gitops) 
     * [gitlab Kubernetes Agent with gitops - mode](/kubernetes-gitlab-gitops/example-gitlab-kubernetes-agent-with-gitops-mode.md)  
     
  1. gitlab / Kubernetes (CI/CD - old-school mit kubectl aber agent) 
     * [Vorteile gitlab-agent](/kubernetes/gitlab/advantage-gitlab-agent.md)
     * [Step 1: Installation gitlab-agent for kubernetes](/kubernetes-gitlab-ci-cd/99-gitlab-agent-with-kubectl.md)
     * [Step 2: Debugging KUBE_CONTEXT - Community Edition](kubernetes-gitlab-ci-cd/04-fix-problem-context-auto-devops.md)
     * [Step 3: gitlab-ci.yml setup for deployment and sample manifest](/kubernetes-gitlab-ci-cd/05-setup-deployment-with-sample-manifest.md)
     * [Documentation](https://docs.gitlab.com/ee/user/clusters/agent/ci_cd_workflow.html)

  1. gitlab / Kubernetes (CI/CD - Auto Devops) 
     * [Was ist Auto DevOps](/gitlab-ci-cd/was-ist-autodevops.md)
     * [Debugging KUBE_CONTEXT - Community Edition](kubernetes-gitlab-ci-cd/04-fix-problem-context-auto-devops.md)

  1. Tipps&Tricks
     * [Passwörter in Kubernetes verschlüsselt speichern](kubernetes/sealed-secrets.md)
  
