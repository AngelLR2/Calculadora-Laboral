# Calculadora de Prestaciones Laborales

Herramienta web para calcular prestaciones laborales en casos de despido. Funciona completamente en el navegador: no requiere servidor, instalación ni conexión a bases de datos.

## Prestaciones que calcula

1. Indemnización constitucional (90 días, ajustable)
2. Aguinaldo
3. Vacaciones
4. Prima vacacional (25 %)
5. Prima de antigüedad (con salario tope)
6. 20 días por año laborado

Cada prestación tiene un interruptor **Incluir**: al apagarla desaparece de la tabla y no se suma al total.

También permite calcular el Salario Diario Integrado (SDI) y elegir, por prestación, si se calcula con salario diario o con SDI.

## Funciones

- Cálculo automático del tiempo laborado a partir de las fechas de ingreso y baja (ajustable a mano).
- Campo de observaciones (expediente, notas del caso).
- Impresión / PDF con el logo en el encabezado.
- Historial de cálculos con búsqueda, exportación a CSV y respaldo en JSON (exportar e importar).

## Uso

### En línea (GitHub Pages)

1. Sube estos archivos a un repositorio.
2. Ve a **Settings → Pages**.
3. En **Source** elige **Deploy from a branch**, rama `main` y carpeta `/ (root)`.
4. Guarda. En uno o dos minutos la calculadora estará en:
   `https://TU-USUARIO.github.io/NOMBRE-DEL-REPOSITORIO/`

### Local

Descarga `index.html` y ábrelo con cualquier navegador.

## Privacidad

El historial se guarda en el `localStorage` del navegador de quien usa la calculadora. **Los datos de los clientes no se suben a GitHub ni a ningún servidor.** Por lo mismo:

- El historial es propio de cada navegador y equipo.
- Si se borran los datos del navegador, se pierde el historial: usa **Exportar JSON** para respaldarlo.
- Los respaldos (`.json`, `.csv`) están en `.gitignore` para que no se suban por accidente al repositorio.

## Mantenimiento

- El **salario tope de la prima de antigüedad** (`SALARIO_TOPE`, actualmente `630.08`) depende del salario mínimo vigente. Actualízalo cada año en la parte superior del script de `index.html`.
- La tabla de días de vacaciones (`TABLA_VACACIONES`) sigue la Ley Federal del Trabajo vigente.

## Aviso

Esta herramienta es un apoyo de cálculo. Los resultados deben revisarse por el abogado responsable antes de utilizarse en una demanda, convenio o negociación.
