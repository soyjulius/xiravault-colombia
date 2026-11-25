<p align="center">
  <img src="https://xirafa.soyjuli.us/assets/logo.webp" alt="Proyecto XIRAFA Logo" width="120" />
</p>
<p align="center">
  <strong>Este proyecto forma parte de la iniciativa del <a href="https://xirafa.soyjuli.us" target="_blank">Proyecto XIRAFA</a>.</strong>
</p>
# 🇨🇴 XiraVault Colombia
 
### Biblioteca de emergencia offline en una memoria USB
 
> **"Que no pase nada, hasta que pasa."**
 
<p align="center">
  <img src="https://img.shields.io/badge/Estado-En_construcción_(v0.x)-orange?style=for-the-badge" alt="Estado: en construcción" />
  <img src="https://img.shields.io/badge/Open_Source-100%25-green?style=for-the-badge" alt="Open Source" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License MIT" />
</p>
---
 
## 🔍 ¿Qué es XiraVault?
 
XiraVault es un proyecto de código abierto que responde a una pregunta:
 
**¿Qué necesita saber una familia cuando se va la luz, se cae internet y no hay señal celular?**
 
La respuesta es una **memoria USB dedicada** con información confiable sobre primeros auxilios, agua, energía, alimentos, comunicaciones y protocolos de emergencia. Se consulta en cualquier computador o celular, sin internet y sin instalar nada.
 
Lo valioso no es la USB, sino la **curaduría**: documentos revisados, con fuente conocida y organizados para encontrarlos rápido, incluso bajo estrés.
 
---
 
## 🚧 Estado del proyecto
 
**XiraVault está en fase de diseño y construcción (versiones 0.x).** Todavía no hay una versión funcional para el público.
 
La prioridad es construir una primera prueba que funcione de punta a punta. La comunidad y las donaciones se abrirán cuando exista esa prueba funcional.
 
---
 
## 👥 ¿Para quién es?
 
XiraVault distingue dos roles:
 
| Rol | Quién es | Qué hace |
| --- | --- | --- |
| **Preparador** | Alguien con algo de conocimiento técnico | Usa la app de Windows para crear y actualizar la USB |
| **Usuario** | Cualquier persona de la familia o la comunidad, sin conocimientos técnicos | Conecta la USB y consulta la información en una emergencia |
 
Lo técnico es para el preparador. Lo que hay dentro de la USB debe ser simple para cualquiera.
 
---
 
## 🌎 ¿Solo Colombia?
 
El contenido se organiza en dos niveles:
 
- **Núcleo común:** información que sirve en cualquier país de habla hispana (primeros auxilios, agua, energía, alimentos).
- **Paquete por país:** lo propio de cada país (líneas de emergencia, entidades oficiales, normas de radioafición, mapas y riesgos).
El proyecto comienza con **Colombia**. Está diseñado para que más adelante otros países agreguen su propio paquete.
 
---
 
## ⚙️ ¿Cómo funciona?
 
El sistema tiene cuatro piezas:
 
```text
 ┌────────────────────┐      publica      ┌─────────────────────┐
 │  Panel web         │ ───────────────▶  │  Catálogo público   │
 │  (curaduría)       │                   │  (fichas, paquetes, │
 │  solo el curador   │                   │   manifiestos)      │
 └────────────────────┘                   └──────────┬──────────┘
                                                     │ consulta y descarga
                                                     ▼
                                          ┌─────────────────────┐
                                          │  Sincronizador      │
                                          │  (app de Windows)   │
                                          └──────────┬──────────┘
                                                     │ copia lo que falta
                                                     ▼
                                          ┌─────────────────────┐
                                          │  USB XiraVault      │
                                          │  consulta offline   │
                                          └─────────────────────┘
```
 
1. **Panel web de curaduría:** donde se suben los documentos, se completa la ficha de cada uno (fuente, entidad, licencia, permiso), se extrae su texto para la búsqueda y se organizan en paquetes.
2. **Catálogo público:** el panel publica las fichas y los paquetes con su versión. El panel y el sincronizador nunca se comunican directamente: uno publica y el otro lee lo publicado.
3. **Sincronizador (app de Windows):** detecta la USB, muestra los paquetes disponibles y descarga solo lo que falta o cambió.
4. **USB XiraVault:** queda lista para consultar sin internet.
### Paquetes y sincronización
 
Cada categoría o país es un **paquete con versión**, por ejemplo *Primeros auxilios v3* o *Colombia v5*. La persona elige qué paquetes sincronizar.
 
Cuando vuelve a conectar la USB, la app compara lo instalado con el catálogo, muestra las novedades y descarga solo lo nuevo, con un clic por paquete.
 
### La USB
 
- **Dedicada 100 % a XiraVault**, de **mínimo 32 GB**.
- La app la prepara y la administra completa.
- Contiene solo **información pública e informativa**: no guarda documentos personales ni datos sensibles.
### Consulta en tres niveles
 
Para no depender de una sola tecnología:
 
| Nivel | Dónde funciona | Cómo |
| --- | --- | --- |
| **Básico** | Cualquier equipo | Carpetas y archivos con nombres claros, abiertos con el explorador de archivos |
| **Computador** | Windows, Mac, Linux | `index.html` con buscador, abierto con doble clic, sin instalar nada |
| **Celular** | Android, iPhone | [Kiwix](https://kiwix.org), lector offline de código abierto con búsqueda (en evaluación) |
 
### Búsqueda
 
El texto de cada documento se extrae y se indexa en el servidor, no en el equipo de cada persona. El índice viaja dentro de cada paquete, de modo que el buscador de la USB encuentra los documentos que hablan de un tema, incluso dentro de los PDF.
 
---
 
## ⚖️ Contenido y derechos de autor
 
**Este repositorio no almacena documentos de terceros.** Contiene el código del proyecto y, más adelante, contenido escrito por la comunidad con licencia libre.
 
Cada documento del catálogo tiene una **ficha** con su fuente, entidad autora, licencia y estado de permiso. Según ese estado, el documento llega a la USB de una de tres formas:
 
| Tipo de documento | Cómo se distribuye |
| --- | --- |
| **Libre** (Creative Commons, dominio público) | Desde el servidor de XiraVault |
| **Con permiso** de la entidad autora | Desde el servidor de XiraVault, con la autorización registrada |
| **Sin permiso de redistribución** | El sincronizador lo descarga directamente desde el sitio oficial |
 
Los documentos sin fuente verificada no se publican.
 
---
 
## 🔒 Confianza y seguridad
 
XiraVault es una herramienta para emergencias, así que la confianza es parte del diseño:
 
- **Código abierto y verificable:** cualquiera puede revisar qué hace cada pieza.
- **Ejecutables compilados de forma automática** desde el código público.
- **Contenido firmado:** cada paquete lleva una firma digital y cada archivo su huella (hash). El sincronizador rechaza lo que haya sido alterado.
- **Ejecutable de Windows firmado**, para evitar advertencias de seguridad.
- **Privacidad total:** sin cuentas, sin rastreo y sin pedir permisos de administrador.
- **Trazabilidad:** cada documento muestra su fuente, licencia, fecha de verificación y quién lo revisó.
---
 
## 🗺️ Hoja de ruta
 
| Versión | Meta |
| --- | --- |
| **v0.1** | Panel web de curaduría para crear el catálogo inicial de documentos |
| **v0.2** | El panel publica paquetes y el catálogo público |
| **v0.3** | Primer sincronizador que lleva un paquete a la USB |
| **v0.4** | `index.html` con búsqueda dentro de la USB |
| **v0.5+** | Kiwix para celular, firma de contenido y ajustes tras pruebas reales |
| **v1.0** | Ciclo completo funcionando: preparar una USB real y entregarla |
 
### v0.1: panel web de curaduría
 
La primera versión tiene una sola meta: **convertir una colección de PDF y ebooks en un catálogo confiable.**
 
- **Tablero:** documentos por estado y por paquete.
- **Carga masiva:** detección de duplicados, extracción de texto, páginas, miniatura y metadatos, y OCR para PDF escaneados.
- **Biblioteca:** listado con filtros y búsqueda dentro del texto.
- **Ficha:** vista previa del documento junto al formulario de datos.
- **Entidades:** fuentes como Cruz Roja o UNGRD, con su contacto y su permiso.
- **Paquetes y categorías:** núcleo común, Colombia y sus categorías.
Ciclo de vida de un documento:
 
```text
sin fuente → por verificar → listo → publicado → retirado
```
 
Estados de permiso: `libre` · `pendiente` · `solicitado` · `aprobado` · `rechazado` · `solo enlace`.
 
**Tecnología prevista:** Django (Python), PostgreSQL y Redis para el procesamiento en segundo plano, desplegados con Docker. El almacenamiento de archivos se separa en una zona privada (archivo de trabajo) y una pública (solo contenido publicable).
 
---
 
## 🤝 Contribuir
 
Por ahora el proyecto está enfocado en lograr una primera prueba funcional. **Cuando exista, todos serán bienvenidos**: desarrolladores, educadores, brigadistas, personal de salud, radioaficionados y comunidades de otros países que quieran crear su propio paquete.
 
Mientras tanto, puedes seguir el avance en este repositorio y en el [Proyecto XIRAFA](https://xirafa.soyjuli.us).
 
---
 
## 📄 Licencia
 
El código de este proyecto se distribuye bajo la **Licencia MIT**. Consulta el archivo `LICENSE` para más detalles.
 
Cada documento del catálogo conserva la licencia 
