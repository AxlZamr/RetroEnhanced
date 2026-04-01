![Logo](screenshots/clearlogo.png) 

[![Version](https://img.shields.io/badge/4.3.0-s?style=for-the-badge&logo=github&logoColor=ffffff&label=Versi%C3%B3n%20de%20RetroEnhanced&color=809CC9)
](https://github.com/tu-usuario/retroenhanced/releases)
[![Youtube](https://img.shields.io/badge/Canal%20de%20Youtube-yt?style=for-the-badge&logo=youtube&logoColor=ffffff&label=Subscribirse%20a&color=FF0000)
](https://youtube.com/@axl_zamr)
[![Discord](https://img.shields.io/badge/Comunidad%20de%20Discord-Unirse?style=for-the-badge&logo=discord&logoColor=ffffff&label=Unirse%20a&color=5865F2)
](https://discord.gg/aNfr96shm)

> Dale una nueva vida a tus clásicos. **RetroEnhanced** es una suite de herramientas de post-procesamiento para emuladores que mejora la calidad visual de los juegos retro utilizando algoritmos modernos de escalado y filtros avanzados.

---

## 📖 Tabla de Contenidos

* [🧐 Acerca del Proyecto](#-acerca-del-proyecto)
* [🎨 Experiencia Visual (Theming)](#-experiencia-visual-theming)
    * [Personalización y Layouts](#personalización-y-layouts)
    * [Galería (Demostración Visual)](#galería-demostración-visual)
* [ ✨ Características Principales](#-características-principales)
* [💻 Requisitos del Sistema](#-requisitos-del-sistema)
* [🛠️ Instalación](#%EF%B8%8F-instalación)
* [🤝 Créditos y Referencias](#-creditos-y-referencias)

---

## 🧐 Acerca del Proyecto

**RetroEnhanced** nació de la pasión por los videojuegos clásicos y la frustración de verlos pixelados en monitores 4K modernos. El objetivo no es solo estirar la imagen, sino *reinterpretarla* inteligentemente.

A diferencia de los filtros simples integrados en muchos emuladores, RetroEnhanced implementa una cadena de renderizado (pipeline) que combina:
1.  **Algoritmos de Escalado:** (ej. xBRZ, ScaleHQ) para suavizar bordes sin perder definición.
2.  **Shaders de Post-Procesamiento:** Para simular la curvatura de CRT, líneas de escaneo (scanlines) y la floración de color (bloom) original.
3.  **Corrección de Color:** Ajusta la paleta para que coincida con los estándares de visualización modernos (NTSC/PAL a sRGB).

| Problema | Solución de RetroEnhanced |
| :--- | :--- |
| Píxeles "estirados" en pantallas 4K/1080p. | Integer Scaling forzado: Mantiene la proporción perfecta de píxeles sin distorsión. |
| Interfaz genérica que no encaja con el juego. | Integración de Arte Dinámico: El tema de RetroBat cambia sutilmente para coincidir con la estética del sistema activo. |
| Input Lag visual por filtros pesados. | Shaders de Baja Latencia: Optimizados específicamente para los núcleos (cores) de RetroArch dentro de RetroBat. |
| Colores lavados en paneles IPS/OLED modernos. | Perfiles de Color Rec.709: Ajuste automático de la saturación para replicar el fósforo de las TV de tubo. |
| Navegación lenta en colecciones masivas. | VRAM Caching: Estructura de archivos optimizada para que el scroll en RetroBat sea fluido (60fps). |
| Colores apagados o incorrectos | Perfiles de color LUTs avanzados. |
| Imagen demasiado "limpia" o estéril | Simulación de texturas y fósforo CRT. |

---

## 🎨 Experiencia Visual (Theming)

RetroEnhanced utiliza un sistema dinámico de capas que permite una transición fluida entre el arte del juego y la información técnica, optimizando el uso de la memoria de video (VRAM).

### Vistas de Sistema
Diseñadas para adaptarse a cualquier tipo de catálogo, desde colecciones pequeñas hasta librerías completas.

<p align="center">
  
| Modo Gris | Modo Oscuro | Modo Blanco | Modo Colorido |
| :--- | :--- | :--- | :--- |
| ![IMG](screenshots/Interfaz-en-Gris/gray-menu.png)  | ![IMG](screenshots/Interfaz-en-Oscuro/dark-menu.png) | ![IMG](screenshots/Interfaz-en-Claro/white-menu.png)  |  ![IMG](screenshots/Interfaz-en-Colorido/colorful-menu.png) | 
| ![IMG](screenshots/Interfaz-en-Gris/gray-detallado.png)  | ![IMG](screenshots/Interfaz-en-Oscuro/dark-detallado.png) | ![IMG](screenshots/Interfaz-en-Claro/white-detallado.png) | ![IMG](screenshots/Interfaz-en-Colorido/colorful-detallado.png) | 
| ![IMG](screenshots/Interfaz-en-Gris/gray-cajas.png)  | ![IMG](screenshots/Interfaz-en-Oscuro/dark-cajas.png) | ![IMG](screenshots/Interfaz-en-Claro/white-cajas.png)|  ![IMG](screenshots/Interfaz-en-Colorido/colorful-cajas.png) | 
| ![IMG](screenshots/Interfaz-en-Gris/gray-cuadricula.png)  | ![IMG](screenshots/Interfaz-en-Oscuro/dark-cuadricula.png) | ![IMG](screenshots/Interfaz-en-Claro/white-cuadricula.png) |  ![IMG](screenshots/Interfaz-en-Colorido/colorful-cuadricula.png) | 
 | ![IMG](screenshots/Interfaz-en-Gris/gray-tiles.png)  | ![IMG](screenshots/Interfaz-en-Oscuro/dark-tiles.png) | ![IMG](screenshots/Interfaz-en-Claro/white-tiles.png)|  ![IMG](screenshots/Interfaz-en-Colorido/colorful-tiles.png) | 
| ![IMG](screenshots/Interfaz-en-Gris/gray-cajas-verticales.png)  | ![IMG](screenshots/Interfaz-en-Oscuro/dark-cajas-verticales.png) | ![IMG](screenshots/Interfaz-en-Claro/white-cajas-verticales.png) | ![IMG](screenshots/Interfaz-en-Colorido/colorful-cajas-verticales.png) | 
</p>

---

### Personalización y Layouts
Inspirado en la modularidad de **[RetroFix]([#-sobre-retroenhanced](https://github.com/20GotoTen/es-theme-retrofix))**, puedes alterar profundamente la apariencia del tema desde el menú de `Opciones de Tema` de EmulationStation sin editar archivos XML.

#### 🔧 Opciones Disponibles:

* **Estilos para menú (Paletas):**
    * `Modo Normal`: Gris clasico con tonos claros sin saturar la interfaz.
    * `Modo Oscuro`: Gris mucho más oscuro, para dar un entorno menos vibrante.
    * `Modo Blanco`: Cambia por completo la interfaz, ahora es un blanco grisaseo bastante claro.
    * `Modo Colorido`: Gradientes vibrantes y con un efecto arcoiris.

* **Bibliotecas (Lista de juegos):**
    * **Detallado:** El arte y el video se alinean al centro de la pantalla.
    * **Cuadricula:** El arte y el video se alinean al centro de la pantalla.
    * **Detallado + Caja:** El arte y el video se alinean al centro de la pantalla.
    * **Cajas:** El arte y el video se alinean al centro de la pantalla.
    * **Tiles:** El arte y el video se alinean al centro de la pantalla.
    * **Cajas + Información:** El arte y el video se alinean al centro de la pantalla.
    * **Cajas en Vertical:** El arte y el video se alinean al centro de la pantalla.
    
* **Logo de consolas (Región):**
    * **Automatico:** Los logos de consolas seran aplicaran de forma automatica.
    * **Japón:** Los logos de consolas seran todos de Japón.
    * **America:** Los logos de consolas seran todos de America.
    * **Europa:** Los logos de consolas seran todos de Europa.


* **Y OTRAS OPCIONES MÁS**


> [!TIP]
> **Recomendación de Rendimiento:** Si usas una Raspberry Pi o hardware limitado, selecciona el modo `VRAM Optimized` en la sección de layouts para desactivar las animaciones pesadas de los logos.

---

## Galería (Demostración Visual)
Con el uso de los shaders que se inluyen en el paquete `shaders-retroenhanced.zip` desde la página de [Releases](https://github.com/tu-usuario/retroenhanced/releases).

<p align="center">
  
### Comparación 1: Pixel Art (SNES)
</p>

| Antes | Despues |
| :--- | :--- |
| ![IMG](screenshots/Shaders-SNES/antes.png) | ![IMG](screenshots/Shaders-SNES/despues.png) |

<p align="center">
  <em>Izquierda: Resolución Nativa. Derecha: RetroEnhanced (Corrección de perspectiva + FXAA + Scanlines).</em>
</p>


### Comparación 2: Primeros 3D (PS1)

| Antes | Despues |
| :--- | :--- |
| ![IMG](screenshots/Shaders-PSX/antes.png) | ![IMG](screenshots/Shaders-PSX/despues.png) |

</p>

<p align="center">
  <em>Izquierda: Resolución Nativa. Derecha: RetroEnhanced (Corrección de perspectiva + FXAA + Scanlines).</em>
</p>
<p align="center">
  <em>Usando el preset RetroEnhanced - PSX Dark</em>
</p>


### Comparación 3: Consolas portatiles (GBC)
</p>


| Antes | Despues |
| :--- | :--- |
| ![IMG](screenshots/Shaders-GBC/antes.png) | ![IMG](screenshots/Shaders-GBC/despues.png) |

<p align="center">
  <em>Izquierda: Resolución Nativa. Derecha: RetroEnhanced (Corrección de perspectiva + FXAA + Scanlines).</em>
</p>


---


## ✨ Características Principales

* **⚡ Soporte Multmotor:** Compatible con núcleos de RetroArch, emuladores independientes (como Dolphin, PCSX2) e incluso algunos juegos de PC antiguos a través de inyección de DLL.
* **🖼️ Algoritmos de Escalado Propios:** Implementación optimizada de `xBRZ` (hasta 6x) y `Hybrid-Scale` (nuestro algoritmo personalizado).
* **🕹️ Perfiles CRT Realistas:** No solo líneas negras. Simulamos:
    * Curvatura de la pantalla (Barrel distortion).
    * Máscara de sombra (Shadow Mask/Aperture Grille).
    * Sangrado de color y Bloom.
* **🎨 Ajuste de Color HDR:** Soporte experimental para pantallas HDR para resaltar los brillos y contrastes originales.
* **⚙️ Interfaz de Configuración en Tiempo Real:** Un menú superpuesto (overlay) te permite ajustar los filtros mientras juegas.
* **📦 Bajo Impacto en Rendimiento:** Optimizado para funcionar en hardware de gama media y GPUs integradas modernas.

---

## 💻 Requisitos del Sistema

### Mínimos
* **SO:** Windows 7/8/10/11 (64-bit) o Linux-Batocera (con soporte Vulkan/OpenGL moderno).
* **CPU:** Procesador con al menos 4 nucleos y 4 hilos de preferencia
* **GPU:** Gráficos integrados Intel HD 620 o AMD Vega (Soporte Shader Model 5.0).
* **API:** Vulkan 1.1 (Recomendado) u OpenGL 4.5.

### Recomendados
* **GPU:** NVIDIA GTX 1060 / AMD RX 580 o superior.
* **Pantalla:** Monitor 1440p o 4K para apreciar el escalado de alta resolución.

Ideal para jugar juegos de ps2, wii, u otro tipo exigente con los shaders sin ningun problema, tirón o error visual.

---

## 🛠️ Instalación

Actualmente, RetroEnhanced se distribuye como un paquete que se aplica a una vez ya inslalado "retrobat" o "batocera".

### Método Retrobat: Instalación Manual

1.  Descarga la última versión de `retroenhanced-for-retrobat.zip` desde la página de [Releases](https://github.com/tu-usuario/retroenhanced/releases).
2.  Copia todos los archivos dentro del zip
3.  Y pegalos en la carpeta raiz de RetroBat
4.  Y listo, eres libre de usarlo y disfrutar de este proyecto.

### Método Batocera: Instalación Manual

 `En desarrollo...`


---

## 🤝 Créditos y Referencias

El desarrollo de **RetroEnhanced** es posible gracias a la generosidad de la comunidad de preservación y emulación. Este proyecto se construye sobre los hombros de gigantes:

### 🎨 Inspiración y Código de Temas
* **[20GotoTen (Retrofix)](https://github.com/20GotoTen/es-theme-retrofix) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)]([https://opensource.org/licenses/MIT](https://creativecommons.org/licenses/by-nc-sa/4.0/)):** Referencia principal para la estructura lógica del archivo `theme.xml`, el manejo avanzado de vistas y la organización profesional de activos (assets). 
* **[AlekFull](https://github.com/AlekFull):** Por los conceptos de diseño artístico en sistemas de emulación que inspiraron nuestra paleta de colores.

### 🎨 Post-Procesamiento y Visuales (Shaders)
* **[HyperspaceMadness (Mega Bezel)](https://github.com/HyperspaceMadness):** Por el increíble **HSM Mega Bezel Reflection Shader**, que proporciona los reflejos dinámicos y marcos realistas que son el núcleo visual de RetroEnhanced.
* **[Duimon (Graphics)](https://github.com/Duimon):** Por los assets gráficos y presets de alta calidad que complementan los Mega Bezels en múltiples sistemas.
* 
### ⚙️ Ecosistema y Motores
* **[RetroBat Team](https://www.retrobat.org/):** Por crear el mejor frontend basado en Windows, permitiendo una integración fluida de scripts y configuraciones personalizadas.
* **[Libretro / RetroArch](https://www.libretro.com/):** Por el desarrollo de los núcleos de emulación y el potente motor de Shaders (Slang/Glsl) que utilizamos para el post-procesamiento.
* **[EmulationStation Desktop Edition](https://es-de.org/):** Por mantener la base del motor de temas que da vida a nuestra interfaz.

### 🖼️ Recursos Multimedia
* **[ScreenScraper.fr](https://www.screenscraper.fr/):** La fuente principal de donde provienen los metadatos, manuales y artes de alta calidad que dan vida a las vistas de RetroEnhanced.
* **[Dan Patrick (Recalbox Themes)](https://github.com/recalbox):** Por las bases de algunos iconos de sistemas y logotipos vectorizados (SVG).

---

> [!IMPORTANT]
> **RetroEnhanced** es un proyecto gratuito y de código abierto creado por y para la comunidad. Si has contribuido a alguna de las herramientas mencionadas arriba, ¡gracias por hacer esto posible!

<p align="center">
  <br>
  <b>
