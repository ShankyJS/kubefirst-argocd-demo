# ArgoCD con Kubefirst

[Kubefirst](https://kubefirst.io/) es una plataforma de GitOps que instala las herramientas más populares del mercado en cuestión de minutos 🚀.

![Arquitectura de Kubefirst k3d](image.png)

## Instalación

Instala Kubefirst con Homebrew

```bash
brew install kubefirst/tools/kubefirst
brew install mkcert
mkcert -install
```

## Creando nuestro ambiente local de K3d

Para crear nuestro ambiente en K3d necesitamos unos cuantos prerequisitos:

1. Tener instalado Docker y funcionando.
2. Una cuenta de GitHub y un GITHUB_TOKEN expuesto en nuestra terminal.

Simplemente corremos el siguiente comando:

```bash
kubefirst k3d create
```

## Credenciales de la infraestructura

Si necesitas obtener las credenciales de los sistemas que Kubefirst instaló puedes usar el comando:

```bash
kubefirst k3d root-credentials


  ----------------------------------------------------------------------
  k3d Authentication

  Keep this data secure. These passwords can be used to access the
  following applications in your platform.
  ----------------------------------------------------------------------

  Argo CD admin Password: password

  KBot User Password: random

  Vault root Token: randomtoken
```
