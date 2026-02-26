# 📊 Challenge Telecom X: Análisis de Evasión de Clientes

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-Data_Manipulation-150458.svg)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Data_Visualization-orange.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626.svg)

## Este proyecto forma parte del programa de formación Oracle Next Education (ONE) en colaboración con Alura Latam.

## 🎯 Propósito del Proyecto
El objetivo principal de este proyecto es analizar la base de datos de clientes de la empresa de telecomunicaciones **TelecomX LATAM** para entender y mitigar el **Churn** (tasa de cancelación o evasión de clientes). 

En la industria de las telecomunicaciones, retener a un cliente existente es significativamente más rentable que adquirir uno nuevo. A través de un Análisis Exploratorio de Datos (EDA) y la ingeniería de características, este proyecto identifica los perfiles de usuarios más propensos a darse de baja, con el fin de proporcionar recomendaciones estratégicas que mejoren la lealtad y los ingresos de la compañía.

---

## 📂 Estructura del Proyecto

El repositorio está organizado de la siguiente manera:

* `TelecomX_LATAM.ipynb`: Notebook principal con el código de extracción, limpieza, EDA y conclusiones.
* `TelecomX_Data.json`: Dataset original (contiene datos anidados de clientes).
* `TelecomX_diccionario.md`: Explicación de las columnas del dataset original
* `README.md`: Documentación del proyecto.

---

## 💡 Principales Insights Obtenidos

Durante el Análisis Exploratorio de Datos, se generaron diversas visualizaciones (gráficos de torta, barras e histogramas) que revelaron patrones clave en el comportamiento de los clientes:

1. **La barrera de los primeros meses:** Los histogramas de distribución mostraron que la gran mayoría de las cancelaciones ocurren en las etapas iniciales de la relación con el cliente (bajos meses de *tenure*). Si un cliente supera los primeros meses, su probabilidad de permanencia a largo plazo aumenta drásticamente.

   <img width="556" height="391" alt="image" src="https://github.com/user-attachments/assets/2efe4370-bc75-4355-a3d1-e71e18593ec8" />

2. **El riesgo del contrato mensual:** El análisis cruzado por tipo de contrato evidenció que los clientes con contratos "Month-to-month" tienen una tasa de cancelación alarmantemente alta. Por el contrario, los contratos de 1 o 2 años garantizan una excelente retención.

   <img width="502" height="430" alt="image" src="https://github.com/user-attachments/assets/e1d73427-dbe6-450d-a8d7-f07613ee79db" />

3. **La "Zona de Peligro" en los servicios contratados:** Mediante la creación de una nueva variable que suma los servicios de cada cliente, se descubrió una tendencia no lineal: tener 1 solo servicio es seguro, tener el ecosistema completo (5+ servicios) es muy seguro, pero **tener entre 2 y 4 servicios representa una zona altamente riesgosa** con los picos más altos de evasión.
   
   <img width="617" height="449" alt="image" src="https://github.com/user-attachments/assets/2d36ce8f-aadd-4043-948a-0ffd3d8c993b" />
   
4. **Métodos de pago:** El uso de "Electronic check" está fuertemente correlacionado con el Churn, sugiriendo la necesidad de incentivar el débito automático.
   
   <img width="524" height="496" alt="image" src="https://github.com/user-attachments/assets/cebc0714-f29b-422a-9760-b5cdf79ff707" />
   
---

## 🚀 Instrucciones para ejecutar el Notebook

Este proyecto fue desarrollado utilizando Python y puede ser ejecutado localmente o a través de Google Colab.

### Opción 1: Usando Google Colab
El notebook está configurado para trabajar nativamente en Google Colab.
1. Sube el archivo `TelecomX_LATAM.ipynb` a tu cuenta de Google Colab.
2. Sube el archivo de datos `TelecomX_Data.json` al entorno de Colab (ya sea directamente en la carpeta `/content/` o montando tu Google Drive).
3. Asegúrate de que la ruta en la celda de lectura `pd.read_json('/content/TelecomX_Data.json')` coincida con la ubicación de tu archivo.
4. Ejecuta las celdas.

### Opción 2: Ejecución Local
Si prefieres ejecutarlo en tu máquina local:
1. Clona este repositorio:
    `git clone [https://github.com/tu-usuario/telecomx-churn-analysis.git](https://github.com/tu-usuario/telecomx-churn-analysis.git)`

2. Asegúrate de tener instaladas las dependencias necesarias:
  `pip install pandas numpy matplotlib jupyter`
  
3. Inicia Jupyter Notebook:
  `jupyter notebook`

4. Abre TelecomX_LATAM.ipynb.

5. Comenta o elimina la celda correspondiente a from google.colab import drive (ya que es exclusiva de Colab) y actualiza la ruta del archivo JSON a tu ruta local (ej. pd.read_json('TelecomX_Data.json')).

6. Ejecuta todas las celdas.
   
## Autora
- 👩‍💻 Desarrollado por Agustina Gonella.
