# TP Integrador - Computación Aplicada (2026 C1)

## Grupo 01

### Integrantes
- Herman Cesar
- Omar Jeremías PalMastromaureas
- Roberto Ignacio Mastromaure
- Luciana Fierro

## Descripción
Repositorio correspondiente al Trabajo Práctico Integrador de Computación Aplicada (Modalidad Online).

Se configuró un servidor GNU/Linux **Debian 12** (hostname `TPServer`) sobre una máquina virtual, con:
- Acceso remoto por **SSH** mediante clave pública/privada para el usuario root
- Servidor web **Apache** con soporte **PHP**
- Base de datos **MariaDB** (base `ingenieria`)
- **IP estática** en el rango de la red física
- **Almacenamiento adicional** con dos particiones montadas de forma persistente (`/www_dir` y `/backup_dir`)
- **Script de backup** automatizado mediante `cron`

### Contenido del repositorio
Los directorios solicitados (`/root`, `/etc`, `/opt`, `/www_dir`, `/backup_dir`) están comprimidos individualmente en formato `.tar.gz`. El directorio `/var` se dividió en partes menores a 25 MB (`var_part_*`).

Para reconstruir /var:
    cat var_part_* > var.tar.gz
    tar -xzf var.tar.gz
