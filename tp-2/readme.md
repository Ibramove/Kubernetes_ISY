# - Déploiement de l'Application Simple WebApp Color

Ce document explique les étapes que j'ai suivies pour déployer avec succès l'application Simple WebApp Color sur un cluster Kubernetes. L'application utilise l'image "mmumshad/simple-webapp-color" avec la couleur spécifiée comme rouge.

## Étapes de déploiement

### 1. Configuration du Manifeste Kubernetes

Le fichier de configuration du pod (`simple-webapp-pod.yml`) a été créé avec les spécifications nécessaires pour déployer l'application avec la couleur rouge. Assurez-vous que ce fichier est correctement configuré avec les bonnes spécifications pour le conteneur et les éventuelles variables d'environnement.

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: simple-webapp-pod
spec:
  containers:
  - name: simple-webapp-container
    image: mmumshad/simple-webapp-color
    env:
    - name: APP_COLOR
      value: "red"
```

### 2. Déploiement du Pod

Le pod a été déployé en utilisant la commande `kubectl apply` avec le fichier de configuration du manifeste.

```bash
kubectl apply -f simple-webapp-pod.yml
```

Vérifiez que le pod est en cours d'exécution en utilisant la commande suivante :

```bash
kubectl get pods
```

### 3. Exposition du Pod

Le pod a été exposé en redirigeant le port 8080 du pod vers le port 8080 de la machine locale à l'aide de la commande `kubectl port-forward`.

```bash
kubectl port-forward simple-webapp-pod 8080:8080 --address 0.0.0.0
```

### 4. Vérification de l'Accessibilité

L'application est accessible en ouvrant le port 8080 sur la machine locale. Vous pouvez utiliser un navigateur web ou la commande `curl` pour vérifier l'accessibilité.

Exemple avec `curl` :

```bash
curl http://localhost:8080
```

Assurez-vous que l'application s'affiche correctement avec la couleur rouge spécifiée.
# Readme - Déploiement de l'Application Simple WebApp Color

Ce document explique les étapes que j'ai suivies pour déployer avec succès l'application Simple WebApp Color sur un cluster Kubernetes. L'application utilise l'image "mmumshad/simple-webapp-color" avec la couleur spécifiée comme rouge.

## Étapes de déploiement

### 1. Configuration du Manifeste Kubernetes

Le fichier de configuration du pod (`simple-webapp-pod.yml`) a été créé avec les spécifications nécessaires pour déployer l'application avec la couleur rouge. Assurez-vous que ce fichier est correctement configuré avec les bonnes spécifications pour le conteneur et les éventuelles variables d'environnement.

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: simple-webapp-pod
spec:
  containers:
  - name: simple-webapp-container
    image: mmumshad/simple-webapp-color
    env:
    - name: APP_COLOR
      value: "red"
```

### 2. Déploiement du Pod

Le pod a été déployé en utilisant la commande `kubectl apply` avec le fichier de configuration du manifeste.

```bash
kubectl apply -f simple-webapp-pod.yml
```

Vérifiez que le pod est en cours d'exécution en utilisant la commande suivante :

```bash
kubectl get pods
```

### 3. Exposition du Pod

Le pod a été exposé en redirigeant le port 8080 du pod vers le port 8080 de la machine locale à l'aide de la commande `kubectl port-forward`.

```bash
kubectl port-forward simple-webapp-pod 8080:8080 --address 0.0.0.0
```

### 4. Vérification de l'Accessibilité

L'application est accessible en ouvrant le port 8080 sur la machine locale. Vous pouvez utiliser un navigateur web ou la commande `curl` pour vérifier l'accessibilité.

Exemple avec `curl` :

```bash
curl http://localhost:8080
```
# Readme - Déploiement de l'Application Simple WebApp Color

Ce document explique les étapes que j'ai suivies pour déployer avec succès l'application Simple WebApp Color sur un cluster Kubernetes. L'application utilise l'image "mmumshad/simple-webapp-color" avec la couleur spécifiée comme rouge.

## Étapes de déploiement

### 1. Configuration du Manifeste Kubernetes

Le fichier de configuration du pod (`simple-webapp-pod.yml`) a été créé avec les spécifications nécessaires pour déployer l'application avec la couleur rouge. Assurez-vous que ce fichier est correctement configuré avec les bonnes spécifications pour le conteneur et les éventuelles variables d'environnement.

```yaml
apiVersion: v1
kind: Pod
metadata:
  name: simple-webapp-pod
spec:
  containers:
  - name: simple-webapp-container
    image: mmumshad/simple-webapp-color
    env:
    - name: APP_COLOR
      value: "red"
```

### 2. Déploiement du Pod

Le pod a été déployé en utilisant la commande `kubectl apply` avec le fichier de configuration du manifeste.

```bash
kubectl apply -f simple-webapp-pod.yml
```

Vérifiez que le pod est en cours d'exécution en utilisant la commande suivante :

```bash
kubectl get pods
```

### 3. Exposition du Pod

Le pod a été exposé en redirigeant le port 8080 du pod vers le port 8080 de la machine locale à l'aide de la commande `kubectl port-forward`.

```bash
kubectl port-forward simple-webapp-pod 8080:8080 --address 0.0.0.0
```

### 4. Vérification de l'Accessibilité

L'application est accessible en ouvrant le port 8080 sur la machine locale. Vous pouvez utiliser un navigateur web ou la commande `curl` pour vérifier l'accessibilité.

Exemple avec `curl` :

```bash
curl http://localhost:8080
```

Assurez-vous que l'application s'affiche correctement avec la couleur rouge spécifiée.

## Problèmes courants

Si le pod reste dans l'état "Pending" ou si des erreurs surviennent lors du déploiement, consultez les journaux du pod pour identifier les problèmes spécifiques.

```bash
kubectl logs <nom du pod>
```

De plus, vérifiez les événements associés au pod pour obtenir des informations supplémentaires.

```bash
kubectl describe pod <nom du pod>
```

N'hésitez pas à ajuster la configuration du manifeste ou à consulter les ressources en ligne pour résoudre des problèmes spécifiques.

Ce Readme fournit une documentation de base pour le déploiement de l'application Simple WebApp Color. Vous pouvez le personnaliser davantage en fonction des besoins spécifiques de votre environnement.
Assurez-vous que l'application s'affiche correctement avec la couleur rouge spécifiée.


## Problèmes courants

Si le pod reste dans l'état "Pending" ou si des erreurs surviennent lors du déploiement, consultez les journaux du pod pour identifier les problèmes spécifiques.

```bash
kubectl logs <nom du pod>
```

De plus, vérifiez les événements associés au pod pour obtenir des informations supplémentaires.

```bash
kubectl describe pod <nom du pod>
```

N'hésitez pas à ajuster la configuration du manifeste ou à consulter les ressources en ligne pour résoudre des problèmes spécifiques.

Ce Readme fournit une documentation de base pour le déploiement de l'application Simple WebApp Color. Vous pouvez le personnaliser davantage en fonction des besoins spécifiques de votre environnement.

## Problèmes courants

Si le pod reste dans l'état "Pending" ou si des erreurs surviennent lors du déploiement, consultez les journaux du pod pour identifier les problèmes spécifiques.

```bash
kubectl logs <nom du pod>
```

De plus, vérifiez les événements associés au pod pour obtenir des informations supplémentaires.

```bash
kubectl describe pod <nom du pod>
```

# Readme - Déploiement NGINX sur Kubernetes

Ce document décrit les étapes suivies pour déployer NGINX sur Kubernetes en utilisant des manifests YAML, les commandes impératives, et la gestion du code avec GitHub.

## Étapes de Déploiement

### 5. Création du Manifeste NGINX Deployment

Le fichier manifest `nginx-deployment.yml` a été créé pour déployer deux répliques d'un pod NGINX en version 1.18.0.

```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: nginx-deployment
spec:
  replicas: 2
  selector:
    matchLabels:
      app: nginx
  template:
    metadata:
      labels:
        app: nginx
    spec:
      containers:
      - name: nginx-container
        image: nginx:1.18.0
```

### 6. Déploiement Initial et Vérification

- Le déploiement NGINX a été lancé avec la commande `kubectl apply -f nginx-deployment.yml`.
- Le nombre de pods créés a été vérifié avec la commande `kubectl get pods`.
- Les ressources Deployment et ReplicaSet, ainsi que la version de l'image utilisée, ont été vérifiées avec `kubectl get deployments` et `kubectl get replicaset`.

### 7. Mise à jour vers l'Image "latest"

- Le fichier `nginx-deployment.yml` a été modifié pour utiliser l'image NGINX en version "latest".
- La mise à jour a été appliquée avec la commande `kubectl apply -f nginx-deployment.yml`.

### 8. Vérification après la Mise à Jour

- Après la mise à jour, plusieurs ReplicaSets ont été créés, l'un pour la version précédente de l'image et l'autre pour la version "latest".
- Le nombre de ReplicaSets a été vérifié avec la commande `kubectl get replicaset`.
- L'image utilisée par le ReplicaSet en cours d'utilisation a été vérifiée avec `kubectl describe deployment nginx-deployment`.

### 9. Suppression et Recréation des Ressources

- Toutes les ressources ont été supprimées avec les commandes `kubectl delete deployment nginx-deployment` et `kubectl delete pods --all`.
- Les ressources ont été recréées avec des commandes impératives :
  ```bash
  kubectl create deployment nginx-deployment --image=nginx:latest --replicas=2
  ```

### 10. Organisation dans un Répertoire et Poussée sur GitHub

- Un répertoire `Kubernetes-training` et un sous-dossier `tp-2` ont été créés.
- Les manifests YAML ont été copiés dans ce répertoire.
- Le répertoire a été initialisé comme un dépôt Git et les fichiers ont été ajoutés, commités et poussés sur GitHub :
  ```bash
  git init
  git add .
  git commit -m "Initial commit"
  git remote add origin <lien_vers_votre_repo_github>
  git push -u origin master
  ```

Replacez `<lien_vers_votre_repo_github>` par le lien réel de votre dépôt GitHub.

Ce Readme documente le processus de déploiement NGINX sur Kubernetes, de la création des manifests à la gestion du code avec GitHub. 
