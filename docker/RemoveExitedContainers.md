If you want to remove all containers that are exited:
```
docker rm -f `docker ps -a | grep Exited | awk '{ print $1}'`
```


**Note:** This can be prevented with th `--rm` flag, but may still be needed if a system shuts down unexpectedly.
