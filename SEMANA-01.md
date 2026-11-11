# Semana 1 — Empezar sin saber nada

**Meta:** entender qué es un dato, hacer tu primer análisis en Excel/Google Sheets y publicar tu primer repositorio.

**Tiempo total:** 5 horas (5 sesiones de 1 hora). Si tienes más tiempo, suma práctica de matemáticas al final.

**Material:** `datos/ventas_mini.csv` (40 pedidos de una tienda ficticia en Chile).

---

## Sesión 1 (1 h) — Preparar el terreno

1. **Crea una cuenta de GitHub** en https://github.com (10 min). Usa un nombre profesional, por ejemplo `nombre-apellido`.
2. **Elige tu herramienta de hojas de cálculo** (10 min):
   - Google Sheets: https://sheets.google.com (gratis, no instalas nada).
   - Excel: si ya lo tienes instalado, úsalo.
3. **Descarga el archivo** `datos/ventas_mini.csv` a una carpeta llamada `semana-01` (10 min).
4. **Crea un archivo `bitacora.md`** con estas tres preguntas (20 min):
   - ¿Por qué quiero aprender análisis de datos?
   - ¿Qué trabajo me gustaría tener en 12 meses?
   - ¿Qué días y a qué hora haré mis 5 horas semanales?

**Entregable de la sesión:** cuenta creada, archivo descargado y bitácora escrita.

---

## Sesión 2 (1 h) — Primer contacto con los datos

1. Abre `ventas_mini.csv` en Google Sheets o Excel.
   - Si todo aparece en una sola columna: en Excel usa **Datos → Texto en columnas** y elige coma como separador. En Sheets usa **Archivo → Importar → Separar por comas**.
2. Responde en tu bitácora:
   - ¿Cuántas filas tiene la tabla (sin contar el encabezado)?
   - ¿Cuántas columnas?
   - ¿Qué significa cada columna?
   - ¿Qué tipo de dato es cada una: texto, número o fecha?
   - ¿Hay celdas vacías?
3. Aprende estos tres conceptos y escríbelos con tus palabras:
   - **Fila** = una observación (un pedido).
   - **Columna** = una variable (fecha, vendedor, región...).
   - **Celda** = un valor concreto.
4. Convierte el rango en **tabla** (Excel: `Ctrl + T`; Sheets: **Formato → Convertir en tabla**), congela la primera fila y aplica formato de moneda a `precio_unitario`.

**Entregable de la sesión:** tabla ordenada con encabezados congelados.

---

## Sesión 3 (1 h) — Tu primera fórmula y porcentajes

1. Crea una columna nueva llamada `ingreso` y calcula `unidades * precio_unitario`.
   - En la primera fila de datos escribe `=E2*F2` (ajusta las letras según tu tabla) y arrastra hacia abajo.
2. Practica estas funciones en celdas separadas:
   - `=SUMA(ingreso)`
   - `=PROMEDIO(ingreso)`
   - `=CONTAR(ingreso)`
   - `=MAX(ingreso)`
   - `=MIN(ingreso)`
3. Aprende a filtrar: filtra `estado = completado` y observa cómo cambia la suma.
4. **Matemáticas aplicadas (15 min):** resuelve estos ejercicios sin calculadora y luego verifica:
   - 15% de 80.000
   - Aumentar 120.000 en 8%
   - Bajar 250.000 en 20%
   - Si 30 de 120 pedidos fueron devueltos, ¿qué porcentaje es?
   - Si una categoría representa el 25% de 4.000.000, ¿cuánto dinero es?
   - Promedio de tres ventas: 100.000, 200.000 y 300.000.

**Entregable de la sesión:** columna `ingreso` calculada y ejercicios resueltos.

---

## Sesión 4 (1 h) — Tus primeras preguntas de negocio

Responde usando fórmulas o una tabla dinámica:

1. ¿Cuál es el ingreso total **solo de pedidos completados**?
2. ¿Qué región genera más ingreso?
3. ¿Qué producto genera más ingreso?
4. ¿Qué vendedor genera más ingreso?
5. ¿Cuál es el ticket promedio por pedido completado?
6. ¿Qué porcentaje de los pedidos fue devuelto?

**Pistas**
- Para sumar con condiciones: `=SUMAR.SI(rango_estado;"completado";rango_ingreso)`.
- Para contar con condiciones: `=CONTAR.SI(rango_estado;"completado")`.
- Una tabla dinámica es más rápida: selecciona la tabla → **Insertar → Tabla dinámica** → arrastra `region` a filas e `ingreso` a valores.

**Entregable de la sesión:** las 6 respuestas con su fórmula o tabla dinámica.

---

## Sesión 5 (1 h) — Insights y publicación

1. Escribe **5 insights** en tu bitácora. Cada uno debe tener:
   - Un número.
   - Una interpretación.
   - Una recomendación.
   - Ejemplo: “La Región Metropolitana genera el 42% del ingreso; recomiendo concentrar ahí la campaña de marzo”.
2. Crea el repositorio `hola-datos` en GitHub.
3. Sube estos archivos:
   - `ventas_mini.csv`
   - `analisis.xlsx` o el enlace a tu Google Sheet
   - `README.md`
   - `bitacora.md`
4. Tu `README.md` debe tener:
   - Título.
   - De qué trata el dataset.
   - 5 insights.
   - Qué aprendiste.
   - Cómo abrir el archivo.

**Si GitHub te complica:** usa el botón **Add file → Upload files** en la web. No necesitas instalar Git todavía.

**Entregable de la semana:** repo `hola-datos` publicado con README.

---

## Checklist de la semana

- [ ] Tengo cuenta de GitHub.
- [ ] Abrí el CSV y entendí filas, columnas y tipos de dato.
- [ ] Calculé el ingreso con una fórmula.
- [ ] Usé `SUMA`, `PROMEDIO`, `CONTAR`, `MAX`, `MIN`.
- [ ] Filtré por estado y comparé resultados.
- [ ] Respondí las 6 preguntas de negocio.
- [ ] Escribí 5 insights con números.
- [ ] Publiqué el repo `hola-datos`.

---

## Verificación de las 6 preguntas

Con `estado = completado` (36 pedidos), deberías obtener aproximadamente:

1. Ingreso total: **CLP 24.950.000**
2. Región con más ingreso: **Biobío, CLP 9.965.000**
3. Producto con más ingreso: **Notebook, CLP 14.300.000**
4. Vendedor con más ingreso: **Carla, CLP 8.455.000**
5. Ticket promedio: **CLP 693.056**
6. Pedidos devueltos: **4 de 40 = 10%**

Si tus números no coinciden, revisa:
- Que filtraste solo `completado`.
- Que el ingreso es `unidades × precio_unitario`.
- Que no arrastraste mal la fórmula.
- Que el separador de miles no cambió el valor.

---

## Soluciones de matemáticas

1. 15% de 80.000 = **12.000**
2. 120.000 + 8% = **129.600**
3. 250.000 − 20% = **200.000**
4. 30/120 = **25%**
5. 25% de 4.000.000 = **1.000.000**
6. (100.000 + 200.000 + 300.000) / 3 = **200.000**

---

## Si te sobra tiempo

- Khan Academy en español: “Aritmética” → porcentajes y fracciones (20 min).
- Mira un video de 10 minutos sobre “tablas dinámicas desde cero”.
- Escribe en LinkedIn: “Empecé a aprender análisis de datos. Esta semana aprendí X”. Sin miedo.

---

## Qué viene la próxima semana

Fórmulas más potentes (`SI`, `BUSCARV`/`XLOOKUP`, `SUMAR.SI`), tablas dinámicas y limpieza de datos. No avances hasta completar el checklist.




