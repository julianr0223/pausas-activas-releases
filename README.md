# Pausas Activas — releases

Repo **público** que solo distribuye los **instaladores** y el **manifiesto de
actualización** (`latest.json`) de la app Pausas Activas.

El **código fuente es privado** (`julianr0223/pausas-activas`). Acá no hay
código: el workflow de [`.github/workflows/release.yml`](.github/workflows/release.yml)
clona el repo privado con un token de solo lectura, compila el cliente y publica
los instaladores en los **Releases** de este repo.

¿Por qué un repo aparte? Para que el **auto-update** del cliente pueda descargar
los binarios sin autenticación, sin tener que exponer el código. Los binarios no
contienen secretos (la URL y el token del coordinador se configuran en la app;
la clave de firma vive solo en los secrets del CI).

## Instalar

Descargá el instalador de la última [release](../../releases/latest):

- **Linux**: `.AppImage` (recomendado, con auto-update) o `.deb`.
- **macOS**: `.dmg` (universal, Intel + Apple Silicon).
