# Jenkins-rails-postgres-docker

This docker compose environment of Jenkins CI can test rails with postgres.

It's a modified version of [Official Jenkins Docker image](https://github.com/jenkinsci/docker)

# Usage

1. Clone this project and run command below.

```
docker-compose up
```

2. Copy admin password from terminal then put it into executed jenkins container.

3. Fill user info likes id,password,email etc.

4. Create a Multi-configuration project.

5. Choose git from `Source Code Management` section.

6. Copy [https://github.com/dorajistyle/rails-postgres-sample-for-jenkins](https://github.com/dorajistyle/rails-postgres-sample-for-jenkins) and put into Repository URL field.

7. Check rbenv build wrapper from 'Build Environment'.  
Put `2.3.1` into The Ruby version field.  
Put `bundler,rake,execjs` into Preinstall gem list.

8. Chose Execute shell from the select box called Add build step.  
Put `bash jenkins-test.sh` into Command field.

9. Save configuration and run build with `Build Now` button in left side menu of the project.

