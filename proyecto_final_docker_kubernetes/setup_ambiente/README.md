# **Parte 1 – Setup del Ambiente (MicroK8s + Addons + Configuración v2.0)**

Esta seccion describe los pasos iniciales para preparar los ambientes, configurarlos,  habilitación de los componentes necesarios para ejecutar el Proyecto Final utilizando **MicroK8s**, **registry local**, **addons de Kubernetes**, y la preparación del entorno para desplegar imágenes personalizadas versión **v2.0**.

---

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
