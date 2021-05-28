# cron-git-pull-docker

Git clone or git pull periodically to a folder.

## Usage

```
docker run \
  -v /my-folder-where-the-git-clone-must-go/:/folder-to-clone/
  -e GIT_REPOSITORY_URL="https://github.com/raspberrypi/documentation.git" \
  -e CRON="* * * * * *" \
  abesesr/cron-git-pull-docker:1.0.0
```

This command will firstly git clone this github repository https://github.com/raspberrypi/documentation.git to your local folder `/my-folder-where-the-git-clone-must-go/`, then it will wait 1 minute and it will run a `git pull` to update the new changes from the github (if any).
