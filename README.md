# -challenge1-data-science-alura-store-latam

## Descripcion del Proyecto

Este proyecto realiza un analsis completo de datos de ventas de 4 tiendas diferentes, combinando multiples fuentes de datos para extraer insights comerciales e identificar patrones de ventas, compara rendimiento entre tiendas.


### Esquema del DataFrame Consolidado

```python
<class 'pandas.core.frame.DataFrame'>
RangeIndex: 9435 entries, 0 to 9434
Data columns (total 13 columns):
 #   Column                  Non-Null Count  Dtype  
---  ------                  --------------  -----  
 0   Producto                9435 non-null   object 
 1   Categoría del Producto  9435 non-null   object 
 2   Precio                  9435 non-null   float64
 3   Costo de envío          9435 non-null   float64
 4   Fecha de Compra         9435 non-null   object 
 5   Vendedor                9435 non-null   object 
 6   Lugar de Compra         9435 non-null   object 
 7   Calificación            9435 non-null   int64  
 8   Método de pago          9435 non-null   object 
 9   Cantidad de cuotas      9435 non-null   int64  
 10  lat                     9435 non-null   float64
 11  lon                     9435 non-null   float64
 12  Tiendas                 9435 non-null   object 
dtypes: float64(4), int64(2), object(7)
memory usage: 958.4+ KB

Requisitos:
Dependencias Principales

python>=3.12.1
pandas>=1.3.0
numpy>=1.21.0
seaborn>=0.11.0
matplotlib>=3.4.0
google colab
jupyter>=1.0.0  # Para notebooks

Ejemplo de Código para Visualización
python


# Grafica Ingresos Totales

# Configurar el estilo de seaborn
sns.set(style="whitegrid")

# Crear el gráfico de barras
plt.figure(figsize=(10, 6))
barplot = sns.barplot(
    data=df_ingresos_totales,
    x="Tiendas", 
    y="Promedio",
    palette="viridis"
)

# Personalizar el gráfico
plt.title("Ingresos Totales por Tienda", fontsize=16, fontweight='bold')
plt.xlabel("Tiendas", fontsize=12)
plt.ylabel("Ingresos Totales", fontsize=12)

# Añadir los valores encima de cada barra
for bar in barplot.patches:
    barplot.annotate(
        f'{bar.get_height():,.0f}',
        (bar.get_x() + bar.get_width() / 2, bar.get_height()),
        ha='center', va='bottom',
        fontsize=11, fontweight='bold'
    )

# Ajustar layout
plt.tight_layout()

# Mostrar el gráfico
plt.show()


🤝 Contribución

¡Las contribuciones son bienvenidas! Sigue estos pasos:

    Fork el proyecto

    Crea una rama para tu feature (git checkout -b feature/AmazingFeature)

    Commit tus cambios (git commit -m 'Add some AmazingFeature')

    Push a la rama (git push origin feature/AmazingFeature)

    Abre un Pull Request

📄 Licencia

Distribuido bajo la licencia MIT. Ver LICENSE para más información.
📧 Contacto

Tu Nombre - @tuusuario - email@ejemplo.com

Enlace del proyecto: https://github.com/tu-usuario/analisis-ventas-tiendas