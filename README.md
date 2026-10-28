# Tripulaciones Llaüt · CRCV

App Android del Club de Remo Ciudad de Valencia para cuadrar las tripulaciones de los llaüts de competición: se marca quién ha venido a la sesión y genera alineaciones alternativas respetando la banda de cada remero y equilibrando peso y experiencia. Cada llaüt lleva 8 remeros y puede salir con 6 o 7; si no hay gente para dos llaüts sale uno y el resto queda en reserva con cambios sugeridos.

## Descargar e instalar

Desde el móvil, abre este enlace y descarga el APK:

**https://github.com/jbromero-prog/tripulaciones-llaut/releases/latest/download/tripulaciones-llaut.apk**

1. Abre el archivo descargado. Android pedirá permiso para instalar apps desde el navegador: **Ajustes → Permitir de esta fuente**.
2. Si Play Protect avisa de que es una app desconocida: **Más detalles → Instalar de todos modos**.
3. Para actualizar, descarga el APK de nuevo e instálalo encima. Los datos se conservan.

Requiere Android 7 o superior.

## Plantilla de remeros

La app lee la hoja de Google *Plantilla Tripulaciones Llaüt* (carpeta Coordinacion Deportiva de administracion@removalencia.com). Tiene una pestaña por categoría (VF, ASM, ASF; se puede añadir VM) y la app asigna la categoría por el nombre de la pestaña. La pestaña Instrucciones debe seguir siendo la primera.

| Columna | Valores |
|---|---|
| Nombre | Nombre y apellido, único dentro de la pestaña |
| Banda | B (babor), E (estribor) o A (ambas) |
| Experiencia | 1 (iniciación) a 5 (experto) |
| Altura | cm; con ella se calcula la distancia tolete–bancada |
| Peso | kg |
| Patrón | sí / no |

### Reglaje tolete–bancada

Pestaña **Reglaje** con las columnas *Altura desde*, *Altura hasta* y *Tolete-bancada* (todo en cm), una fila por tramo de altura. La app muestra en cada plaza de la alineación la distancia que corresponde a la altura del remero. Si un remero necesita un valor propio, se añade la columna *Tolete-bancada* en su pestaña de categoría y ese valor tiene prioridad sobre la tabla.

Un remero que esté en dos categorías aparece en las dos pestañas con el mismo nombre; la app lo une en una sola ficha.

La hoja debe estar compartida como «Cualquier persona con el enlace · Lector». La app la descarga al abrirse y con el botón Actualizar; sin conexión usa la última copia.

## Cómo se compila

Cada cambio en `main` lanza el flujo de GitHub Actions, que compila el APK firmado y lo publica en *Releases*. El código de la app está en `app/src/main/assets/index.html`; `MainActivity.java` solo aloja la página y da acceso a red, compartir y portapapeles.
