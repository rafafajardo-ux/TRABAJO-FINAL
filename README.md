# PFI — Producción anual y diaria de las Reservas 1P de Colombia y regalías esperadas (WTI y Brent)

Proyecto Final Integrador con metodología **CRISP-DM**. Modelos supervisados (árbol de decisión, regresión lineal, red neuronal y ensambles de árboles)
entrenados con la producción real por campo 2023-2026 y el perfil de Reservas 1P/2P/3P; aprendizaje no supervisado (segmentos de campos); aplicativo local.

Integrantes: Rafael Fajardo Moreno, Sonia Catalina Martinez Herrera y Laura Marcela Garnica Tapia

| Archivo | Qué es |
|---|---|
| `cuaderno_PFI.ipynb` | Análisis completo y reproducible (semilla 42). Genera `artefactos/` y `ficha_datos.md`. |
| `app/app.py` | Aplicativo Streamlit (consulta por año, desagregación, WTI/Brent, regalías). |
| `iniciar_app.command` | Doble clic en macOS: prepara el entorno y abre http://localhost:8501. |
| `informe_PFI`, `resumen_ejecutivo_EN`, `guia_PFI` | Documentos en Word y PDF. |
| `anexo_A_enfoque.md` | Anexo A: enfoque del aplicativo (producción y regalías solo con desarrollo de Reservas 1P, WTI y Brent). |
| `anexo_B_datos_reales.md` | Anexo B: datos reales del IRR 2024, anonimización y medidas de acceso. |
| `guia_sustentacion.html` / `.pdf` | Guía para preparar la sustentación: estructura en cuatro momentos, guion de 10 diapositivas y preguntas del jurado. |
| `presentacion_sustentacion.pdf` | Diapositivas de la sustentación: 10 diapositivas en cuatro momentos más 7 anexos. |
| `declaracion_IA.md` | Declaración de uso de inteligencia artificial (Claude Opus 5.5, Anthropic). |
| `datos_crudos/` | Excel original y precios mensuales EIA. |

Repositorio: https://github.com/rafafajardo-ux/TRABAJO-FINAL

**Aplicativo en línea:** https://rafafajardo-ux.github.io/TRABAJO-FINAL/ (la primera carga tarda unos 30 segundos; pide aceptar los términos y la contraseña).

## Uso

```bash
python3 -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
jupyter nbconvert --to notebook --execute cuaderno_PFI.ipynb --inplace   # opcional: regenera artefactos
streamlit run app/app.py
```

## Términos y condiciones

Los datos son de **carácter reservado** y tienen un **único uso académico**, en el marco de la Especialización en Machine Learning de la
Universidad EAN (2026). **Está prohibido el uso, la distribución, la copia o la mejora, total o parcial.** Solo se tiene en cuenta el pronóstico de
desarrollo de reservas del IRR 2024, sin contemplar la migración de reservas 2P y 3P ni la evolución de recursos contingentes. El aplicativo pide
aceptar estos términos antes de ingresar.

Identidad visual: paleta de www.rafaelfajardomoreno.com y letra Arial Narrow (con la equivalente libre `app/static/PFINarrow-*.ttf`, derivada de
Liberation Sans bajo licencia SIL OFL, si Arial Narrow no está instalada).

## Acceso y datos anonimizados

- El aplicativo pide aceptar los términos y condiciones y, después, una **contraseña**. Solicítela a **rafajard53009@universidadean.edu.co**.
  El código solo guarda la huella PBKDF2-SHA256 de la contraseña, no la contraseña.
- Como el repositorio es público, en `datos_crudos/` los nombres de los campos están anonimizados (`Campo_001` a `Campo_397`) y también los de los
  contratos (`Contrato_001` a `Contrato_135`). La numeración sigue el orden alfabético original, por lo que los resultados son idénticos a los obtenidos
  con los nombres reales. La tabla de correspondencia no se publica.
