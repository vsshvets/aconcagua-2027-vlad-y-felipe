[← volver al inicio](../README.md)

# Datos

Tablas planas en CSV (se abren en Excel o Google Sheets). Precios en la moneda indicada en cada fila.

| Archivo | Qué contiene |
|---|---|
| [precios-permisos.csv](precios-permisos.csv) | Tarifas oficiales de permisos: preventa 2026-27, temporada 2025-26 y preventa 2025-26 |
| [proveedores.csv](proveedores.csv) | Las 11 empresas habilitadas: contactos, unidades por campamento, paquete y precio conocido |
| **[cotizaciones.csv](cotizaciones.csv)** | Las cotizaciones que mandaron las empresas (17-23 sep 2026): un paquete por fila, con el total con permiso y si cubre el plan de 7 noches |
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

**cotizaciones.csv**

| Columna | Significado |
|---|---|
| carpeta | Carpeta del repo con los emails completos y los adjuntos de esa empresa |
| estado | respondió, respondió por WhatsApp, no vende mulas sueltas o sin respuesta |
| precio_usd_por_persona | Precio del paquete tal como lo cotizó la empresa |
| precio_regular_usd_por_persona | Precio sin descuento, cuando la empresa lo indica (en Pared Sur, el Básico Short equivalente) |
| permiso_incluido | sí solo si la empresa escribe que el permiso de USD 950 está dentro del precio |
| total_con_permiso_preventa_usd_por_persona | Precio + USD 950 del permiso de preventa cuando no está incluido. Es la columna para comparar |
| total_dos_personas_usd | El total anterior × 2 |
| mulas_kg_por_persona | Kilos por persona que suben y bajan en mula dentro del paquete |
| seguro_evacuacion_exigido | Altura de evacuación que pide la empresa. El mínimo oficial de la preventa es 5.500 m |
| fuente | Email o adjunto de donde sale la fila; el texto completo está en la carpeta |

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
