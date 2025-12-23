# Telecom X - Analisis de Evasion de Clientes (Churn)

## Descripcion del Proyecto

Este proyecto realiza un analisis exploratorio de datos (EDA) sobre la base de clientes de Telecom X, con el objetivo de identificar los factores que influyen en la evasion de clientes (Churn). El analisis proporciona insights valiosos para desarrollar estrategias de retencion y reducir la tasa de cancelaciones.

## Tabla de Contenidos

- [Descripcion del Proyecto](#descripcion-del-proyecto)
- [Estructura del Proyecto](#estructura-del-proyecto)
- [Requisitos](#requisitos)
- [Instalacion](#instalacion)
- [Uso](#uso)
- [Metodologia](#metodologia)
- [Principales Hallazgos](#principales-hallazgos)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Autor](#autor)

## Estructura del Proyecto

```
telecomx/
│
├── TelecomX_LATAM.ipynb    # Notebook principal con el analisis completo
├── TelecomX_Data.json      # Dataset en formato JSON
└── README.md               # Documentacion del proyecto
```

## Requisitos

- Python 3.8 o superior
- Jupyter Notebook o VS Code con extension de Jupyter

### Dependencias

```
pandas>=1.5.0
matplotlib>=3.6.0
seaborn>=0.12.0
```

## Instalacion

1. Clonar o descargar el repositorio:
```bash
git clone <url-del-repositorio>
cd telecomx
```

2. Instalar las dependencias:
```bash
pip install pandas matplotlib seaborn
```

3. Abrir el notebook en Jupyter o VS Code:
```bash
jupyter notebook TelecomX_LATAM.ipynb
```

## Uso

1. Abrir el archivo `TelecomX_LATAM.ipynb` en Jupyter Notebook o VS Code
2. Ejecutar las celdas en orden secuencial (Shift + Enter)
3. El notebook esta dividido en secciones:
   - **Extraccion**: Carga de datos desde el archivo JSON
   - **Transformacion**: Limpieza y preparacion de datos
   - **Carga y Analisis**: Visualizaciones y analisis estadistico
   - **Informe Final**: Conclusiones y recomendaciones

## Metodologia

### 1. Extraccion de Datos (ETL)
- Carga de datos desde archivo JSON
- Normalizacion de estructura anidada
- Conversion a DataFrame de Pandas

### 2. Transformacion de Datos
- Conversion de tipos de datos
- Tratamiento de valores nulos (imputacion con mediana)
- Eliminacion de duplicados
- Creacion de nuevas variables (cargo diario)
- Estandarizacion de nombres de columnas
- Codificacion de variables binarias

### 3. Analisis Exploratorio
- Estadisticas descriptivas
- Distribucion de la variable objetivo (Churn)
- Analisis por tipo de contrato
- Analisis por metodo de pago
- Analisis por servicio de internet
- Analisis por antiguedad y cargos
- Analisis demografico
- Impacto de servicios adicionales

## Principales Hallazgos

### Tasa General de Cancelacion
- Aproximadamente el **26.5%** de los clientes cancelan el servicio

### Factores de Mayor Riesgo

| Factor | Tasa de Cancelacion |
|--------|---------------------|
| Contrato mes a mes | ~42% |
| Cheque electronico | ~45% |
| Fibra optica | ~42% |
| Adultos mayores | ~41% |
| Sin servicios adicionales | >35% |

### Perfil del Cliente en Riesgo
- Contrato mensual
- Menos de 12 meses de antiguedad
- Pago con cheque electronico
- Servicio de fibra optica
- Sin servicios adicionales (seguridad, soporte)
- Adulto mayor sin pareja ni dependientes

### Recomendaciones Estrategicas
1. Programa de fidelizacion para nuevos clientes
2. Incentivos para migracion a contratos anuales
3. Promocion de pago automatico
4. Revision de calidad del servicio de fibra optica
5. Paquetes de servicios adicionales
6. Atencion especializada para adultos mayores

## Tecnologias Utilizadas

| Tecnologia | Uso |
|------------|-----|
| Python 3.x | Lenguaje de programacion |
| Pandas | Manipulacion y analisis de datos |
| Matplotlib | Visualizacion de datos |
| Seaborn | Visualizacion estadistica |
| Jupyter Notebook | Entorno de desarrollo interactivo |

## Dataset

El dataset contiene **7,267 registros** de clientes con las siguientes categorias de informacion:

- **Datos del cliente**: ID, genero, edad, pareja, dependientes
- **Servicios telefonicos**: Servicio telefonico, lineas multiples
- **Servicios de internet**: Tipo de internet, seguridad, respaldo, proteccion, soporte, streaming
- **Cuenta**: Tipo de contrato, facturacion, metodo de pago, cargos
- **Variable objetivo**: Churn (cancelacion)

## Proximos Pasos

- [ ] Desarrollo de modelo predictivo de churn (Machine Learning)
- [ ] Analisis de lifetime value (LTV) de clientes
- [ ] Implementacion de A/B testing para estrategias de retencion
- [ ] Analisis de cohortes por periodo de adquisicion

## Autor

**Equipo de Analisis de Datos - Telecom X**

Proyecto desarrollado como parte del desafio de analisis de evasion de clientes.

---

*Fecha de elaboracion: Diciembre 2025*
