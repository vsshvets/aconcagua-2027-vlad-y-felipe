[← volver al inicio](../README.md)

# Datos

Tablas planas en CSV (se abren en Excel o Google Sheets). Precios en la moneda indicada en cada fila.

| Archivo | Qué contiene |
|---|---|
| [precios-permisos.csv](precios-permisos.csv) | Tarifas oficiales de permisos: preventa 2026-27, temporada 2025-26 y preventa 2025-26 |
| [proveedores.csv](proveedores.csv) | Las 11 empresas habilitadas: contactos, unidades por campamento, paquete y precio conocido |
| [campamentos.csv](campamentos.csv) | Puntos de la Ruta Normal con alturas (usada y rango), tiempos y servicios |
| [equipo.csv](equipo.csv) | Lista de equipo por persona con pesos aproximados y dónde va |
| [comida.csv](comida.csv) | Plan de comida por tipo de día con totales para dos personas |
| [seguros.csv](seguros.csv) | Opciones de seguro comparadas |
| [presupuesto.csv](presupuesto.csv) | Presupuesto por persona en USD |

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

**campamentos.csv**

| Columna | Significado |
|---|---|
| altura_usada_m | Altura usada en esta guía; altura_min/max_fuentes_m es el rango entre fuentes |
| distancia_km, desnivel_m, tiempo_tipico_h | Desde el punto anterior (texto cuando es un rango) |

**equipo.csv**

| Columna | Significado |
|---|---|
| cantidad_por_persona | Unidades por persona (si compartido = sí, una para los dos) |
| donde_va | cuerpo (puesto), mochila, mula (llega a Plaza de Mulas) o auto |
| peso_aprox_g_unidad | Peso aproximado de un modelo típico, en gramos |
| obligatorio_o_clave | sí = obligatorio o imprescindible; clave; recomendado; opcional |

**comida.csv**

| Columna | Significado |
|---|---|
| tipo_de_dia | bajo (Confluencia/Plaza de Mulas, 8 días), altura (Canadá/Nido/Cólera y reservas, 8 días), cumbre |
| g_por_persona_por_dia | Gramos secos por persona por día |
| total_g_con_10pct_reserva | g × días × personas × 1,1 (sin reserva en los extras de cumbre y la fruta fresca) |

**presupuesto.csv**

| Columna | Significado |
|---|---|
| por_persona_min_usd / max_usd | Rango en dólares por persona |
| tipo | obligatorio, posible, según lo que tengan, opcional |
| confianza | alta = norma oficial; media = precio publicado por la empresa o terceros; baja = estimación |
