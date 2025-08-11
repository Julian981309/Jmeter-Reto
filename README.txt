# Prueba de Carga JMeter - Servicio de Login

## Descripción
Este proyecto contiene la implementación de una prueba de carga para el servicio de login, basada en un CURL provisto. La prueba utiliza un archivo CSV para parametrizar usuarios y contraseñas y busca validar el rendimiento bajo carga.

## Tecnologías y versiones utilizadas
- Apache JMeter 5.6.3
- Java 17 (JDK)
- Git 2.40.1
- Sistema Operativo: Windows 10 / Linux Ubuntu 20.04

## Contenido del repositorio
- Summary Report.jmx         -> Script de prueba JMeter configurado
- credenciales.csv           -> Archivo CSV con datos de usuario y contraseña
- readme.txt                 -> Instrucciones de uso
- conclusiones.txt           -> Hallazgos y conclusiones

## Instrucciones paso a paso para ejecutar la prueba

1. Clonar el repositorio

2. Abrir Apache JMeter (versión 5.6.3) en tu equipo.

3. Cargar el script `login_test.jmx` en JMeter.

4. Verificar que el archivo `users.csv` esté en la ruta correcta dentro del proyecto (ruta configurada en el CSV Data Set Config).

5. Configurar los parámetros de carga:
- Número de hilos (usuarios concurrentes)
- Ramp-up (tiempo de subida)
- Loop Count (cantidad de iteraciones)

Para alcanzar al menos 20 TPS (transacciones por segundo), ajusta los usuarios y ramp-up en el Thread Group.

6. Ejecutar la prueba desde JMeter.

7. Al finalizar, revisar los resultados en los listeners configurados (Summary Report, View Results Tree, Aggregate Report).

8. Analizar los reportes generados en la carpeta `report/`.

## Validaciones que debe cumplir la prueba
- Tiempo máximo de respuesta: 1.5 segundos
- Tasa de error menor al 3%
- Al menos 20 TPS (transacciones por segundo)
