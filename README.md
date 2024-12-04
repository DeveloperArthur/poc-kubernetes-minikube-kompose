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

### Converte o compose em arquivos Kubernetes:

    kompose convert -f docker-compose.yaml

![obj](assets/kompose2.png)

### Deploy desses arquivos Kubernetes no Minikube:

    kubectl apply -f .

![obj](assets/apply.png)

### Para ver os Pods via terminal:
    
    kubectl get pods

![obj](assets/pods.png)

### Para acessar o Dashboard do Minikube:

    minikube dashboard

![obj](assets/dashboard.png)
![obj](assets/dashboard2.png)

## Outros Comandos Minikube

- **Iniciar o Minikube com o CNI Calico:**

    ```bash
    minikube start --cni=calico
    ```

- **Executar um pod temporário com a imagem `hello-world`:**

    ```bash
    kubectl run --rm --stdin --image=hello-world --restart=Never --request-timeout=30 test-pod
    ```

- **Adicionar um nó no cluster do Minikube:**

    ```bash
    minikube node add
    ```

Você pode executar este comando quantas vezes quiser para adicionar novos nós ao cluster.

- **Deletar o cluster Minikube:**

    ```bash
    minikube delete
    ```
