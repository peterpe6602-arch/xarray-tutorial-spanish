# Introducción a xarray

Este es un notebook utilizado como introducción al paquete de python [xarray](https://docs.xarray.dev/en/stable/):

> Xarray introduce etiquetas en la forma de dimensiones, coordenadas y atributos en matrices sin procesar similar a las de Numpy, lo que permite una experiencia de desarrollo más intuitiva, más concisa y menos propensa a errores. El paquete incluye una gran librería en crecimiento, de funciones independientes de dominio (domain-agnostic) para analisis avanzados y visualización con estas estructuras de datos.
> Xarray fue inspirado por y se basa fuertemente en pandas, el popular paquete de análisis de datos enfocado en datos tabulares etiquetados. Está particularmente adaptado para trabajar con netCDF, los cuáles fueron la fuente de modelos de datos de Xarray, y se integra estrechamente con dask para computación paralela.

Estos notebook son una reinterpretación en español de la serie "introduction_to_xarray" del usuario [
coecms-training ](https://github.com/coecms-training/introduction_to_xarray/tree/master). Cuyo formato opcional del turorial se encuentra en el canal de youtube [CLEX CMS youtube channel](https://www.youtube.com/channel/UCSmoK6oWV9O0Hmyt9UdDNsQ)

Para los datos se utilizo, la base da datos Madrigal, el cuál contempla datos ionosféricos en formato netCDF4. Utilizandose los datos específicos del día de tormeta geomagnética del 16-18 de mayo del 2025, obtenidos del Radio Observatorio de Jicamarca. El fin no es hacer una análisis del evento, sino hacer una breve exploración en función de las herramientas de xarray.

<table style="width:100%; border-collapse: collapse;">
  <thead>
    <tr style="background-color: #f2f2f2;">
      <th style="border: 1px solid #dddddd; text-align: left; padding: 8px;">Archivo</th>
      <th style="border: 1px solid #dddddd; text-align: left; padding: 8px;">Fecha</th>
      <th style="border: 1px solid #dddddd; text-align: left; padding: 8px;">Observatorio</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">jro20250516_132000.nc</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">16/05/2025</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">JRO</td>
    </tr>
    <tr>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">jro20250517_050004</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">17/05/2025</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">JRO</td>
    </tr>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">jro20250518_050004</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">18/05/2025</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">JRO</td>
    </tr>
    <tr>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">jro20250519_050005.nc</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">19/05/2025</td>
      <td style="border: 1px solid #dddddd; text-align: left; padding: 8px;">JRO</td>
    </tr>
  </tbody>
</table>


Esta serie consiste de notebooks de igual manera a [aidanheerdegen](https://github.com/coecms-training/introduction_to_xarray/tree/master) divide los temas en:

1. Lectura de datos y metadatos de un archivo netCDF dentro de un dataset xarray
2. Separación de un dataset por tiempo y espacio
3. Ploteo
4. Cálculo de métricas (e.g. promedio, máximo)
5. Masking
6. Apertura de multiples archivos como un solo dataset
7. Guardado de datasets a un netCDF
