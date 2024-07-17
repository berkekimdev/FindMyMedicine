# Proje Hakkında

Merhaba, bu projede kendi geliştirdiğim uygulamaları kullanarak dockerfile, docker-compose, kubernetes deployment ve service yaml'larını oluşturdum.

## Projeler

Bu sistemde kullanılan projeler ve ilgili bağlantılar aşağıda listelenmiştir:

- **Frontend:** [ilacimibul](https://github.com/berkekimdev/ilacimibul)
- **Backend:** [jwtbackend](https://github.com/berkekimdev/jwtbackend)

## Kurulum Notları

### Docker Compose

Docker Compose ile sistem kurulumu yapmadan önce, sunucudaki MySQL servisini inaktif etmeniz gerekmektedir.

### Kubernetes

Kubernetes üzerinde deploy işlemi gerçekleştirildikten sonra, sistem bileşenlerinin düzgün çalışabilmesi için hem frontend hem de backend servislerinin port forward işlemi yapılmalıdır.

Bu adımları takip ederek sistem kurulumunu tamamlayabilirsiniz.

# Proje Görselleri

Aşağıda, projenin çeşitli bileşenleri ve yapılandırmalarının görselleri bulunmaktadır:

## Jenkins

![Jenkins](https://github.com/berkekimdev/DockercomposeandKubernetesYamls/blob/main/Jenkins.jpg?raw=true)

## Jenkins Dockerhub'a Pipeline

![Jenkins Dockerhub Pipeline](https://github.com/berkekimdev/DockercomposeandKubernetesYamls/blob/main/JenkinsandDockerhubpush.jpg?raw=true)

## Prometheus

![Prometheus](https://github.com/berkekimdev/DockercomposeandKubernetesYamls/blob/main/Prometheus.jpg?raw=true)

## Grafana

![Grafana](https://github.com/berkekimdev/DockercomposeandKubernetesYamls/blob/main/Grafana.jpg?raw=true)

## Grafana ve Bütün Pod'lar

![Grafana ve Bütün Pod'lar](https://github.com/berkekimdev/DockercomposeandKubernetesYamls/blob/main/GrafanaandAllPods.jpg?raw=true)

