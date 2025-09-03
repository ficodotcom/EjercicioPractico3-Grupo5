# Proyecto: Análisis de Rankings de Empresas en Ecuador (2010–2016)

## 📌 Descripción
Este proyecto realiza un **análisis exploratorio de datos (EDA)** sobre un dataset que recopila información de empresas ecuatorianas entre los años 2010 y 2016.  
El objetivo es **comprender la estructura del tejido empresarial en Ecuador**, su evolución y las características más relevantes de las compañías en distintos sectores y regiones.  

---

## 📂 Dataset
**Archivo:** `combined_ranking_data.csv`  
**Número de registros:** ~255,000  
**Número de columnas:** 22  

### Variables principales:
- **Identificación:** `Expediente`, `Nombre`, `RUC`  
- **Clasificación:** `Tipo Compañia`, `Actividad económica`, `Sector`, `Tamaño`  
- **Ubicación:** `Región`, `Provincia`, `Ciudad`  
- **Recursos humanos:** `Cant_Empleados`  
- **Finanzas:** `Activo`, `Patrimonio`, `Ingreso_por_ventas`, `Utilidad antes del impuesto`, `Utilidad del ejercicio`, `Utilidad neta`, `IR causado`, `Ingreso Total`  
- **Metadatos de ranking:** `Posicion`, `Anio`, `Posicion_1`, `Anio_1`  

---

## ⚙️ Proceso realizado en el Notebook

1. **Carga de datos**
   - Se utilizó `pandas` para leer el CSV, especificando `delimiter=";"` y `encoding="utf-8"`.  
   - Se ajustó el encabezado con `header=0` para alinear correctamente las columnas.  

2. **Inspección inicial**
   - Visualización con `df.head()` para conocer las primeras filas.  
   - Exploración de metadatos con `df.info()` y `df.describe()`.  
   - Identificación del número máximo de posiciones (`df['Posicion'].max()`).  

3. **Calidad de los datos**
   - Se detectó que casi todas las columnas están completas.  
   - Única excepción: la columna `Tamano`, que presenta valores nulos en varios registros.  

4. **Exploración de variables**
   - Análisis de columnas categóricas: distribución de `Sector`, `Tipo Compañia`, `Actividad económica`.  
   - Análisis geográfico: `Provincia`, `Ciudad`, `Región`.  
   - Revisión de métricas financieras (`Activo`, `Ingreso_por_ventas`, `Utilidad`).  

5. **Documentación de hallazgos preliminares**
   - El dataset ofrece información robusta para estudios de competitividad y desarrollo regional.  
   - Se identificó que la mayor parte de la información financiera y de empleados está completa, lo que permite futuros análisis cuantitativos.  

---

## 🧑‍💻 Stack tecnológico
- **Lenguaje:** Python 3  
- **Librerías principales:**  
  - `pandas` → manipulación de datos  
  - `numpy` → cálculos numéricos  
  - (opcionalmente ampliable con `matplotlib` y `seaborn` para visualizaciones)  

---

## 🚀 Posibles extensiones
- Visualizaciones gráficas de distribución de empresas por sector y región.  
- Análisis temporal de crecimiento de empresas por año.  
- Modelado predictivo sobre supervivencia de empresas o tendencias de utilidades.  
- Dashboard interactivo para exploración de resultados.  

---

## 📌 Conclusión
Este proyecto constituye un punto de partida sólido para estudiar el **ecosistema empresarial ecuatoriano (2010–2016)** desde una perspectiva económica, social y regional.  
El dataset es lo suficientemente amplio y detallado como para dar soporte tanto a **investigaciones académicas** como a **análisis de política pública y estrategia empresarial**.
