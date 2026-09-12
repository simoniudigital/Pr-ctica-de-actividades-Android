# Evidencia de Aprendizaje 2 — Actividades Android

**Estudiante:** Simón Arbey Castaño Ríos
**Programa:** Ingeniería de Software — IU Digital de Antioquia
**Curso:** Programación de Dispositivos Móviles — Grupo PREICA2602B010101
**Tutor:** Juan Esteban Acevedo
**Aplicación:** NotaExpress

---

## Contenido de esta carpeta

| Archivo / carpeta | Descripción |
|---|---|
| `Evidencia_Aprendizaje_2_Actividades_Android_Simon_Castano.pdf` | Documento de entrega listo para subir. |
| `Evidencia_Aprendizaje_2_Actividades_Android_Simon_Castano.docx` | El mismo documento en Word, por si hay que editarlo. |
| `NotaExpress/` | Proyecto Android completo (código fuente). |
| `capturas/` | Capturas de pantalla originales usadas como evidencia. |
| `capturas/recortes/` | Las capturas del emulador recortadas para el documento. |

---

## La aplicación

NotaExpress tiene dos pantallas:

1. **MainActivity** — se escribe una nota y se pulsa *Enviar a Activity2*.
   Si el campo está vacío, muestra un error y no navega.
2. **Activity2** — muestra la nota recibida y ofrece dos botones:
   *Marcar como recibido* y *Cancelar la nota*.

Al volver, MainActivity muestra en un `TextView` el estado **recibido** o
**cancelado**, con icono y color según el caso. Si se regresa con el botón de
retroceso sin elegir ninguna opción, se indica *sin respuesta*.

### Aspectos técnicos

- Java, `AppCompatActivity` y Material Design 3.
- Comunicación entre pantallas con `Intent` explícito y *extras*.
- Retorno del resultado con la **API de resultados de AndroidX**
  (`registerForActivityResult`), no con el obsoleto `startActivityForResult`.
- `ConstraintLayout` dentro de `ScrollView` en ambas pantallas.
- `View Binding` en lugar de `findViewById`.

---

## Cómo compilar y ejecutar

### Requisitos

- Android Studio (probado con la versión 2026.1.4.7).
- JDK 17. El proyecto apunta a él desde `gradle.properties` con la propiedad
  `org.gradle.java.home`. **Si cambias de equipo, ajusta esa ruta.**
- SDK de Android con la plataforma API 35 y un emulador o dispositivo con
  API 24 o superior.

### Desde Android Studio

1. Abrir la carpeta `NotaExpress/`.
2. Esperar a que termine la sincronización de Gradle.
3. Elegir un dispositivo y pulsar *Run*.

### Desde la línea de comandos

```bash
cd NotaExpress
./gradlew installDebug
```

> El archivo `local.properties` contiene la ruta del SDK de este equipo y por
> eso no se versiona. Si el proyecto se abre en otra máquina, Android Studio lo
> vuelve a generar automáticamente.

---

## Dispositivo virtual utilizado

- **Nombre:** `Pixel7_API36_NotaExpress`
- **Perfil:** Pixel 7 — 1080 × 2400 px, densidad 420 dpi
- **Imagen:** Android 16 (API 36), x86_64
- **Aceleración:** WHPX (Plataforma de Hipervisor de Windows)
