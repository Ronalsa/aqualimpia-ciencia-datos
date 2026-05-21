
# Análisis de Datos — AquaLimpia S.A.
## Proyecto de Ciencia de Datos | IACC 2026

---

## Objetivo General
Analizar el comportamiento de las plantas de tratamiento de aguas
residuales de AquaLimpia S.A. para identificar patrones de
incumplimiento normativo en los niveles de DBO del efluente tratado
y generar información que apoye la toma de decisiones operacionales
y ambientales.

## Preguntas de Investigación
1. ¿Qué variables están más asociadas al incumplimiento normativo
   en los niveles de DBO de salida?
2. ¿Existen diferencias significativas en el desempeño entre las
   plantas Norte, Centro y Sur?
3. ¿Qué planta requiere atención prioritaria según los indicadores
   de cumplimiento normativo?
4. ¿La eficiencia de remoción de DBO es homogénea entre las plantas
   o existen diferencias relevantes?

---

## Dataset Utilizado
- **Archivo:** dataset_set_A_aguas_residuales.xlsx
- **Registros:** 200
- **Variables:** 10
- **Período:** julio — octubre 2025
- **Plantas:** Norte, Centro, Sur
- **Variables críticas:** DBO_salida_mg_L, cumplimiento_norma

### Descripción de Variables
| Variable | Tipo | Descripción |
|----------|------|-------------|
| fecha_registro | Fecha | Fecha del registro diario |
| planta | Texto | Planta de tratamiento |
| caudal_entrada_m3_d | Entero | Caudal de entrada (m³/día) |
| DBO_entrada_mg_L | Entero | DBO de entrada (mg/L) |
| SST_entrada_mg_L | Entero | Sólidos suspendidos totales entrada |
| pH_entrada | Decimal | pH del agua de entrada |
| energia_aeracion_kWh | Decimal | Energía de aireación (kWh) |
| lodos_generados_kg_d | Decimal | Lodos generados (kg/día) |
| DBO_salida_mg_L | Decimal | DBO del efluente tratado (mg/L) |
| cumplimiento_norma | Binario | 1 = cumple norma, 0 = no cumple |

---

## Metodología
El proyecto aplica el ciclo completo de ciencia de datos
establecido por IACC (2026):

1. **Carga de datos:** pd.read_excel() con preparación
   de columna temporal
2. **Exploración inicial:** head(), info(), describe()
   para revisión estructural
3. **Cálculo de métricas:** NumPy para eficiencia de remoción,
   SciPy para intervalos de confianza al 95%
4. **Visualización:** Dashboard con 8 gráficos mediante
   Matplotlib y Seaborn
5. **Exportación:** Reportes Excel diferenciados por área
   y almacenamiento con Joblib
6. **Documentación:** README.md con objetivos,
   proceso y resultados

---

## Librerías Utilizadas
| Librería | Versión | Uso principal |
|----------|---------|---------------|
| pandas | 2.x | Carga y manipulación de datos |
| numpy | 1.x | Cálculo numérico y métricas |
| matplotlib | 3.x | Visualización y dashboard |
| seaborn | 0.x | Visualización estadística |
| scipy | 1.x | Intervalos de confianza |
| joblib | 1.x | Persistencia de resultados |

---

## Estructura del Proyecto
