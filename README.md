# 📊 Análisis de Rendimiento: Benchmarks ANTES vs DESPUÉS

Una aplicación interactiva desarrollada en Python con Dash y Plotly para analizar y comparar el rendimiento de operaciones CRUD y consultas optimizadas utilizando Entity Framework Core, ADO.NET y Dapper.

## 🎯 Propósito

Esta aplicación permite realizar un análisis integral del rendimiento de diferentes tecnologías de acceso a datos en .NET, comparando:

- **ANTES**: Operaciones CRUD tradicionales (Create, Read, Update, Delete)
- **DESPUÉS**: Consultas optimizadas implementadas tras mejoras de rendimiento

## ✨ Características Principales

- 📈 **Gráficos Interactivos**: Visualizaciones dinámicas con Plotly
- 🔄 **Comparativas ANTES vs DESPUÉS**: Análisis temporal de mejoras
- 🏆 **Análisis por Tecnología**: Comparación entre EF Core, ADO.NET y Dapper
- ⚡ **Análisis por Tipo de Operación**: Desglose detallado por Create, Read, Update, Delete
- 📊 **Dashboard Interactivo**: Interfaz web responsiva con Dash
- 🌐 **Análisis Textual Dinámico**: Explicaciones contextuales para cada vista
- 📋 **Resumen Ejecutivo**: Conclusiones y recomendaciones

## 🚀 Instalación y Configuración

### Prerrequisitos

- Python 3.7 o superior
- pip (gestor de paquetes de Python)

### 1. Clonar o Descargar el Proyecto

```bash
# Si tienes git instalado
git clone <tu-repositorio>
cd scripts

# O simplemente descarga los archivos en una carpeta
```

### 2. Instalar Dependencias

```bash
pip install pandas matplotlib plotly dash numpy
```

### 3. Verificar Archivos CSV

Asegúrate de tener los siguientes archivos CSV en el directorio del proyecto:

**Período ANTES (Operaciones CRUD):**
- `CrudBenchmarks-report.csv`
- `AdonetBenchmarks-report.csv`
- `DapperBenchmarks-report.csv`

**Período DESPUÉS (Consultas Optimizadas):**
- `PruebasDeRendimiento.BenchMarks_Despues.EfBenchmarkTests-report.csv`
- `PruebasDeRendimiento.BenchMarks_Despues.AdoNetBenchmarkTests-report.csv`
- `PruebasDeRendimiento.BenchMarks_Despues.DapperBenchmarkTests-report.csv`

## 🎮 Uso de la Aplicación

### Ejecutar la Aplicación

```bash
python pruebas.py
```

### Acceder al Dashboard

1. Abre tu navegador web
2. Navega a: `http://127.0.0.1:8050`
3. La aplicación se cargará automáticamente

### Navegación por las Vistas

El dashboard incluye las siguientes opciones de análisis:

#### 📊 Comparación Completa ANTES vs DESPUÉS
- Vista principal con 4 subgráficos
- Distribución de tiempos y memoria por período
- Promedios por tecnología
- Análisis comparativo integral

#### 🔄 Operaciones CRUD (Antes) - Con Comparativa
- Análisis detallado de operaciones Create, Read, Update, Delete
- Comparación de rendimiento entre tecnologías
- Contexto con datos estimados del período DESPUÉS

#### 🔍 Operaciones de Consulta (Después) - Con Comparativa
- Análisis de consultas optimizadas
- Mejoras implementadas tras optimización
- Comparación con rendimiento original estimado

#### 📈 Análisis de Mejoras de Rendimiento
- Cálculo de porcentajes de mejora
- Distribución de operaciones por período
- Análisis de eficiencia por tecnología

#### 🏆 Comparación por Tecnología
- Rendimiento promedio por tecnología
- Identificación de fortalezas y debilidades
- Recomendaciones de uso

#### ⚡ Análisis por Tipo de Operación
- Desglose por operaciones CRUD individuales
- Identificación de operaciones más costosas
- Patrones de rendimiento por tipo

#### 📋 Resumen y Análisis Final Detallado
- Conclusiones ejecutivas
- Recomendaciones técnicas
- Métricas consolidadas
- Análisis de categorías

## 📁 Estructura del Proyecto

```
scripts/
├── pruebas.py                          # Aplicación principal
├── README.md                           # Este archivo
├── CrudBenchmarks-report.csv           # Datos EF Core (ANTES)
├── AdonetBenchmarks-report.csv         # Datos ADO.NET (ANTES)
├── DapperBenchmarks-report.csv         # Datos Dapper (ANTES)
├── PruebasDeRendimiento.BenchMarks_Despues.EfBenchmarkTests-report.csv     # Datos EF Core (DESPUÉS)
├── PruebasDeRendimiento.BenchMarks_Despues.AdoNetBenchmarkTests-report.csv # Datos ADO.NET (DESPUÉS)
└── PruebasDeRendimiento.BenchMarks_Despues.DapperBenchmarkTests-report.csv # Datos Dapper (DESPUÉS)
```

## 🛠️ Dependencias

| Paquete | Versión | Propósito |
|---------|---------|-----------|
| pandas | >= 1.3.0 | Manipulación y análisis de datos |
| plotly | >= 5.0.0 | Gráficos interactivos |
| dash | >= 2.0.0 | Framework web para aplicaciones analíticas |
| numpy | >= 1.20.0 | Operaciones numéricas |

## 📊 Formato de Datos CSV

Los archivos CSV deben tener la siguiente estructura:

```csv
Method;Mean;Error;StdDev;Allocated
CreateCustomer;1.234 ms;0.045 ms;0.123 ms;1.23 KB
ReadCustomer;0.567 μs;0.012 μs;0.034 μs;0.45 KB
...
```

**Columnas requeridas:**
- `Method`: Nombre del método/operación
- `Mean`: Tiempo promedio de ejecución (con unidad: ms, μs, s)
- `Allocated`: Memoria asignada (con unidad: KB, MB, GB)

## 🔧 Funcionalidades Técnicas

### Normalización de Datos
- **Tiempo**: Conversión automática a microsegundos (μs)
- **Memoria**: Conversión automática a kilobytes (KB)
- **Limpieza**: Eliminación de caracteres especiales y formato consistente

### Análisis Estadístico
- Cálculo de promedios por tecnología y período
- Análisis de distribución con boxplots
- Cálculo de porcentajes de mejora
- Agrupación por categorías de operación

### Visualizaciones
- **Gráficos de Barras**: Comparaciones directas
- **Boxplots**: Distribución de datos
- **Gráficos de Pastel**: Distribución proporcional
- **Scatter Plots**: Análisis de correlación tiempo/memoria
- **Subplots Combinados**: Vistas múltiples integradas

## 📈 Casos de Uso

### Para Desarrolladores
- Identificar cuellos de botella en operaciones específicas
- Seleccionar la tecnología óptima para casos de uso particulares
- Validar mejoras de rendimiento implementadas

### Para Arquitectos de Software
- Tomar decisiones técnicas basadas en datos
- Planificar optimizaciones futuras
- Comparar alternativas tecnológicas

### Para Gerentes de Proyecto
- Entender el impacto de las optimizaciones
- Comunicar mejoras de rendimiento a stakeholders
- Justificar inversiones en optimización

## 🎨 Personalización

### Modificar Colores
```python
colors = {
    'Entity Framework': '#1f77b4',  # Azul
    'ADO.NET': '#ff7f0e',          # Naranja
    'Dapper': '#2ca02c'            # Verde
}
```

### Agregar Nuevas Vistas
1. Crear nueva función de gráfico en la sección correspondiente
2. Agregar opción al dropdown en el layout
3. Incluir lógica en el callback `update_chart`
4. Agregar texto explicativo en `get_analysis_text`

### Modificar Puerto de Ejecución
```python
app.run(debug=True, port=8050)  # Cambiar puerto aquí
```

## 🚨 Solución de Problemas

### Error: Archivo CSV no encontrado
- Verificar que todos los archivos CSV estén en el directorio correcto
- Comprobar nombres de archivos exactos (sensible a mayúsculas/minúsculas)

### Error: Dependencias no instaladas
```bash
pip install --upgrade pandas plotly dash numpy
```

### Puerto en uso
- Cambiar el puerto en el código: `app.run(debug=True, port=8051)`
- O cerrar otras aplicaciones que usen el puerto 8050

### Datos vacíos o incorrectos
- Verificar formato CSV con separador ';'
- Asegurar que las columnas 'Method', 'Mean', 'Allocated' existen
- Comprobar que las unidades estén incluidas en los valores

## 🤝 Contribución

Para contribuir al proyecto:

1. Fork el repositorio
2. Crear rama para nueva funcionalidad (`git checkout -b feature/nueva-funcionalidad`)
3. Realizar cambios y commit (`git commit -m 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Crear Pull Request

## 📝 Licencia

Este proyecto está bajo la Licencia MIT. Ver archivo `LICENSE` para más detalles.

## 📞 Soporte

Para reportar bugs o solicitar funcionalidades:
- Crear un issue en el repositorio
- Incluir detalles del error y pasos para reproducir
- Adjuntar archivos de ejemplo si es necesario

## 🔄 Historial de Versiones

### v1.0.0 (Actual)
- ✅ Implementación inicial completa
- ✅ Dashboard interactivo con Dash
- ✅ 7 tipos de análisis diferentes
- ✅ Normalización automática de datos
- ✅ Texto explicativo dinámico
- ✅ Soporte completo para ANTES vs DESPUÉS

## 🎯 Roadmap Futuro

- [ ] Exportar gráficos a PDF/PNG
- [ ] Análisis de tendencias temporales
- [ ] Comparación con benchmarks de la industria
- [ ] Integración con CI/CD para monitoreo continuo
- [ ] API REST para integración externa
- [ ] Alertas automáticas por degradación de rendimiento

---

**Desarrollado con ❤️ usando Python, Dash y Plotly**

*Para más información técnica, consulta los comentarios detallados en el código fuente.*
