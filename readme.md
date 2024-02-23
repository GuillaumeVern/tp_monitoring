## Objectifs :  
- Configurer un/des outil(s) de monitoring sur une application.
- Surveiller le fonctionnement de votre système (métriques système) et/ou de votre application (logs applicatif).
- Positionner des alertes lorsque certains seuils (CPU, RAM, Disk) sont franchis 
- Choix des technos : Elasticsearch, Kibana, Logstash (ELK) ou Grafana, Loki, Prometheus.


### Création d'un conteneur avec prometheus pour explorer l'application

docker run --name prometheus -d -p 127.0.0.1:9090:9090 prom/prometheus

![prometheus example](image.png)  

test d'une expression pour l'interface de graphiques (l'application se monitore elle-même pour le moment)

![graphique](image-1.png) 

second test avec l'utilisation du cpu

![cpu metric](image-2.png)

