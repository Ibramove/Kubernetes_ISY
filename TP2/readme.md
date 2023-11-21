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

N'hésitez pas à ajuster la configuration du manifeste ou à consulter les ressources en ligne pour résoudre des problèmes spécifiques.

Ce Readme fournit une documentation de base pour le déploiement de l'application Simple WebApp Color. Vous pouvez le personnaliser davantage en fonction des besoins spécifiques de votre environnement.
