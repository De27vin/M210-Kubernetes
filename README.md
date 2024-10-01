Minikube ist nur um das Cluster zu starten oder löschen.
Kubectl ist um das Cluster zu konfigurieren.


Weil es auf meinem Linux Debian nicht funktioniert hat:
sudo systemctl stop apparmor → Stoppt anti-virus
minikube delete --all
minikube start --driver=docker --force


Minikube starten:
minikube start --driver=docker --force


Zeigt alle nodes an:
kubectl get node
kubectl node -o wide → Gibt IP-Adresse von nodes
Zeigt alle Pods an:
kubectl get pod


Kubernetes File als Input um was auch immer im File ist zu erstellen:
kubectl apply -f {Filename} (z.B. mongo-config.yaml)


Erstellte Components überprüfen:
kubectl get all → Alle überprüfen
kubectl get configmap → Nur configMap überprüfen
kubectl get secret → Nur secret überprüfen


App auf Browser öffnen:
kubectl get svc → Gibt einem alle laufenden Services zurück
minikube ip → IP:nodePort (in webapp.yaml file)

Die Logs überprüfen:
kubectl get pod
kubectl logs {NAME von Pod}

HILFE:
kubectl --help → Zeigt alle Optionen an
kubectl get --help → Zeigt nur für “get” Optionen an
