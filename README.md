# memcached-mock-opm-max-ocp-version

1) Create the mock with the Max OCP version annotation
2) Make the bundle and pushed it to: https://quay.io/repository/cmacedo/bundle-memcached
3) Executed : 

```
$ opm version
Version: version.Version{OpmVersion:“v1.17.3”, GitCommit:“b660eab”, BuildDate:“2021-06-03T09:58:39Z”, GoOs:“darwin”, GoArch:“amd64”}
```

```
rm -rf index.db
touch index.db
```

```
opm registry add -b quay.io/cmacedo/bundle-memcached -d index.db --container-tool=docker
```

```
open index.db 
```

SELECT * from properties
operator","version":"0.0.1"}	memcached-operator.v0.0.1	0.0.1	quay.io/cmacedo/bundle-memcached
