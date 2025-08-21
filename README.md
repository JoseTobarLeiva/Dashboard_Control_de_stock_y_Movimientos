# 📊 Dashboard de Costos y Proyectos

Este proyecto muestra un **Dashboard Interactivo** desarrollado en **Power BI**, se realizo con el objetivo de analizar:
- Datos históricos de materiales.
- control de stock actual vs stock objetivo.
- Entradas y salidas de materiales en distintos períodos.
- Diferencias de stock según movimientos realizados.
- Distribución de materiales por proyectos y productos.


---


## 🛠️ Herramientas Utilizadas
- **Power BI** Para visualización y modelado
- **DAX** para cálculos personalizados.
- **Power Query** para limpieza y transformación de datos.
- **Excel** para integración de información.
- **ERP Odoo** Para recopilar los datos.


---


## 🧮 Formulas DAX utilizadas

- Para calcular el ingreso de stock
  
**" MAX_Entrada =SUMX(FILTER('Movimientos de productos','Movimientos de productos'[Entrada/Salida/Inventario.1]="Entrada"),'Movimientos de productos'[Realizado]) "**
  
- Para calcular las salidas de stock
  
**"MAX_Salida =
   SUMX(
        FILTER(
              'Movimientos de productos',
              'Movimientos de productos'[Entrada/Salida/Inventario.1]="Salida"
        ),
        'Movimientos de productos'[Realizado])**"
  
- Para calcular la diferencias de stock.
  
**"Diferencia stock = [MAX_Entrada]-[MAX_Salida]"**


---


## 📷 Capturas de pantalla


![Dashboard_Heavy_duty](https://github.com/user-attachments/assets/810cc938-dac1-4463-a157-9c22f848a40a)
- Se puede visualizar el stock histórico del producto Heavy Duty, mostrando ingresos, salidas, diferencias y comparación con el stock objetivo.
- El dashboard incluye KPIs y gráficos que reflejan el comportamiento de los materiales en el tiempo.
- Se utilizan filtros dinámicos para seleccionar un rango de tiempo y distintos productos.

![Dashboard_Esmalte_al_agua_blanco](https://github.com/user-attachments/assets/142d0b1b-7826-400f-8b04-b0bf8e052ce1)

- Se puede visualizar el stock histórico del producto Esmalte al Agua,mostrnado la misma lógica aplicada anteriormente.
- El dashboard es totalmente dinámico, por lo que se puede analizar cualquier producto disponible en la ERP Odoo



---


## 📌 Notas
- Por motivos de confidencialidad, no se incluye el archivo '.pbix' con información original.
  
