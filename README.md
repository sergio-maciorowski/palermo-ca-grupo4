# palermo-ca-grupo4
Computacion Aplicada - Trabajo práctico integrador grupal 2025-2C

## Integrantes:
- María Graciela García
- Brian Grau
- Sergio Maciorowski
- Diego Salatino
Restaurar /var

## Backup de /var
### Creación
El backup del directorio `/var` se creó utilizando el siguiente comando:

```bash
tar czpvf - /var/ | split -d -b 50M - var_bkp_split
```
### Restauración
Para reconstruirlo el archivo original y restaurar el contenido en `/var`, ejecutar:

```bash
cat var_bkp_split* | tar xzpvf -
```
Basado en: https://superuser.com/a/290990
