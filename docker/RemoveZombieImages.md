
When you have a list of zombie/none docker images, like this:
```
<none>                     <none>              d9cf1b925335        18 hours ago        4.206 GB
<none>                     <none>              f3efeec3061f        18 hours ago        4.198 GB
<none>                     <none>              72522c49840c        13 days ago         4.182 GB
<none>                     <none>              95a6d94a057a        2 weeks ago         4.182 GB
<none>                     <none>              dca1670b3c26        2 weeks ago         4.124 GB
<none>                     <none>              281acf015ff4        2 weeks ago         4.124 GB
<none>                     <none>              8736d93bcb3c        2 weeks ago         4.124 GB
<none>                     <none>              15a97315ad6f        2 weeks ago         4.139 GB
<none>                     <none>              93a423f5b14b        2 weeks ago         4.139 GB
<none>                     <none>              91faf65b2e9e        3 weeks ago         4.103 GB
<none>                     <none>              a42d66a71446        3 weeks ago         4.103 GB
```

You can remove them with the following command:
```
docker rmi `docker images  | grep none | awk '{ print $3}'`
```
