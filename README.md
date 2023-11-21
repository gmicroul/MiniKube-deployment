# MiniKube-deployment
Dashboard format:
http://127.0.0.1:55555/api/v1/namespaces/kubernetes-dashboard/services/http:kubernetes-dashboard:/proxy/#/workloads?namespace=_all

  sudo sysctl fs.protected_regular=0
  sudo minikube start --driver=podman --image-mirror-country=cn --force
  sudo minikube dashboard &
  sudo minikube addons enable metrics-server
  sudo  kubectl proxy --port=8003 --address='0.0.0.0' --accept-hosts='^.*' &

  sudo kubectl cluster-info
Kubernetes control plane is running at https://192.168.49.2:8443
CoreDNS is running at https://192.168.49.2:8443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

To further debug and diagnose cluster problems, use 'kubectl cluster-info dump'.
