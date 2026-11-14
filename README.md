# Ecuafact CLI

CLI de Ecuafact para la facturación electrónica del SRI de Ecuador. Desde la terminal o desde un script, crea un comprobante de ejemplo, lo valida, lo emite, espera el resultado del SRI y descarga el RIDE y el XML.

Qué incluye:

- Emisión desde archivos JSON o XML del SRI, desde carpetas, y desde CSV o Excel con una plantilla de mapeo.
- `vigilar`: observa una carpeta donde tu ERP deja los comprobantes y los emite.
- Lista de operaciones, consulta de tu cuenta, tu cupo y el perfil del emisor.
- Consultas al SRI, estado del servicio (`ecuafact estado-servicio`) y catálogos (`ecuafact catalogos`).
- Administración y prueba de tus destinos de webhooks.
- `doctor`: diagnostica tu conexión.
- Entornos `sandbox` y `produccion`, o uno propio con la URL de tu servidor. La API Key se guarda sin mostrarla o se lee de `ECUAFACT_API_KEY`, y en producción pide confirmar las operaciones que emiten o cambian datos.
- Binarios para Windows, Linux y macOS.

```bash
npm install -g @ecuafact/cli
```

También con Scoop (`scoop bucket add ecuafact https://github.com/Ecuanexus/ecuafact-scoop` y `scoop install ecuafact/ecuafact`) o Homebrew (`brew install ecuanexus/ecuafact/ecuafact`).

Documentación: https://docsapi.ecuafact.com/v1/guias/cli

El tipo del comprobante (`01` a `07`) elige la ruta de emisión y no viaja en el cuerpo. Indícalo con `--tipo`; si no lo indicas, el CLI lo deduce de la forma del comprobante. Los archivos `.xml` del SRI se envían tal cual y su tipo sale de la raíz del XML.
