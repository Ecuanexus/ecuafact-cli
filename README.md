# Ecuafact CLI

`ecuafact` es la línea de comandos oficial de Ecuafact para la facturación electrónica del SRI (Ecuador): emite comprobantes desde JSON, JSONL, carpetas, CSV o Excel; los valida sin consumir cupo; sigue su autorización; descarga el RIDE y el XML; consulta el SRI y vigila carpetas para emitir lo que deja tu ERP.

> [!IMPORTANT]
> Versión preliminar (`preview`): puede cambiar sin aviso. Pruébala primero en el entorno `sandbox`.

Este repositorio solo publica las versiones descargables. La documentación completa del CLI está en <https://docsapi.ecuafact.com/v1/guias/cli>.

## Instalación

| Sistema | Comando |
|---|---|
| Cualquiera con Node.js 18+ | `npm install -g @ecuafact/cli@preview` |
| Sin instalar (Node.js o Bun) | `npx @ecuafact/cli@preview --help` o `bunx @ecuafact/cli@preview --help` |
| Windows (Scoop) | `scoop bucket add ecuafact https://github.com/Ecuanexus/ecuafact-scoop` y `scoop install ecuafact/ecuafact-preview` |
| macOS y Linux (Homebrew) | `brew install ecuanexus/ecuafact/ecuafact-preview` |
| Descarga directa | El `.zip` (Windows) o `.tar.gz` (Linux y macOS) de la sección **Releases**; verifica el archivo con `SHA256SUMS`. |

## Primeros pasos

```bash
ecuafact --entorno sandbox login     # pide tu API Key sin mostrarla y la guarda en el almacén de credenciales del sistema
ecuafact --entorno sandbox doctor    # revisa conexión, API Key, IP registrada y cupo
ecuafact ayuda inicio
ecuafact <comando> --help
```

Tu API Key solo funciona desde una IP registrada en el portal (**Cuenta > IP permitidas**).

## Soporte

Abre un caso desde el portal de clientes indicando la salida de `ecuafact --version` y `ecuafact doctor`.
