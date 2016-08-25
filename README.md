# Jenkins-rails-postgres-docker

This docker compose environment of Jenkins CI can test rails with postgres.

It's a modified version of [Official Jenkins Docker image](https://github.com/jenkinsci/docker)

# Usage

Clone this project and run command below.

```
docker-compose up
```


1. Copy admin password from terminal then put it into executed jenkins container.

1. Fill user info likes id,password,email etc.

1. Create a Multi-configuration project.

1. Choose git from `Source Code Management` section.

1. Copy [https://github.com/dorajistyle/rails-postgres-sample-for-jenkins](https://github.com/dorajistyle/rails-postgres-sample-for-jenkins) and put into Repository URL field.

1. Check rbenv build wrapper from 'Build Environment'.  
Put `2.3.1` into The Ruby version field.  
Put `bundler,rake,execjs` into Preinstall gem list.

1. Chose Execute shell from the select box called Add build step.  
Put `bash jenkins-test.sh` into Command field.

1. Save configuration and run build with `Build Now` button in left side menu of the project.

