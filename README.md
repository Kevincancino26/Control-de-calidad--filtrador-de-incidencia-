# 📊 Filtrador de Datos de Calidad - Procesamiento de Incidencias  

[![Python](https://img.shields.io/badge/Python-3.13.5-blue?logo=python)](https://www.python.org/)  
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)](https://jupyter.org/)  
[![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-success?logo=pandas)](https://pandas.pydata.org/)  
[![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-yellow?logo=powerbi)](https://powerbi.microsoft.com/)  

---

## 📋 Descripción  
Este proyecto procesa y analiza **datos de incidencias de calidad** en un taller mecánico.  

📌 Funcionalidades:  
- Carga de archivos Excel  
- Limpieza de datos (filtrado de filas nulas)  
- Análisis de causas raíz de incidencias  
- Exportación de resultados a Excel  
- Integración con **Power BI** para visualización avanzada  

---

## 🚀 Funcionalidades Principales  
- **Exploración de archivos Excel** → Listado de hojas  
- **Carga inteligente de datos** → Ajuste automático de encabezados  
- **Limpieza de datos** → Eliminación de valores faltantes  
- **Análisis de incidencias** → Conteo detallado por categoría  
- **Exportación de resultados** → Generación de archivo `datosfiltradosdelmes.xlsx`  

---

## 📊 Ejemplo de Resultados  

### Principales Causas de Incidencia  
- **SIN OBSERVACION:** 484 casos  
- **SIN TAPETE:** 176 casos  
- **SIN PLASTICO Y TAPETE:** 62 casos  
- **SIN POLIZA EN VEHICULO:** 45 casos  
- **SIN PLASTICO NI TAPETE:** 32 casos  

### Dashboard en Power BI  
- Total de incidencias mensuales *(ej: 978 en el período)*  
- Análisis por categoría, técnico, lavador y asesor  
- Comparación mensual *(mayo vs junio 2025)*  
- Ranking de personal con más incidencias  

---

## 🛠️ Tecnologías Utilizadas  
- **Python 3.13.5**  
- **Pandas**  
- **Openpyxl** (para manejo de Excel)  
- **Jupyter Notebook**  
- **Power BI**  

---

## 📁 Estructura del Código  

### Importación de Librerías  
```python
import pandas as pd

excel_file = pd.ExcelFile(url)
print("Hojas disponibles en el archivo:")
print(excel_file.sheet_names)

df_ = pd.read_excel(url, sheet_name='2025 Junio ', header=1)

dg = pd.DataFrame(df_[['FECHA','CAUSA A RAIZ DE LA INCIDENCIA (CI)',
                       'ORDEN DE SERVICO','VEHICULO ',
                       'ASESOR', 'TECNICO ', ' lavador']])
dg = dg.dropna()
conteo = dg['CAUSA A RAIZ DE LA INCIDENCIA (CI)'].value_counts()

dg.to_excel('datosfiltradosdelmes.xlsx', index=False)
```
## 📷 Dashboar de Seguimiento de Incidencias  

### Vista previa de la hoja 1
![Hoja 1](https://raw.githubusercontent.com/Kevincancino26/Control-de-calidad--filtrador-de-incidencia-/main/hoja%201.jpg)

### Vista previa de la hoja 2
![Hoja 2](https://raw.githubusercontent.com/Kevincancino26/Control-de-calidad--filtrador-de-incidencia-/main/hoja%202.jpg)


---

## 📈 Aplicaciones del Análisis
- **Identificación de problemas recurrentes**
- **Mejora en protocolos de control de calidad**
- **Capacitación de personal en áreas críticas**
- **Seguimiento del desempeño mensual**
- **Optimización de recursos en función de tendencias**

---
## 📝 Notas Adicionales

- **Adaptar el nombre de la hoja según el periodo: '2025 Junio ' → '2025 Julio '**

- **El dashboard de Power BI se actualiza automáticamente al agregar nuevos datos**

- **El proyecto puede ampliarse para incluir análisis predictivo de incidencias**

---

## 👨‍💻 Desarrollado por Kevin Gutierrez Cancino
- Correo: [kevincancino15@gmail.com](kevincancino15@gmail.com)
- Numero.Cel: +52 2291407161

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Perfil-blue?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/kevin-gutierrez-cancino-8583bb208/)




