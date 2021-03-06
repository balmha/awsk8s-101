# Kind playground

## Introduccion

Kind es una implementacion liviana de kubernetes que corre sobre Docker, su nombre proviene del ingles *Kubernetes IN Docker*

Kind es una forma facil y rapida de crear un cluster de kubernetes para propositos como:

* Aprendizaje
* Integracion Continua

## Como crear un Cluster

### Inicio rapido

```shell
$ kind create cluster --name aws101
Creating cluster "aws101" ...
 â Ensuring node image (kindest/node:v1.21.1) đŧ
 â Preparing nodes đĻ
 â Writing configuration đ
 â Starting control-plane đšī¸
 â Installing CNI đ
 â Installing StorageClass đž
Set kubectl context to "kind-aws101"
You can now use your cluster with:

kubectl cluster-info --context kind-aws101

Not sure what to do next? đ  Check out https://kind.sigs.k8s.io/docs/user/quick-start/


$ kubectl get nodes
NAME                   STATUS   ROLES                  AGE   VERSION
aws101-control-plane   Ready    control-plane,master   59s   v1.21.1
```

### Como eliminar un cluster

```shell
$ kind delete cluster --name aws101
Deleting cluster "aws101" ...
```

### Crear un cluster usando archivo de configuraciones

```shell
$ kind create cluster --config kind-cluster.yml
Creating cluster "kind" ...
 â Ensuring node image (kindest/node:v1.21.1) đŧ
 â Preparing nodes đĻ đĻ đĻ
 â Writing configuration đ
 â Starting control-plane đšī¸
 â Installing CNI đ
 â Installing StorageClass đž
 â Joining worker nodes đ
Set kubectl context to "kind-kind"
You can now use your cluster with:

kubectl cluster-info --context kind-kind

Thanks for using kind! đ
```

## Autor

Damian A. Gitto Olguin
[AWS Community Hero](https://www.youtube.com/c/damianolguinAWSHERO)
[@enlink](https://twitter.com/enlink)] / [@teracloudio](https://twitter.com/teracloudio)
<https://teracloud.io>
