# TableDesk · Descargas

Cliente de bases de datos de escritorio para PostgreSQL, MySQL/MariaDB, SQLite, SQL Server, Redis y MongoDB.

Versión actual: **v0.1.2** · [Todas las versiones](https://github.com/jpdealba/tabledesk-downloads/releases)

## Descargar

| Sistema | Descarga |
|---|---|
| **Windows 10/11** (recomendado) | [TableDesk-windows-setup.exe](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-windows-setup.exe) |
| Windows (instalador MSI) | [TableDesk-windows.msi](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-windows.msi) |
| **macOS** con chip Apple (M1, M2, M3, M4…) | [TableDesk-macos-apple-silicon.dmg](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-macos-apple-silicon.dmg) |
| macOS con procesador Intel | [TableDesk-macos-intel.dmg](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-macos-intel.dmg) |
| **Linux** (cualquier distribución) | [TableDesk-linux.AppImage](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-linux.AppImage) |
| Linux Debian / Ubuntu | [TableDesk-linux.deb](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-linux.deb) |
| Linux Fedora / openSUSE | [TableDesk-linux.rpm](https://github.com/jpdealba/tabledesk-downloads/releases/latest/download/TableDesk-linux.rpm) |

¿No sabes qué Mac tienes? Menú  → *Acerca de esta Mac*: si dice "Chip Apple M…" es Apple; si dice "Procesador Intel…" es Intel.

## Instalar (los instaladores no están firmados)

TableDesk todavía no tiene un certificado de firma de Microsoft ni de Apple, así que el sistema avisa
la primera vez. Es normal; así se instala de todos modos:

### Windows
1. Si el navegador dice que el archivo *no se descarga con frecuencia*: menú **⋯** → **Conservar** →
   **Mostrar más** → **Conservar de todos modos**.
2. Abre `TableDesk-windows-setup.exe`. Si aparece **"Windows protegió tu PC"** (SmartScreen):
   pulsa **Más información** → **Ejecutar de todas formas**.
3. Sigue el instalador; TableDesk queda en el menú Inicio.

### macOS
1. Abre el `.dmg` y arrastra **TableDesk** a **Aplicaciones**.
2. Abre TableDesk. Si dice que *no se puede abrir porque Apple no puede verificarlo*:
   - Ve a **Configuración del Sistema → Privacidad y seguridad**, baja hasta el aviso de TableDesk y pulsa
     **Abrir de todos modos**; confirma con tu contraseña o Touch ID.
3. Si en cambio dice que la app **"está dañada"**, abre *Terminal* y ejecuta:
   ```
   xattr -dr com.apple.quarantine /Applications/TableDesk.app
   ```
   y vuelve a abrirla. (Solo quita la marca de "descargado de internet"; no cambia la app.)

### Linux
- **AppImage**: dale permiso de ejecución y ábrelo:
  ```
  chmod +x TableDesk-linux.AppImage
  ./TableDesk-linux.AppImage
  ```
  (Si no abre, instala `libfuse2`: `sudo apt install libfuse2`.)
- **Debian/Ubuntu**: `sudo apt install ./TableDesk-linux.deb`
- **Fedora/openSUSE**: `sudo dnf install ./TableDesk-linux.rpm`

## Actualizar
Descarga de nuevo desde esta página e instala encima; tus conexiones, favoritos e historial se conservan.

## Respaldos con herramientas del servidor (opcional)
Para respaldar Postgres con `pg_dump` o MySQL con `mysqldump`, instala sus herramientas de cliente.
Sin ellas, TableDesk usa su propio respaldo SQL.
