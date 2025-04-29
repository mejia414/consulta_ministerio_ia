# Clasificador de Empresas con IA Local 🤖

Este proyecto implementa un sistema automatizado para clasificar empresas colombianas según su tipo de razón social (pública, privada o mixta) utilizando Modelos de Lenguaje Local (LLM) a través de Ollama.

## 🎯 Objetivo

Automatizar el proceso de clasificación de empresas según su naturaleza jurídica (pública, privada o mixta) utilizando técnicas de Inteligencia Artificial, específicamente con modelos de lenguaje que se ejecutan localmente.

## ✨ Características

- Procesamiento automatizado de datos desde archivos Excel
- Utilización de modelos LLM locales (Gemma y DeepSeek)
- Sistema de clasificación robusto con manejo de errores
- Procesamiento por lotes con respaldo automático
- Exportación de resultados en formato Excel
- Validación de datos con Pydantic

## 🛠️ Tecnologías Utilizadas

- **Python**: Lenguaje principal de desarrollo
- **Ollama**: Framework para ejecutar LLMs localmente
- **Modelos utilizados**:
  - Gemma
  - DeepSeek
- **Bibliotecas principales**:
  - pandas: Procesamiento de datos
  - pydantic: Validación de datos
  - tqdm: Barras de progreso
  - numpy: Operaciones numéricas

## 📁 Estructura del Proyecto

```
consulta_ministerio_ia/
├── data/                   # Archivos de datos
│   ├── empresas.xlsx      # Dataset completo
│   ├── mini.xlsx          # Dataset de prueba
│   └── result.xlsx        # Resultados procesados
├── result/                # Resultados individuales
├── notebook.ipynb         # Notebook principal
├── requirements.txt       # Dependencias del proyecto
└── README.md             # Esta documentación
```

## 🚀 Cómo Usar

1. **Preparación del Entorno**
   ```bash
   # Clonar el repositorio
   git clone [url-del-repositorio]
   cd consulta_ministerio_ia

   # Crear y activar entorno virtual
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate

   # Instalar dependencias
   pip install -r requirements.txt
   ```

2. **Configurar Ollama**
   - Asegúrate de tener Ollama instalado y ejecutándose
   - Los modelos necesarios se descargarán automáticamente

3. **Ejecutar el Clasificador**
   - Abre el notebook `notebook.ipynb` en Jupyter
   - Ejecuta las celdas en orden
   - Los resultados se guardarán en `data/result.xlsx`

## 📊 Flujo de Trabajo

1. Carga de datos desde Excel
2. Preprocesamiento y normalización
3. Consulta al modelo LLM
4. Validación y clasificación
5. Almacenamiento de resultados
6. Exportación final

## 🎯 Clasificaciones

El sistema clasifica las empresas en las siguientes categorías:
- **Pública**: Control estatal mayoritario
- **Privada**: Capital completamente privado
- **Mixta**: Participación público-privada
- **Indefinido**: Cuando no hay información suficiente

## ⚙️ Configuración

El sistema permite configurar varios parámetros:
- Tiempo máximo de respuesta (timeout)
- Modelo a utilizar (Gemma o DeepSeek)
- Número de reintentos en caso de error
- Temperatura del modelo

## 📝 Notas

- Los modelos se ejecutan localmente, garantizando la privacidad de los datos
- El sistema implementa respaldo automático para evitar pérdida de progreso
- Se recomienda usar GPU para mejor rendimiento

## 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor, abre un issue primero para discutir los cambios que te gustaría hacer.

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo LICENSE para más detalles.