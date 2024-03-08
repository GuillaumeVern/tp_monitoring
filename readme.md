## Objectifs :  
- Configurer un/des outil(s) de monitoring sur une application.
- Surveiller le fonctionnement de votre système (métriques système) et/ou de votre application (logs applicatif).
- Positionner des alertes lorsque certains seuils (CPU, RAM, Disk) sont franchis 
- Choix des technos : Grafana, Loki, Prometheus.


### Création d'un conteneur avec prometheus pour explorer l'application

docker run --name prometheus -d -p 127.0.0.1:9090:9090 prom/prometheus

![prometheus example](image.png)  

test d'une expression pour l'interface de graphiques (l'application se monitore elle-même pour le moment)

![graphique](image-1.png) 

second test avec l'utilisation du cpu

![cpu metric](image-2.png)


ajout d'autres service a monitorer

![alt text](image-3.png)
![alt text](image-4.png)

datasource prometheus dans grafana
![alt text](image-8.png)

prometheus job dans grafana
![alt text](image-7.png)

connexion a prometheus dans grafana
![alt text](image-8.png)

ajout du monitoring d'utilisation cpu dans le dashboard
![alt text](image-9.png)


dashboard dans grafana
![alt text](image-10.png)


