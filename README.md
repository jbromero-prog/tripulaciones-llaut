# Tripulaciones Llaüt · CRCV

App Android del Club de Remo Ciudad de Valencia para cuadrar las tripulaciones de los llaüts de competición: se marca quién ha venido a la sesión y genera alineaciones alternativas respetando la banda de cada remero y equilibrando peso, altura y experiencia.

## Descargar e instalar

Desde el móvil, abre este enlace y descarga el APK:

**https://github.com/jbromero-prog/tripulaciones-llaut/releases/latest/download/tripulaciones-llaut.apk**

1. Abre el archivo descargado. Android pedirá permiso para instalar apps desde el navegador: **Ajustes → Permitir de esta fuente**.
2. Si Play Protect avisa de que es una app desconocida: **Más detalles → Instalar de todos modos**.
3. Para actualizar, descarga el APK de nuevo e instálalo encima. Los datos se conservan.

Requiere Android 7 o superior.

## Plantilla de remeros

La app lee la hoja de Google *Plantilla Tripulaciones Llaüt* (carpeta Coordinacion Deportiva de administracion@removalencia.com). Columnas:

| Columna | Valores |
|---|---|
| Nombre | Nombre y apellido, único |
| Banda | B (babor), E (estribor) o A (ambas) |
| Experiencia | 1 (iniciación) a 5 (experto) |
| Altura | cm |
| Peso | kg |
| Equipo | VM, VF, ASM o ASF |
| Patrón | sí / no |

La hoja debe estar compartida como «Cualquier persona con el enlace · Lector». La app la descarga al abrirse y con el botón Actualizar; sin conexión usa la última copia.

## Cómo se compila

Cada cambio en `main` lanza el flujo de GitHub Actions, que compila el APK firmado y lo publica en *Releases*. El código de la app está en `app/src/main/assets/index.html`; `MainActivity.java` solo aloja la página y da acceso a red, compartir y portapapeles.
