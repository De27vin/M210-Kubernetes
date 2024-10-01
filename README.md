Hier ist ein Vorschlag für dein README:

```markdown
# Kubernetes Dokumentation

## Minikube und Kubectl

- **Minikube**: Wird verwendet, um das Kubernetes-Cluster zu starten oder zu löschen.
- **Kubectl**: Wird verwendet, um das Cluster zu konfigurieren und zu verwalten.

### Hinweise für Linux Debian:
Falls Minikube auf deinem Linux Debian nicht funktioniert, führe folgende Schritte aus:
```bash
sudo systemctl stop apparmor   # Stoppt AppArmor (anti-virus)
minikube delete --all          # Löscht alle Minikube-Cluster
minikube start --driver=docker --force  # Startet Minikube mit Docker als Treiber
```

### Minikube starten:
```bash
minikube start --driver=docker --force
```

### Nodes anzeigen:
- Zeigt alle Nodes im Cluster an:
  ```bash
  kubectl get node
  ```

- Zeigt zusätzliche Informationen wie die IP-Adressen der Nodes:
  ```bash
  kubectl get node -o wide
  ```

### Pods anzeigen:
- Zeigt alle laufenden Pods im Cluster an:
  ```bash
  kubectl get pod
  ```

### Konfigurationsdateien anwenden:
- Um Ressourcen aus einer Kubernetes-Konfigurationsdatei zu erstellen:
  ```bash
  kubectl apply -f {Dateiname}  # z.B. mongo-config.yaml
  ```

### Erstellte Komponenten überprüfen:
- Alle erstellten Ressourcen anzeigen:
  ```bash
  kubectl get all
  ```

- Nur ConfigMaps anzeigen:
  ```bash
  kubectl get configmap
  ```

- Nur Secrets anzeigen:
  ```bash
  kubectl get secret
  ```

### App im Browser öffnen:
- Zeigt alle laufenden Services im Cluster:
  ```bash
  kubectl get svc
  ```

- Ermittelt die Minikube-IP:
  ```bash
  minikube ip
  ```

- Die App kann mit IP:nodePort im Browser geöffnet werden. NodePorts werden definiert in der Webapp-Konfigurationsdatei, hier `webapp.yaml`.

### Logs überprüfen:
- Zeigt die Pods an:
  ```bash
  kubectl get pod
  ```

- Überprüft die Logs eines bestimmten Pods:
  ```bash
  kubectl logs {Pod-Name}
  ```

### Hilfe und Optionen:
- Allgemeine Hilfe für Kubectl:
  ```bash
  kubectl --help
  ```

- Hilfe für spezifische Befehle, z.B. `get`:
  ```bash
  kubectl get --help
  ```

```
