# Trabajo Práctico Final - Computer Vision

- Sancho Almenar, Mariano S-5778/9

# Instrucciones para ejecutar el Notebook

Este repositorio esta pensado para ser ejecutado tanto de forma local o en plataformas en línea como Google Colab.
En lo particular, recomiendo que sea ejecutado en Colab si no se tiene a disposición una GPU potente.

---
## Ejecuciones

## Colab: 
El notebook esta pensado para que se instalen automáticamente todas las dependencias necesarias para su correcta ejecución, como tambien así la descarga del dataset a utilizar.


[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1mRUonxoyVZcOv-eSvxFCJpoWmVy08c60?usp=sharing)
---
## Requisitos Local (Windows):

- **Para Docker GPU**:
  - Windows 10/11 con WSL2 instalado y habilitado.
  - Docker Desktop instalado y configurado para usar WSL2.
  - GPU NVIDIA con drivers y CUDA Toolkit compatible instalado.
  - NVIDIA Container Toolkit para Docker configurado ([Guía oficial](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html)).

- **Para entorno virtual CPU**:
  - Python 3.8+ instalado.
  - pip actualizado.

---

## Opción 1: Ejecutar con Docker (GPU)

1. Clona el repositorio y navega a la carpeta raíz donde está el archivo `devcontainer.json` y `requirements.txt`.

2. Abre PowerShell o terminal WSL2 y ejecuta:

   ```bash
   docker run --gpus all -it --rm -v ${PWD}:/workspace -w /workspace pytorch/pytorch:2.0.1-cuda11.7-cudnn8-runtime bash

  esto abrirá un shell dentro del contenedor con PyTorch y CUDA configurados.

3. Dentro del contenedor instala las siguientes dependencias: 

  ```
  pip install --upgrade pip 
   
  pip install -r requirements.txt 
  ```

4. Ejecutar el Notebook

---

## Opción 2: Ejecutar Entorno Virtual (CPU)

1. Con el repositorio abiero crear y activar el entorno virtual:

  ```
  python -m venv .venv

  .\.venv\Scripts\activate
  ```

2. Actualizar pip e instalar dependencias:

  ```
  python -m pip install --upgrade pip
  pip install -r requirements.txt

3. Ejecutar el Notebook