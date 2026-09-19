# Radio Inteligente Dispatch — LSPD / SARP.es

Descargas de **Radio Inteligente Dispatch LSPD** para Windows 10/11 de 64 bits.
El ZIP completo contiene Dispatch portable, WAV, voces en español e inglés, el motor de voz y WebView2 local.
No hace falta instalar Python ni iniciar sesión en GitHub para usarla.

## Descargar

[Ver versiones y descargar Dispatch](https://github.com/elchimeneas/radio-inteligente-dispatch-descargas/releases)

Las versiones de prueba se identifican como **beta / Pre-release**. No sustituyen una definitiva.

## Instalación paso a paso

1. Abre la versión que quieras descargar y despliega **Assets**.
2. Descarga **Radio-Inteligente-Dispatch-LSPD-SARP.es-<versión>.zip**: es el paquete completo para jugadores.
3. Si hay otra Radio Inteligente abierta, ciérrala desde **Salir** en su icono de la bandeja de iconos de Windows; puede estar dentro de la flecha de iconos ocultos.
4. Extrae la carpeta completa donde prefieras; **recomiendo el Escritorio**. No ejecutes el programa dentro del ZIP ni mezcles los archivos con una carpeta antigua.
5. Abre **rintel-lspd-dispatch.exe**. Conserva junto a él las carpetas `sonidos`, `voice`, `WebView2Runtime` y el resto del contenido extraído. Puedes crear un acceso directo al ejecutable.
6. Sigue el tutorial, configura tu indicativo y elige idioma, voz y volumen. Los ajustes se guardan automáticamente. La guía PDF y `LEEME.txt` incluidos explican todas las opciones.

## Qué es cada archivo de la descarga

`<versión>` identifica la entrega; `<hash>` es la huella que permite verificar el contenido del componente.

| Archivo en Assets | Qué contiene y para qué sirve | ¿Lo descargo manualmente? |
|---|---|---|
| `Radio-Inteligente-Dispatch-LSPD-SARP.es-<versión>.zip` | Aplicación completa, dependencias, WAV, voces, guía y licencias. | **Sí. Es el único ZIP necesario para instalar.** |
| `app-<hash>.zip` | Ejecutable, lógica de voz compilada, WAV, documentación y archivos de control de la versión. | No; lo gestiona el actualizador. No funciona solo. |
| `voice-runtime-<hash>.zip` | Intérprete y bibliotecas que necesita el motor de voz, licencias y herramienta de diagnóstico incluida. | No; lo gestiona el actualizador. |
| `voice-models-<hash>.zip` | Modelos y estilos de voz para las locuciones locales en español e inglés. | No; lo gestiona el actualizador. |
| `webview-<hash>.zip` | WebView2 local, necesario para mostrar la interfaz de Dispatch. | No; lo gestiona el actualizador. |
| `Source code (zip)` / `Source code (tar.gz)` | Archivos que GitHub genera automáticamente a partir de este repositorio de descargas: README y catálogos según la etiqueta. No contienen el proyecto privado ni una aplicación instalable. | No. |

No mezcles componentes ni los extraigas por separado sobre tu instalación: Dispatch selecciona los compatibles y comprueba su integridad.

## Qué ejecutable debo abrir

**Abre únicamente `rintel-lspd-dispatch.exe` para usar la radio.** Los demás binarios son dependencias incluidas:

| Binario o ubicación | Función |
|---|---|
| `rintel-lspd-dispatch.exe` | Aplicación principal: Central, avisos, voz, historial y ajustes. |
| `voice/runtime/python.exe` y `pythonw.exe` | Intérprete utilizado por el servicio local de voz. Las copias dentro de `Lib/venv` pertenecen también a Python. No debes abrirlos manualmente. |
| `WebView2Runtime/.../msedgewebview2.exe` | Runtime que muestra la interfaz. Los demás ejecutables de esa carpeta son auxiliares del runtime de Microsoft; no son pasos de instalación de Dispatch. |
| `tools/PresentMon/PresentMon-2.5.1-x64.exe` | Herramienta incluida para el diagnóstico de rendimiento opcional. Utiliza los controles de diagnóstico de la aplicación. |
| Archivos `.dll` y `voice/compiled/*.pyd` | Bibliotecas y módulos que carga la aplicación. No se ejecutan ni se instalan por separado. |

## Actualizar una instalación existente

- **Desde Dispatch:** entra en **Ajustes > Actualizaciones**, cierra GTA y sigue las opciones para descargar y actualizar/reiniciar. Solo se descargan los componentes que cambian. La búsqueda automática avisa de nuevas versiones, pero tú decides cuándo instalarlas.
- **Mediante ZIP:** utiliza **Salir** en la bandeja de iconos de Windows y extrae la carpeta nueva completa. Puedes borrar la anterior después de conservar cualquier archivo personal que hayas añadido dentro. Los ajustes e historiales se guardan por separado y se conservan. Si cambias de ubicación, actualiza los accesos directos y vuelve a aplicar **Iniciar con Windows**.
- Si tu versión aún no tiene actualizador, necesitas descargar el ZIP completo una primera vez.

## Guía y ayuda

La guía PDF incluida explica por separado los WAV, las locuciones recibidas y las respuestas propias: activar uno no activa los demás. También cubre configuración, rendimiento y solución de problemas.

Este repositorio se dedica a la distribución; no contiene el proyecto de desarrollo.
Los catálogos de actualización están firmados. No se suben registros de jugadores.
Incidencias: mensaje por Discord a **elchimeneas**, indicando edición y versión.
