<p align="center">
  <img src="https://xirafa.soyjuli.us/assets/logo.webp" alt="Proyecto XIRAFA Logo" width="120" />
</p>
<p align="center">
  <strong>Este proyecto forma parte de la iniciativa del <a href="https://xirafa.soyjuli.us" target="_blank">Proyecto XIRAFA</a>.</strong>
</p>

# 🇨🇴 XiraVault Colombia: Búnker Digital y Kit de Autonomía Off-Grid

> **"Que no pase nada, hasta que pasa."** Un framework Open Source soberano, modular y 100% desconectado para la resiliencia familiar, comunitaria y de operadores en Colombia y Latinoamérica.

<p align="center">
  <img src="https://img.shields.io/badge/Open_Source-100%25-green?style=for-the-badge" alt="Open Source" />
  <img src="https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black" alt="Linux" />
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License MIT" />
</p>

---

## 🔍 ¿Qué es XiraVault Colombia?

**XiraVault Colombia** es un proyecto de código abierto (*Open Source*) diseñado para resolver uno de los mayores riesgos de nuestra era digital: **¿qué ocurre cuando se interrumpe el suministro eléctrico por días, caen las redes de telecomunicaciones, desaparece la señal celular y el acceso a internet o a Google se esfuma por completo?**

Inspirado en los principios del **preparacionismo urbano y rural (preppers)**, la soberanía tecnológica y las redes de emergencia (como la radioafición y nodos locales), XiraVault empaqueta en un formato portátil y económico (una memoria USB dual o un servidor local en Docker) una biblioteca táctica de supervivencia, manuales de salud, guías de agricultura tropical, cartografía offline y herramientas de conocimiento libre adaptadas a la realidad geográfica y social de Colombia.

---

## 🎯 ¿Por qué el Preparacionismo y la Autonomía Offline en Colombia?

En regiones como el Eje Cafetero, Antioquia, Cundinamarca y todo el territorio colombiano, nos enfrentamos frecuentemente a emergencias operativas y naturales:

* **Emergencias Climáticas y Sismológicas:** Inundaciones por temporales invernales, deslizamientos de tierra en vías principales y la constante amenaza sísmica.
* **Apagones y Fallas de Infraestructura:** Cortes de energía prolongados o caídas en los servicios de los proveedores de internet (*ISPs*).
* **Zonas de Silencio Comunicativo:** Veredas, zonas rurales y áreas de montaña donde la señal móvil es nula o inestable, requiriendo redes de apoyo autónomas (como radioaficionados en VHF/UHF y nodos LoRa / Meshtastic).

XiraVault nace para dotar a familias, brigadistas, comunidades y radioaficionados de una **herramienta de consulta inmediata** que no dependa de la nube ni de corporaciones tecnológicas centralizadas.

---

## 📁 Estructura Modular de los 6 Pilares Operativos

Tanto si se instala en una memoria USB como en un servidor local, la información se organiza rigurosamente en 6 carpetas principales para permitir una localización ultra rápida bajo presión:

```text
XiraVault/
├── 00_INMEDIATO/               # Primeras 24-48 horas de crisis
│   ├── medicina_emergencia/    # "Donde no hay doctor", guías de trauma táctico y primeros auxilios
│   ├── protocolos_colombia/    # Guías oficiales de la Defensa Civil y Cruz Roja Colombiana
│   └── checklists_supervivencia/ # Listados de acción rápida ante sismos y apagones
├── 01_COMUNICACIONES_Y_REDES/  # Radioaficionados y autonomía conectada
│   ├── manuales_radios/        # Manuales técnicos de equipos (Radtel, Quansheng, Baofeng)
│   ├── meshtastic_colombia/    # Configuración y despliegue de nodos LoRa de emergencia
│   └── directorio_repetidoras/ # Frecuencias VHF/UHF, tonos CTCSS y redes de apoyo (ASOREC)
├── 02_AGUA_ENERGIA_Y_REFUGIO/
│   ├── potabilizacion_agua/    # Métodos de purificación para agua de montaña tropical y lluvia
│   └── energia_solar_12v/      # Diagramas de paneles, reguladores, inversores y baterías
├── 03_ALIMENTACION_Y_LARGO_PLAZO/
│   ├── agrosavia_manuales/     # Agricultura urbana, huertas andinas y soberanía alimentaria (AGROSAVIA)
│   └── conservacion_alimentos/ # Técnicas tradicionales de conservación sin refrigeración
├── 04_MAPAS_Y_CARTOGRAFIA_OFF/
│   └── mbtiles_risaralda/      # Mapas vectoriales offline de OpenStreetMap para OsmAnd (Eje Cafetero / Colombia)
└── 05_SOFTWARE_Y_HERRAMIENTAS/
    ├── apks_lectores/          # Aplicaciones APK ligeras para lectura de PDF y ePub en móviles
    └── kiwix_wikipedia/        # Contenedor y base de datos comprimida ZIM de Wikipedia en español
```

---

## 🔌 Dos Formas de Implementación

### 1. Modo USB Universal (Plug & Play) — *Para cualquier persona y hogar*
* **Ideal para:** Llevar en el llavero, la maleta de evacuación o entregar a familiares y amigos sin perfiles técnicos.
* **Requisitos:** Una memoria USB de alta capacidad (64 GB o 128 GB), preferiblemente de diseño dual (USB-A y USB-C).
* **Instalación:** Formatea la unidad en formato `exFAT` (esencial para soportar archivos pesados como mapas o la Wikipedia offline) y copia la estructura de carpetas en la raíz.
* **Uso en terreno:** Conecta la USB a un teléfono inteligente mediante un adaptador OTG o a una laptop sin internet. Usa visores de PDF o la app Kiwix para navegar por todo el conocimiento acumulado de forma 100% offline.

### 2. Modo Servidor Local (Docker / Homelab) — *Para entusiastas y centros de operación*
* **Ideal para:** Hogares con mini-PCs (como equipos ThinkCentre Tiny o Raspberry Pi) conectados a una UPS o planta eléctrica, centros comunitarios o sedes de radioaficionados.
* **Requisitos:** Un equipo con Docker y Docker Compose instalados.
* **Despliegue rápido:**
  ```bash
  git clone https://github.com/tu-usuario/xiravault-colombia.git
  cd xiravault-colombia
  docker compose up -d
  ```
* **Acceso en red local:** Cualquier dispositivo conectado a la red Wi-Fi interna podrá consultar el portal web de documentos (Puerto `8080`) y el servidor de Wikipedia offline (Puerto `8081`) de forma simultánea.

---

## 🤝 ¿Cómo Contribuir al Proyecto?

XiraVault Colombia busca crecer gracias a la colaboración de la comunidad de preparacionistas, devs, educadores y radioaficionados en el país. Si tienes manuales valiosos, guías de campo adaptadas a Colombia, o mejoras en los scripts:
1. Haz un *Fork* de este repositorio.
2. Crea una rama con tu aporte (`git checkout -b feature/nuevo-manual-regional`).
3. Realiza el *Commit* (`git commit -m 'Adición de guía de potabilización rural para Eje Cafetero'`).
4. Sube los cambios (`git push origin feature/nuevo-manual-regional`).
5. Abre un *Pull Request*.

---

## 📄 Licencia

Este proyecto se distribuye bajo los términos de la **Licencia MIT**. Consulta el archivo `LICENSE` para más detalles.
