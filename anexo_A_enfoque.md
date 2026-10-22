# Anexo A. Enfoque del aplicativo

**Proyecto Final Integrador (PFI):** Producción anual y diaria de las Reservas 1P de Colombia y regalías esperadas según WTI y Brent
**Integrantes:** Rafael Fajardo Moreno, Sonia Catalina Martinez Herrera y Laura Marcela Garnica Tapia · Especialización en Machine Learning, Universidad EAN (2026)

## Qué hace el aplicativo

El aplicativo ayuda a **pronosticar el comportamiento de la producción esperada de petróleo** y **las regalías que se percibirían si solo se
contemplara el desarrollo de las Reservas Probadas (1P)**. Presenta las regalías con los dos indicadores de referencia, **WTI y Brent**, y ambos
precios están pronosticados para los años futuros.

## Cómo lo hace

1. **Producción.** Un modelo de aprendizaje automático (Random Forest, elegido frente a árboles de decisión, regresión lineal y redes neuronales)
   pronostica la producción de cada campo a partir de su producción real y de su perfil de Reservas 1P. 2023 a 2025 son datos reales; 2026 combina
   el dato real de enero a junio con el pronóstico de julio a diciembre; desde 2027 todo es pronóstico.
2. **Tope en la 1P.** Desde 2027 la producción pronosticada de un campo nunca supera su Reserva 1P del año. Si un campo ya no tiene Reservas 1P, no
   se pronostica y el aplicativo informa hasta qué año estuvieron proyectadas.
3. **Regalías.** Se calculan con la escala de la Ley 756 de 2002 en dos versiones: proyectadas con la Reserva 1P y a partir de la producción
   pronosticada. Se expresan en barriles y en dólares.
4. **Precios WTI y Brent.** Para 2023 a 2025, promedios anuales observados (EIA); para 2026, promedio de enero a septiembre; para 2027, la proyección
   de la EIA (Short-Term Energy Outlook, octubre de 2026); desde 2028, supuesto constante. Los precios se pueden editar en el aplicativo.

## Precios de referencia (USD por barril)

| Año | Brent | WTI | Tipo |
|---|---:|---:|---|
| 2024 | 80,53 | 76,55 | Observado |
| 2025 | 69,10 | 65,46 | Observado |
| 2026 | 93,27 | 84,98 | Observado parcial (enero-septiembre) |
| 2027 | 84,00 | 79,85 | Pronóstico EIA STEO |
| 2028 en adelante | 84,00 | 79,85 | Supuesto constante |

## Resultado para el total país (regalías a partir de la producción)

| Año | Miles de barriles por día | Regalías (millones de bl) | USD millones a WTI | USD millones a Brent |
|---|---:|---:|---:|---:|
| 2025 (real) | 746 | 28,8 | 1.885 | 1.990 |
| 2026 | 724 | 27,9 | 2.368 | 2.599 |
| 2027 | 535 | 20,2 | 1.615 | 1.699 |
| 2030 | 328 | 11,7 | 936 | 985 |
| 2035 | 123 | 4,1 | 326 | 343 |

## Alcance

El escenario considera **solo el desarrollo de las Reservas 1P del IRR 2024**. No incluye la migración de reservas probables (2P) y posibles (3P)
a probadas ni la evolución de los recursos contingentes. Por eso la trayectoria posterior a 2027 debe leerse como un **piso conservador** de la
producción y de las regalías, no como la producción total esperada del país.

## Enlaces

- Aplicativo en línea: https://rafafajardo-ux.github.io/TRABAJO-FINAL/
- Repositorio: https://github.com/rafafajardo-ux/TRABAJO-FINAL
