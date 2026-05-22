# 🔥 Dashboard PARRILLA

Dashboard interactivo de **inteligencia de negocio** que analiza compras, ventas, márgenes, patrones, concentración y rentabilidad de tres unidades de negocio: **Parrilla 1, Parrilla 2 y Parrilla 3**.

**Periodo analizado:** 01 de enero – 30 de abril de 2026.

![status](https://img.shields.io/badge/estado-final-success) ![stack](https://img.shields.io/badge/stack-HTML%20%2B%20Chart.js-orange) ![pages](https://img.shields.io/badge/deploy-GitHub%20Pages-blue)

---

## 📊 Secciones del dashboard

| # | Sección | Contenido |
|---|---|---|
| 01 | **Resumen Global** | KPIs principales (ventas, compras, ventas netas, utilidad, margen) + KPIs avanzados (markup, ventas/día, SKUs, mejor día, tasa de devolución), compra vs venta vs utilidad, participación por negocio y tendencia mensual. |
| 02 | **Rentabilidad por Negocio** | Tarjetas individuales por parrilla (incluye markup, ventas/día y SKUs), comparativo y margen vs. global. |
| 03 | **Análisis Mensual** | Ventas, compras, utilidad y margen mes a mes — consolidado y por negocio (selector). |
| 04 | **Patrones de Venta** | Ventas por día de la semana (con selector por negocio) y distribución de tickets por importe. |
| 05 | **Concentración y Crecimiento** | Curva de Pareto (Top 10/20/50/100 artículos) y crecimiento mensual de ventas por negocio. |
| 06 | **Compras por Artículo** | Artículos más y menos comprados por monto y unidades (consolidado y por negocio). |
| 07 | **Ventas por Artículo** | Artículos más y menos vendidos por importe y unidades. |
| 08 | **Márgenes de Utilidad** | Productos más rentables y productos con utilidad negativa/baja. |
| 09 | **Devoluciones** | Impacto de devoluciones por negocio y por mes. |

### KPIs principales (consolidado)
- **Ventas brutas:** $2,459,494 · **Compras:** $2,104,247
- **Utilidad bruta:** $353,902 · **Margen comercial:** 14.4 % · **Markup sobre costo:** 16.8 %
- **Tickets:** 52,618 · **Ticket promedio:** $46.74 · **Ventas/día:** $20,668
- **SKUs vendidos:** 1,732 · **Top 100 artículos = 57 % de la venta**
- **Tasa de devolución:** 0.07 %

### Hallazgos clave
- **Parrilla 3** es la más rentable por peso vendido (margen 17.4 %, markup 21 %); **Parrilla 1** es la de mayor volumen.
- **Domingo** es el día más fuerte; **marzo** el mejor mes (+17 a +23 % vs. febrero).
- Productos estrella: *Cigarro suelto* y *Huevo*. Fugas a revisar: *Amstel Ultra* y *Mayonesa Star* se venden por debajo de costo.

---

## 🔗 Mapeo de negocios

| Cajero | Almacén | Negocio |
|---|---|---|
| Cajero 1 | Parrilla 1 | **PARRILLA1** |
| Cajero 2 | Parrilla 2 | **PARRILLA2** |
| Cajero 3 | Parrilla 3 | **PARRILLA3** |

---

## 🚀 Publicar en GitHub Pages

1. Crea un repositorio nuevo en GitHub (por ejemplo `dashboard-parrilla`).
2. Sube estos archivos:
   - `index.html`
   - `data.json` *(opcional — los datos también vienen embebidos en el HTML)*
   - `README.md`
3. En GitHub: **Settings → Pages**.
4. En *Source* elige la rama `main` y la carpeta `/ (root)`. Guarda.
5. En 1–2 minutos tu dashboard estará en línea en:
   `https://<tu-usuario>.github.io/dashboard-parrilla/`

> El dashboard es **100 % estático y autocontenido**: los datos están embebidos en `index.html`, por lo que también funciona abriendo el archivo directamente en el navegador (doble clic).

---

## 🛠️ Detalles técnicos

- **HTML + CSS + JavaScript** sin frameworks. **Chart.js 4.4** (CDN) para todas las gráficas.
- Tipografías: *Bricolage Grotesque*, *Sora* y *Space Mono* (Google Fonts).
- Diseño responsivo, tema oscuro "carbón & brasa". Secciones interactivas con tabs y tooltips.

### Nota metodológica
La **utilidad** es *rentabilidad bruta compra-venta*: ventas netas (ventas − devoluciones) menos compras del periodo. **No** descuenta gastos operativos (renta, nómina, servicios) ni ajusta por variación de inventario; representa el **margen comercial**, no la utilidad neta contable. La utilidad por artículo se estima como venta − (unidades vendidas × costo unitario de compra).

---

## 📁 Estructura

```
dashboard-parrilla/
├── index.html      ← Dashboard completo (datos embebidos)
├── data.json       ← Datos del análisis (referencia)
└── README.md
```
