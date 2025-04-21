START
Basic
Front: Describe how to create a kubectl context and provide a token for the user.
Back: 

The `kubectl config` command will adjust your `~/.kube/config` file.

Create a cluster entry like this:

```sh
kubectl config set-cluster mycluster \
	--server=http://... \
	--certificate-authority=mycluster.pem
```
Where `--server` points to the API server of the cluster, and `--certificate-authority` points to the CA file for this cluster.

Create a context like this:
```sh
kubectl config set-context mycontext \
  --cluster mycluster \
  --namespace mynamespace \
  --user myuser
```

Instead of the context name, we can use the `--current` flag to adjust the currently used context.

To provide a token for the user, use the `set-credentials` subcommand:
```sh
kubectl config set-credentials myuser --token=ABCD
```

To use the created context, say:
```sh
kubectl config use-context mycontext
```
<!--ID: 1712160434430-->
END
