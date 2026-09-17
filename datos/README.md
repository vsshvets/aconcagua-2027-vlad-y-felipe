[← volver al inicio](../README.md)

# Datos

Tablas planas en CSV (se abren en Excel o Google Sheets). Precios en la moneda indicada en cada fila.

| Archivo | Qué contiene |
|---|---|
| [precios-permisos.csv](precios-permisos.csv) | Tarifas oficiales de permisos: preventa 2026-27, temporada 2025-26 y preventa 2025-26 |
| [proveedores.csv](proveedores.csv) | Las 11 empresas habilitadas: contactos, unidades por campamento, paquete y precio conocido |

## Columnas

**precios-permisos.csv**

| Columna | Significado |
|---|---|
| temporada | Temporada estival del parque (1 nov a 30 abr) |
| modalidad | `preventa` (con sus fechas) o `normal` |
| ruta | Horcones (ruta normal), Vacas / 360 o Matienzo |
| actividad | Ascenso (20 días), Trekking largo (7), Trekking diario (1) |
| categoria | Categoría de visitante según la norma |
| asistencia | `con asistencia` = con empresa habilitada que presta los servicios esenciales |
| moneda, precio | Monto por persona. Los USD se pagan en pesos al cambio comprador del Banco Nación del día anterior |
| vigencia_dias | Días de validez del permiso desde el ingreso |
| fuente, url | Norma o comunicado oficial |

**proveedores.csv**

| Columna | Significado |
|---|---|
| email_oficial, telefono_oficial | Tal como figuran en la lista oficial del Parque |
| email_web, whatsapp_web | Datos adicionales publicados en la web de la empresa |
| legajo_evt | Legajo de Empresa de Viajes y Turismo (vacío si la lista oficial no lo indica) |
| unidades_* | Unidades funcionales adjudicadas por campamento (Decreto 1885/2026, según MDZ) |
| precio_conocido_usd_por_persona | Precio del paquete mínimo, sin permiso; vacío si no es público |
| confianza_precio | alta = web oficial de la empresa; media = cotización publicada por terceros; baja = testimonio |
