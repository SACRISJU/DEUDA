# Datos — Deuda Pública por Presidente

Estructura del directorio de datos.

## Organización

```
data/
  spain/
    debt_monthly.csv     — Deuda mensual 1994-12 → presente
    debt_monthly_raw.csv — Descarga original del Banco de España
    presidents.json      — Presidentes con fechas exactas de mandato
  usa/                   — (pendiente)
  panama/                — (pendiente)
```

---

## España (`spain/`)

### `debt_monthly.csv`

| Columna | Descripción | Unidad |
|---------|-------------|--------|
| `date` | Año-Mes (YYYY-MM) | — |
| `total_aapp_miles_eur` | Deuda total AAPP (EDP) | Miles de € |
| `estado_miles_eur` | Deuda del Estado | Miles de € |
| `ccaa_miles_eur` | Comunidades Autónomas | Miles de € |
| `ccll_miles_eur` | Corporaciones Locales | Miles de € |
| `ss_miles_eur` | Seguridad Social | Miles de € |

- **Cobertura:** diciembre 1994 → presente
- **Frecuencia:** mensual
- **Fuente:** Banco de España — Tabla 11.b (Boletín Estadístico), Protocolo de Déficit Excesivo (PDE/EDP), metodología SEC2010
- **URL fuente:** https://www.bde.es/webbe/es/estadisticas/compartido/datos/csv/be11b.csv
- **Nota:** Los valores `_` indican dato no disponible aún en la fuente oficial.

### `presidents.json`

Presidentes del Gobierno desde la restauración democrática (1977).
Fechas según Real Decreto de nombramiento publicado en el BOE.

---

## Notas generales

- Todos los valores monetarios están en **miles de euros (€ 000)**. Para obtener millones de euros, dividir entre 1.000.
- La deuda EDP (Protocolo de Déficit Excesivo) es la métrica oficial utilizada por la Comisión Europea y el Banco Central Europeo para evaluar la sostenibilidad fiscal de los estados miembros de la UE.
- Los datos del Banco de España pueden sufrir revisiones retroactivas.
