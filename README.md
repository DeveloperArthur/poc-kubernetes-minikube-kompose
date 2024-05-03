## Como converter seu docker-compose.yaml em Kubernetes files com Kompose e deployar no Kubernetes localmente com Minikube

<img src="assets/kubernetes.png" height="200">

Instale o Minikube e Kompose:
- https://kompose.io/
- https://minikube.sigs.k8s.io/docs/start/

<p>
    <img src="assets/kompose.png" height="80">
    <img src="assets/minikube.jpeg" height="80">
</p>

### Starte o Minikube:
    
    minikube start

### Converte o compose em arquivos Kubernetes e joga esses arquivos em um diretório chamado 'kubernetes':

    kompose convert -f docker-compose.yaml

![obj](assets/kompose2.png)

### Deploy desses arquivos Kubernetes no Minikube:

    kubectl apply -f .

![obj](assets/apply.png)

### Para ver os Pods via terminal:
    
    kubectl get po

![obj](assets/pods.png)

### Para acessar o Dashboard do Minikube:

    minikube dashboard

![obj](assets/dashboard.png)
![obj](assets/dashboard2.png)


