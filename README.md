# Brecha-Digital
## Diagnóstico de la brecha digital en Argentina con microdatos EPH
### Proyecto de Practicas Profesionalizante 1: Ciencia de Datos e IA

* "DATA": Contiene los datasets que se utilizó inicialmente para la limpieza de datos junto con la base ya limpia ("base_eph.csv" y "base_eph_limpia.csv") inicialmente con 1000 registros y 10 variables, quedando actualmente 921 registros y 10 variables. 
* "notebooks": Contiene los códigos utilizados durante el proyecto comentados y ordenados listo para ejecutar en Google Colab, junto con los graficos realizados.
* "README.md": Documentación general, guía de uso, diccionario de variables y resumen de resultados.

---

## Guia de Instalación y Ejecución 
### Ejecución en Google Colab
1. Descargar el archivo desde la carpeta "notebooks" junto con los archivos ".csv" que están en la carpeta "DATA".
2. Abrir Google Colab (https://colab.research.google.com/) y abrir un nuevo notebook
3. Cargar el archivo "base_eph_limpia" o base_eph_cg.cvs" en la carpeta de archivos de Google Colab.
4. Ejecutar las celdas apretando en "Ejecutar todas".

---

## Diccionario de Variables
1. CODOSU | TIPO = Texto | Descripción: Identificador único de vivienda/hogar
2. REGION | TIPO = Numerico | Descripcion: Región geográfica (1, 40 a 44)
3. REGION_ETQ | TIPO = Texto | Descripcion: Etiqueta legible de las regines Región geográfica (GBA, NOA, NEA, Cuyo, Pampeana, Patagonia)
4. IX_TOT | TIPO = Numerico | Descripcion: Cantidad total de miembros en el hogar  (1 a 9)
5. NIVEL_ED | TIPO = Numérico | Descripción: Nivel educativo del jefe/a de hogar (1 a 5, y 9 = Sin Respuesta).
6. NIVEL_EDU_ETQ | TIPO = Texto | Descripción: Etiquetas legibles del nivel educativo (Primaria incompleta, Primaria completa, Secundaria incompleta, Secundaria completa, Superior)
7. ITF | TIPO = Numérico | Descripción: Ingreso total familiar expresado en pesos ($67.038,89 a $5.884.802,30)
8. DECIFR | TIPO = Numérico | Descripción: Decil de Ingreso Total Familiar (1 a 10)
9. IV12_3 | TIPO = Numérico | Descripción: Acceso a cmputadora en el hogar (1.0 = Sí / 2.0 = No)
10. II7 | TIPO = Numérico | Descripción: Conexión a Internet en la vivienda (1.0 = Sí / 2.0 = No)

---

## Síntesis de hallazgos
* Métricas generales de ingresos (ITF): sobre los 921 hogares analizados, el ingreso familiar promedio es de $779.201,73 y la mediana es de $632.510,43 (percentil 25 $415855.99 en 50 $632510.43 y percentil 75 en $953.989,80).
* Acceso a computadora e ingresos (IV12_3 vs. ITF): los hogares que cuentan con computadora (1 - Sí) presentan un ingreso promedio de $888.707,57 (mediana $728.645,42), superando ampliamente a los hogares sin computadora (2 - No), que registran una media de $584.927,82 (mediana $490.764,06).
* Nivel educativo e ingresos (NIVEL_EDU_ETQ vs. ITF): el ingreso crece de manera directa con el nivel educativo, desde $326.963,58 promedio en Primaria incompleta hasta $1.630.565,61 en Superior. Secundaria incompleta concentra la mayor cantidad de casos (32,68%).
* Disparidad regional (REGION_ETQ vs. IV12_3): Cuyo (60,5% Sí / 39,5% No) y NOA (61,7% Sí / 38,3% No) muestran los porcentajes más bajos de acceso en el hogar, mientras que GBA concentra el mayor volumen total de encuestados (332 hogares).

### Ejecución Local
   ```bash
   git clone (https://github.com/MaguchiR/Brecha-Digital)

Herramientas: Python, Pandas, Matplotlib
Autora: Magali Belen Rojas
Contexto académico: Practicas Profesionalizante 1 - IEA 
