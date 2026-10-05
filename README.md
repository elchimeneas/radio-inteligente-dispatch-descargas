# Radio Inteligente Dispatch · SARP.es

Descargas de **Dispatch LSPD y Dispatch LSSD** para Windows 10 y 11 de 64 bits. Son aplicaciones separadas, con códigos, emblemas, configuración y catálogo de actualización propios.

| Edición | Publicación | Paquete completo que debes descargar |
|---|---|---|
| **LSPD** | [1.2.5 definitiva](https://github.com/elchimeneas/radio-inteligente-dispatch-descargas/releases/tag/v1.2.5) | `Radio-Inteligente-Dispatch-LSPD-SARP.es-1.2.5.zip` |
| **LSSD** | [1.2.5 definitiva](https://github.com/elchimeneas/radio-inteligente-dispatch-descargas/releases/tag/lssd-v1.2.5) | `Radio-Inteligente-Dispatch-LSSD-SARP.es-1.2.5.zip` |

La 1.2.5 permite apagar un aviso completo desde su casilla: WAV, locución recibida y respuesta propia. Volver a marcarlo recupera la selección anterior, incluso tras reiniciar. En **Configurar** puedes seguir ajustando cada control por separado. La lista muestra qué está activado y las guías explican el nuevo comportamiento. Se conservan tus preferencias y los modos Dinámico y Ligero.

Las versiones de esta tabla pueden no ser las últimas: consulta [Releases](https://github.com/elchimeneas/radio-inteligente-dispatch-descargas/releases) y **Ajustes > Actualizaciones**. El distintivo Latest puede corresponder a otra agencia; comprueba siempre LSPD o LSSD en el nombre.

## Original o Dispatch

La [Radio Inteligente original](https://github.com/elchimeneas/radio-inteligente-descargas/releases) utiliza grabaciones WAV y consume menos recursos. Dispatch añade **locuciones locales en español e inglés**, con indicativos completos, contexto y ubicaciones reconocidas en el chat. Incluye las funciones de radio, mensajes, 911, panel y sesiones.

**Dispatch consume más CPU y memoria y no está pensada para todos los equipos.** Prueba una patrulla, selecciona calidad Ahorro si es necesario y vuelve a la original si afecta al juego. No hay un requisito de rendimiento validado para todos los ordenadores.

## Instalación

1. Abre la publicación de tu agencia y despliega **Assets**.
2. Descarga el **ZIP completo** de la tabla. No descargues `app-…`, `voice-runtime-…`, `voice-models-…` o `webview-…` para instalar manualmente.
3. Cierra cualquier otra radio mediante **Salir**, desde la bandeja de iconos de Windows; el icono puede estar dentro de la flecha de iconos ocultos.
4. Extrae toda la carpeta donde quieras; **recomiendo el Escritorio**. No ejecutes desde dentro del ZIP ni mezcles carpetas de ediciones o versiones.
5. Abre **rintel-lspd-dispatch.exe** para LSPD o **rintel-lssd-dispatch.exe** para LSSD. Conserva todas las carpetas incluidas junto al ejecutable.
6. Sigue el tutorial y configura tu indicativo, idioma, voz y volumen. Los cambios se guardan automáticamente. El ZIP incluye `LEEME.txt`, guía PDF, changelog y licencias.

No necesitas instalar Python ni WebView2 por separado, ni iniciar sesión en GitHub para descargar. La voz se genera en el equipo; Internet se utiliza para buscar o descargar actualizaciones. Solo puede estar activa una Radio Inteligente a la vez.

## WAV, locuciones y respuestas

En **Avisos > Configurar** hay tres ajustes independientes por aviso: grabación WAV, locución recibida y respuesta a tus propios mensajes. Desactivar el WAV no desactiva la voz. Con WAV y locución recibida activos, la voz ocupa el aviso y el WAV queda como respaldo. Las respuestas propias empiezan desactivadas.

LSSD utiliza los códigos de su manual, SCC, ayudantes, apoyo de rutina y asistencia urgente; acepta `10-15` o `'15`, y su canal RJ es **RJ SHERIFF**. LSPD mantiene sus propias reglas y **RJ POLICE**. Las preferencias de una agencia no convierten una aplicación en la otra.

## Avisos repetidos

Como máximo se admiten dos avisos del mismo tipo en diez segundos, contando WAV y voz juntos, incluidas radio y menciones. Los sobrantes no se reproducen después; las comunicaciones siguen registrándose. Cada tipo tiene su contador y se mantiene el máximo conjunto de dos sonidos al volver de la pausa.

## Actualización

- Desde la aplicación: **Ajustes > Actualizaciones**, con GTA cerrado. La búsqueda automática puede avisarte, pero tú decides descargar e instalar. Los catálogos están firmados y cada edición recibe únicamente sus actualizaciones.
- Mediante ZIP: primero **Salir** desde la bandeja. Extrae la carpeta nueva completa. Puedes borrar la anterior tras conservar los archivos personales que hayas añadido dentro. Los ajustes e historiales de esa edición permanecen en su carpeta de datos. Si cambia la ruta, corrige accesos directos y vuelve a aplicar Iniciar con Windows.
- Pasar de la original a Dispatch es una **instalación separada**, no una actualización automática. LSSD no importa automáticamente tus ajustes de otras ediciones.

## Qué es cada archivo de descarga

Desde 1.2.1, cada publicación para jugadores contiene solo su ZIP completo como archivo adjunto. Los componentes del actualizador se guardan en publicaciones «Componentes del actualizador» separadas; no necesitas abrirlas. Los componentes antiguos se conservan donde estaban para que sigan funcionando los catálogos anteriores. GitHub añade automáticamente «Source code»; esos archivos no son la aplicación.

| Archivo | Para qué sirve |
|---|---|
| `Radio-Inteligente-Dispatch-<LSPD o LSSD>-SARP.es-<versión>.zip` | **Paquete completo para jugadores. Es el único ZIP necesario para instalar.** |
| `app-<hash>.zip` | Ejecutable, lógica de voz compilada, WAV y documentación. Lo gestiona el actualizador; no funciona por separado. |
| `voice-runtime-<hash>.zip` | Intérprete, bibliotecas, licencias y diagnóstico del motor de voz. Lo gestiona el actualizador. |
| `voice-models-<hash>.zip` | Modelos y estilos de voz locales. Lo gestiona el actualizador. |
| `webview-<hash>.zip` | Interfaz WebView2 local. Lo gestiona el actualizador. |
| `Source code (zip/tar.gz)` | Archivos automáticos de GitHub con este repositorio de descargas. No contienen el proyecto privado ni la aplicación instalable. |

`<hash>` es la huella que verifica el contenido. No mezcles componentes manualmente.

## Qué ejecutable abrir

| Archivo dentro de la carpeta | Función |
|---|---|
| `rintel-lspd-dispatch.exe` / `rintel-lssd-dispatch.exe` | **Aplicación principal de la agencia elegida.** |
| `voice/runtime/python.exe`, `pythonw.exe` y copias de `Lib/venv` | Dependencias del servicio local de voz. No las abras manualmente. |
| `WebView2Runtime/.../msedgewebview2.exe` y auxiliares | Interfaz de Microsoft incluida. No son instaladores que deba abrir el jugador. |
| `tools/PresentMon/PresentMon-2.5.1-x64.exe` | Diagnóstico opcional, gestionado desde la aplicación. |
| `.dll`, `voice/compiled/*.pyd` | Bibliotecas y módulos; no se ejecutan ni instalan por separado. |
| `ARCHIVOS.sha256` | Inventario para comprobar la integridad; no se ejecuta. |

## Incidencias

Envía un mensaje por **Discord a elchimeneas** con edición, versión, pasos y resultado. Para un fallo de detección o audio, incluye el mensaje completo y tus ajustes de WAV/voz. Puedes utilizar `REPORTAR_INCIDENCIA.txt`; no hace falta enviar toda la carpeta ni el historial completo.

Este repositorio contiene descargas, documentación y catálogos. El proyecto de desarrollo se conserva privado. No se suben registros de jugadores automáticamente.
