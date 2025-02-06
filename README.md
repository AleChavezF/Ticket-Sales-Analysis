# 📊 Análisis de Tickets de Compra y Reglas de Asociación  

Este proyecto implementa un análisis de datos de tickets de compra utilizando técnicas de **Market Basket Analysis**, incluyendo **Apriori**, **FP-Growth** y **análisis de correlaciones** entre productos.  

La base de datos se obtuvo del sistema de gestión de ventas de un restaurante de la ciudad de Villa Elisa - Paraguay
---

## 🚀 **Objetivo del Proyecto**  
El objetivo principal de este análisis es identificar patrones en las compras de los clientes, generar **reglas de asociación** entre productos y visualizar la **relación entre productos con alta correlación**, lo que puede ser útil para estrategias de venta cruzada y promociones.  

---

## 📂 **Estructura del Proyecto**  

📁 **datasets/**  
- `ventas_tickets.csv` → Dataset con los datos de ventas de productos.  

📁 **notebooks/**  
- `analisis_tickets.ipynb` → Notebook principal con el análisis completo.  

📁 **outputs/**  
- `reglas_estructuradas.csv` → Archivo con las reglas de asociación generadas.  
- `correlaciones_estructuradas.csv` → Archivo con las correlaciones entre productos.  
- `top_combinaciones.csv` → Archivo con las combinaciones más frecuentes de productos.  

📁 **scripts/**  
- `fix_ticket_analysis.py` → Script en Python con el código del análisis.  

📄 **README.md** → Este documento con información sobre el proyecto.  

---

## 🔹 **Metodología del Análisis**  

1️⃣ **Carga y limpieza de datos**  
   - Se procesan los datos de ventas, eliminando valores nulos y limpiando categorías irrelevantes (como "Delivery").  

2️⃣ **Transformación de datos para Market Basket Analysis**  
   - Se agrupan productos por transacción y se convierten en formato binario para aplicar los algoritmos.  

3️⃣ **Aplicación de Apriori y FP-Growth**  
   - Se comparan ambos métodos para identificar conjuntos de productos frecuentemente comprados juntos.  
   - **FP-Growth** es más eficiente en bases de datos dispersas, como en este caso.  

4️⃣ **Generación de reglas de asociación**  
   - Se calculan reglas basadas en **confianza**, **lift** y **support**, y se filtran las más relevantes.  

5️⃣ **Análisis de correlaciones entre productos**  
   - Se genera una **red de correlaciones**, mostrando los productos con una relación fuerte en las compras.  

6️⃣ **Visualizaciones**  
   - Gráfico de red de correlaciones.  
   - Gráfico de reglas de asociación basado en confianza.  

---

## 📊 **Ejemplo de Resultados**  

### 🔹 **Ejemplo de Reglas de Asociación**  
📌 _Si un cliente compra **Mandi'o Chyryry**, es probable que también compre **Tortilla 8 Unidades** (Confianza: 57%)_.  

📌 _Si un cliente compra **Café Americano**, es probable que compre **Alfajor** (Confianza: 50%)_.  

### 🔹 **Ejemplo de Correlaciones Entre Productos**  
📌 **Cerveza OPA** y **Pizza Napolitana** tienen una alta correlación (>0.6), lo que indica que suelen comprarse juntas.  

📌 **Ensalada César** y **Topping de Huevo** también muestran una fuerte relación en las ventas.  

---

## 🛠 **Requisitos y Librerías Utilizadas**  

Este proyecto fue desarrollado en **Python 3.11.11** y requiere las siguientes librerías:  

```
Pandas: 2.2.2
Numpy: 1.26.4
Matplotlib: 3.10.0
Seaborn: 0.13.2
Mlxtend: 0.23.4
NetworkX: 3.4.2
```

---

## 💡 **Cómo Ejecutar el Proyecto**  

Para ejecutar el análisis, sigue estos pasos:  

1. **Clona el repositorio**  
   ```
   git clone https://github.com/tu_usuario/tu_repositorio.git
   cd tu_repositorio
   ```
2. **Instala las dependencias**
```pip install -r requirements.txt```

3. **Ejecuta el script de análisis**
``` python scripts/fix_ticket_analysis.py  ```
4. **O abre el Jupyter Notebook para ver los resultados de manera interactiva:**
``` jupyter notebook notebooks/analisis_tickets.ipynb ```

## 📝 Conclusión y Próximos Pasos  

📌 **Conclusión**  
Este análisis nos ha permitido identificar **patrones en las compras** y descubrir **productos que suelen adquirirse juntos**. Esto puede ser utilizado para **optimizar estrategias de marketing, promociones y recomendaciones de productos** en un negocio.  

📌 **Próximos Pasos**  
✅ Mejorar la visualización de los resultados con dashboards interactivos.  
✅ Aplicar modelos de Machine Learning para predicciones de compras futuras.  
✅ Integrar datos de clientes para personalizar ofertas según hábitos de compra.  

---

📌 **Este análisis es un primer paso para optimizar decisiones de negocio basadas en datos de ventas.** 🚀  

