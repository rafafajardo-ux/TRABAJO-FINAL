# Anexo B. Datos reales y medidas de protección

**Proyecto Final Integrador (PFI):** Producción anual y diaria de las Reservas 1P de Colombia y regalías esperadas según WTI y Brent
**Integrantes:** Rafael Fajardo Moreno, Sonia Catalina Martinez Herrera y Laura Marcela Garnica Tapia · Especialización en Machine Learning, Universidad EAN (2026)

## Origen de los datos

Los datos del proyecto son **datos reales**: el pronóstico de desarrollo de Reservas Probadas (1P), Probables (2P) y Posibles (3P) por campo del
**Informe de Recursos y Reservas (IRR) 2024**, con corte al 31 de diciembre de 2023, y la producción fiscalizada de petróleo por campo de 2023 a
junio de 2026. Están en `datos_crudos/1_ML_OIL_produccion_reservas.xlsx`.

## Anonimización

Por su **carácter reservado**, los datos se anonimizaron antes de publicar el repositorio:

- Los nombres de los **397 campos** se reemplazaron por códigos `Campo_001` a `Campo_397`, con el mismo código para un campo en las cuatro hojas
  del archivo.
- Los nombres de los **135 contratos** se reemplazaron por `Contrato_001` a `Contrato_135`, porque 41 de ellos repetían el nombre del campo.
- La numeración sigue el orden alfabético original. Así, todos los resultados del modelo son idénticos a los obtenidos con los nombres reales.
- La tabla de correspondencia entre nombres reales y códigos **no se publica**: se conserva aparte, fuera del repositorio y del aplicativo.
- Se conservan las operadoras, los departamentos y los municipios, necesarios para las desagregaciones que pide el ejercicio.

## Precauciones de acceso y uso

1. **Declaración de uso (términos y condiciones).** Al abrir el aplicativo, la persona debe leer y aceptar los términos y condiciones antes de
   continuar. Establecen que los datos son reservados, que su único uso es académico en la Especialización en Machine Learning de la Universidad EAN
   (2026) y que está prohibido su uso, distribución, copia o mejora, total o parcial. Sin aceptarlos no es posible seguir.
2. **Contraseña única de acceso.** Después de aceptar, el aplicativo pide una contraseña única, que **debe solicitarse a
   rafajard53009@universidadean.edu.co**. La contraseña no está escrita en el código ni en los documentos: el aplicativo solo guarda su huella
   cifrada (PBKDF2-SHA256) y bloquea el acceso durante 60 segundos tras cinco intentos fallidos.
3. **Declaración de uso de inteligencia artificial.** El archivo `declaracion_IA.md` informa cómo se usó la inteligencia artificial en el ejercicio.

## Enlaces

- Aplicativo en línea (con términos y contraseña): https://rafafajardo-ux.github.io/TRABAJO-FINAL/
- Repositorio: https://github.com/rafafajardo-ux/TRABAJO-FINAL
