<p align="center">
  <img src="banner.svg" alt="Antonio Baeza — Ingeniero en Sistemas Computacionales · Fundador de Delta Labs" width="100%">
</p>

<p align="center">
  <a href="https://devlta.com"><img src="https://img.shields.io/badge/Delta_Labs-devlta.com-5b56f0?style=for-the-badge" alt="Delta Labs"></a>
  <a href="mailto:contacto@devlta.com"><img src="https://img.shields.io/badge/contacto-devlta.com-1e2129?style=for-the-badge&logo=maildotru&logoColor=white" alt="Correo"></a>
  <a href="https://github.com/Anton-Bazh/MARC-DOC"><img src="https://img.shields.io/badge/MARC-documentación_abierta-22c55e?style=for-the-badge&logo=markdown&logoColor=white" alt="MARC-DOC"></a>
</p>

**Español** · [English](#english)

## Quién soy

Soy ingeniero en Sistemas Computacionales por el Tecnológico Nacional de México y fundador de **Delta Labs**, donde diseño y construyo software propio de principio a fin: el núcleo, las aplicaciones de escritorio y móviles, la documentación técnica y la publicación en tiendas. Me interesan los sistemas que funcionan sin conexión, respetan los datos de quien los usa y se pueden mantener durante años.

Trabajo con una regla sencilla: cada producto tiene un núcleo compartido escrito una sola vez, interfaces nativas en cada plataforma y documentación de ingeniería que describe cómo está construido hoy, verificada contra el código.

## Lo que construyo

El siguiente diagrama muestra cómo se relacionan los proyectos actuales. MARC define el formato de documentación que usan todos los demás, y los productos de Delta Labs comparten la misma forma de trabajar: núcleo nativo con frontera bien definida e interfaz en Kotlin.

```mermaid
flowchart LR
    subgraph DL["Delta Labs"]
        MARC["MARC<br/>documentación Markdown"]
        OCE["Ocelot<br/>lectura"]
        XOLO["Xolo<br/>escáner y PDF"]
    end
    LASID["LASID<br/>CENIDET"]
    FMT[("Formato abierto<br/>.marc")]
    MARC --> FMT
    OCE -->|"lee y exporta"| FMT
    MARC -.->|"documenta"| OCE & XOLO & LASID
    classDef marc fill:#5b56f0,color:#fff,stroke:none
    classDef oce fill:#22c55e,color:#0b1a10,stroke:none
    classDef xolo fill:#f59e0b,color:#1a1205,stroke:none
    classDef lasid fill:#ec4899,color:#fff,stroke:none
    class MARC marc
    class OCE oce
    class XOLO xolo
    class LASID lasid
```

| Proyecto | Qué es | Tecnología |
|:--|:--|:--|
| **MARC** | Editor y visor de documentación Markdown con diagramas, fórmulas, gráficas e interacción, para escritorio y Android, con exportación a PDF y Word. Su formato `.marc` es abierto ([especificación](https://github.com/Anton-Bazh/MARC-FORMATO)) y su documentación de uso es pública ([MARC-DOC](https://github.com/Anton-Bazh/MARC-DOC)). | Rust, Kotlin Multiplatform, Compose, Typst |
| **Ocelot** | Aplicación de lectura para Android: libros, cómics, manga, webtoons y revistas en una sola biblioteca, con lectura en voz alta. | Rust (31 motores de formato), UniFFI, Jetpack Compose, SQLite |
| **Xolo** | Escáner de documentos y suite PDF para Android que trabaja por completo en el teléfono, sin permiso de red. | C++17 (motor Eagle), OpenCV, Kotlin hexagonal, Jetpack Compose |
| **LASID** | Laboratorio virtual de sistemas dinámicos e inteligencia artificial, desarrollado como residencia en CENIDET. | Next.js, React, Prisma, PostgreSQL |

> Los repositorios de código son privados; MARC-DOC, MARC-FORMATO y MARC-DOC-TRADUCCIONES son públicos.

## Herramientas

<p>
  <img src="https://img.shields.io/badge/Rust-1e2129?style=flat-square&logo=rust&logoColor=white" alt="Rust">
  <img src="https://img.shields.io/badge/Kotlin-1e2129?style=flat-square&logo=kotlin&logoColor=7F52FF" alt="Kotlin">
  <img src="https://img.shields.io/badge/Jetpack_Compose-1e2129?style=flat-square&logo=jetpackcompose&logoColor=4285F4" alt="Jetpack Compose">
  <img src="https://img.shields.io/badge/C++-1e2129?style=flat-square&logo=cplusplus&logoColor=00599C" alt="C++">
  <img src="https://img.shields.io/badge/TypeScript-1e2129?style=flat-square&logo=typescript&logoColor=3178C6" alt="TypeScript">
  <img src="https://img.shields.io/badge/Python-1e2129?style=flat-square&logo=python&logoColor=3776AB" alt="Python">
  <img src="https://img.shields.io/badge/Next.js-1e2129?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js">
  <img src="https://img.shields.io/badge/FastAPI-1e2129?style=flat-square&logo=fastapi&logoColor=009688" alt="FastAPI">
  <img src="https://img.shields.io/badge/PostgreSQL-1e2129?style=flat-square&logo=postgresql&logoColor=4169E1" alt="PostgreSQL">
  <img src="https://img.shields.io/badge/SQLite-1e2129?style=flat-square&logo=sqlite&logoColor=0F80CC" alt="SQLite">
  <img src="https://img.shields.io/badge/Android-1e2129?style=flat-square&logo=android&logoColor=34A853" alt="Android">
  <img src="https://img.shields.io/badge/Linux-1e2129?style=flat-square&logo=linux&logoColor=FCC624" alt="Linux">
  <img src="https://img.shields.io/badge/Docker-1e2129?style=flat-square&logo=docker&logoColor=2496ED" alt="Docker">
  <img src="https://img.shields.io/badge/Cloudflare-1e2129?style=flat-square&logo=cloudflare&logoColor=F38020" alt="Cloudflare">
</p>

## Cómo trabajo

1. **Núcleo una vez, interfaz nativa en cada plataforma.** La lógica vive en Rust o C++ y se expone con una frontera explícita (UniFFI, JNI); la interfaz se escribe para la plataforma.
2. **Sin conexión por defecto.** Los datos se quedan en el dispositivo salvo que la función exija lo contrario.
3. **Documentación como parte del producto.** Cada proyecto tiene su repositorio de ingeniería (sistema, pendientes y procesos), escrito en presente y verificado contra el código.
4. **Publicar es parte del trabajo.** Firma, cumplimiento y fichas de Google Play y Huawei AppGallery se tratan con el mismo cuidado que el código.

## Contacto

Escríbeme a [contacto@devlta.com](mailto:contacto@devlta.com) o visita [devlta.com](https://devlta.com).

---

<a id="english"></a>

## English

I am a Computer Systems Engineer (Tecnológico Nacional de México) and the founder of **Delta Labs**, where I design and build our own software end to end: native cores, desktop and mobile apps, engineering documentation and store releases. I care about software that works offline, respects its users' data and can be maintained for years.

| Project | What it is | Stack |
|:--|:--|:--|
| **MARC** | Markdown documentation editor and viewer for desktop and Android, with diagrams, math, charts and PDF/Word export. Open `.marc` format ([spec](https://github.com/Anton-Bazh/MARC-FORMATO)), public user docs ([MARC-DOC](https://github.com/Anton-Bazh/MARC-DOC)). | Rust, Kotlin Multiplatform, Compose, Typst |
| **Ocelot** | Android reading app: books, comics, manga, webtoons and magazines in one library, with read-aloud. | Rust (31 format engines), UniFFI, Jetpack Compose, SQLite |
| **Xolo** | Offline document scanner and PDF suite for Android, with no network permission. | C++17 (Eagle engine), OpenCV, hexagonal Kotlin, Jetpack Compose |
| **LASID** | Virtual lab for dynamical systems and AI, built during my residency at CENIDET. | Next.js, React, Prisma, PostgreSQL |

How I work: one shared native core, native UI per platform, offline by default, and engineering docs that describe the system as it is today.

Reach me at [contacto@devlta.com](mailto:contacto@devlta.com) · [devlta.com](https://devlta.com)
