
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

---

¡Éxito en el proyecto final!
