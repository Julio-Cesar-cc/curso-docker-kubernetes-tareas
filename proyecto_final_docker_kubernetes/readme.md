
# Proyecto Final - Curso Docker & Kubernetes

## Objetivo 

Preparar ambiente con microk8s, Docker y MetalLB

# Parte 1

## 1. Instalación de MicroK8s

MicroK8s se instaló utilizando Snap:

```bash
sudo snap install microk8s --classic
```

Se añadió el usuario actual al grupo `microk8s`:

```bash
sudo usermod -aG microk8s $USER
sudo chown -f -R $USER ~/.kube
```

Luego, se verificó el estado:

```bash
microk8s status --wait-ready
```

##  Activación de Addons esenciales

Los addons requeridos para Kubernetes se habilitaron así:

```bash
microk8s enable dns
microk8s enable ingress
microk8s enable storage
microk8s enable registry
microk8s enable metrics-server
```
**Screenshot:**

![Container creado](setup_ambiente/screenshots/part1_img2.png)


---
## 2. Proyecto v2.0 funcionando en el cluster

Ante de configurar el proyecto integrador se procede a verificar requisitos previos

### . Verificar que microk8s esté corriendo

```bash
microk8s status
```

### . Verificar conectividad del cluster

```bash
microk8s kubectl cluster-info
```

con las respuestas esperadas se procede con el punto 8, ya que los puntos 2,3,4,5,6,7 se realizaron en el anterior paso 

### 8. Preparar las Imágenes Docker - Importar imágenes desde Docker local

![Container creado](setup_ambiente/screenshots/part1_img2.png)


---
