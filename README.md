# IRIE San Juan — Informe Ejecutivo Interactivo

[![San Juan](https://img.shields.io/badge/Gobierno-San%20Juan-1d4f91?style=for-the-badge)](https://www.sanjuan.gob.ar/)
[![IIEE](https://img.shields.io/badge/IIEE-Información%20económica-2563eb?style=for-the-badge)](https://web.sanjuan.gob.ar/iiee/)
[![UNIDE](https://img.shields.io/badge/UNIDE-Datos%20geoespaciales-0f766e?style=for-the-badge)](https://web.sanjuan.gob.ar/unide/)
[![ONU](https://img.shields.io/badge/ONU-Estadísticas%20oficiales-009edb?style=for-the-badge)](https://unstats.un.org/fpos/)

Aplicación web de una sola página para presentar el diagnóstico preliminar del **Índice de Riesgo de Información para Inversores (IRIE)** de San Juan y su relación con el financiamiento de infraestructura.

El informe está orientado a la toma de decisiones ministeriales y resume brechas de información pública, acciones prioritarias y mecanismos de seguimiento financiero y territorial.

> **La lógica financiera es directa: el bono financia infraestructura; la información pública financia confianza.**

## 🧭 Funcionalidades

- Panel ejecutivo con nivel de riesgo IRIE.
- Matriz IRIE acompañada por un gráfico radial.
- Evaluación ITEI para infraestructura y uso de fondos.
- Acceso directo al benchmark provincial.
- Línea de tiempo continua del disclosure financiero.
- Plan 30–60–90 presentado como Gantt interactiva.
- Filtros por etapa y detalle de cada actividad.
- Registro de tareas completadas mediante `localStorage`.
- Propuesta de georreferenciación basada en UNIDE.
- Fórmulas, rangos y valores recomendados para IRIE e ITEI.
- Diseño adaptable a escritorio y dispositivos móviles.
- Exportación mediante la función de impresión del navegador.

## 🚀 Uso

No requiere instalación, servidor ni dependencias externas.

1. Descargá el archivo:

   `index.html`

2. Abrilo con un navegador moderno.
3. Usá el menú lateral para navegar entre secciones.
4. En la Gantt podés:
   - Filtrar actividades por 30, 60 o 90 días.
   - Seleccionar una actividad para consultar su detalle.
   - Marcar actividades completadas.
   - Conservar el progreso en el navegador.

Para generar un PDF, seleccioná **“Exportar / imprimir PDF”** y elegí la opción de guardar como PDF.

## 🗂️ Estructura

```text
.
├── informe_irie_sanjuan_ministro_disclosure_v4.html
└── README.md
```

Toda la interfaz, los estilos, los datos y la lógica están contenidos en un único archivo HTML.

## 📊 Indicadores

### 🔎 IRIE

Índice de Riesgo de Información para Inversores:

```text
IRIE = 100 − 20 × Σ(wᵢ × sᵢ) / Σwᵢ
```

- `sᵢ`: puntaje de cada dimensión, entre 0 y 5.
- `wᵢ`: peso asignado a la dimensión.
- Valor recomendado: `IRIE ≤ 39`.
- Objetivo inicial sugerido para San Juan: `IRIE < 60`.

### 🏗️ ITEI

Índice de Trazabilidad Estadística de Infraestructura:

```text
ITEI = 100 × Σ(wⱼ × cⱼ) / Σwⱼ
```

- `cⱼ`: nivel de cumplimiento, entre 0 y 1.
- `wⱼ`: peso del indicador.
- Valor recomendado: `ITEI ≥ 80`.
- Mínimo sugerido antes de una emisión: `ITEI ≥ 60`.

## 🗺️ Georreferenciación

La propuesta territorial contempla vincular cada obra con:

- Identificador único.
- Coordenadas y departamento.
- Organismo ejecutor.
- Fondos asignados y desembolsados.
- Avance físico-financiero.
- Empleo y proveedores.
- Población beneficiaria e impacto territorial.

Servicios oficiales de referencia:

- [Portal UNIDE](https://web.sanjuan.gob.ar/unide/)
- [Geoservicios WMS](https://web.sanjuan.gob.ar/unide/geoservicios/)
- [Catálogo de metadatos](https://unide.sanjuan.gob.ar/geonetwork/srv/spa/catalog.search)

El acceso al antiguo GeoPortal no se incluye porque, al momento de preparar esta versión, presentaba una respuesta inválida.

## 🏛️ Instituciones y marcos de referencia

| Icono | Institución | Aporte al proyecto |
|:---:|---|---|
| 🏛️ | [Gobierno de San Juan](https://www.sanjuan.gob.ar/) | Marco institucional provincial. |
| 📈 | [IIEE San Juan](https://web.sanjuan.gob.ar/iiee/) | Producción y publicación de información económica y estadística. |
| 🗺️ | [UNIDE San Juan](https://web.sanjuan.gob.ar/unide/) | Infraestructura de datos espaciales, geoservicios y metadatos. |
| 🌐 | [Naciones Unidas — Estadísticas](https://unstats.un.org/fpos/) | Principios fundamentales para las estadísticas oficiales. |
| 💼 | [GFOA](https://www.gfoa.org/) | Buenas prácticas de gestión financiera y disclosure gubernamental. |
| 📑 | [MSRB / EMMA](https://www.msrb.org/) | Referencia para divulgación continua orientada a inversores. |
| 🌱 | [ICMA](https://www.icmagroup.org/) | Principios para bonos verdes y financiamiento sostenible. |

### Enlaces técnicos

- [Principios Fundamentales de las Estadísticas Oficiales de Naciones Unidas](https://unstats.un.org/fpos/)
- [GFOA — Continuing Disclosure Responsibilities](https://www.gfoa.org/materials/understanding-your-continuing-disclosure-responsibilities)
- [MSRB — Primary and Continuing Disclosure Obligations](https://www.msrb.org/Education/Primary-and-Continuing-Disclosure-Obligations)
- [ICMA — Green Bond Principles](https://www.icmagroup.org/sustainable-finance/the-principles-guidelines-and-handbooks/green-bond-principles-gbp/)
- [UNIDE San Juan](https://web.sanjuan.gob.ar/unide/)

## ⚙️ Consideraciones técnicas

- HTML5, CSS y JavaScript nativo.
- Sin frameworks ni paquetes de terceros.
- Sin envío de datos a servidores.
- El progreso de la Gantt se almacena únicamente en el navegador del usuario.
- Compatible con las versiones actuales de Chrome, Edge, Firefox y Safari.

## ⚠️ Alcance

El documento constituye una **evaluación preliminar basada en disponibilidad web observable y diagnóstico institucional**. Los puntajes y comparaciones no reemplazan una auditoría técnica, financiera, legal o estadística formal.

## 📄 Licencia

Antes de publicar el repositorio, definí la licencia aplicable y las condiciones de reutilización de los datos, textos y elementos institucionales.
