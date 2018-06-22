# Proyecto Servicios - Fase Producto en crecimiento

**Sinopsis**: Nuestra startup está teniendo exito como sistema y así mismo hemos de necesitar de nuevos requerimientos para llegar a la mayor cantidad de clientes posible.

## Análisis de requerimientos:

**Criterios de exito:**

+ Brindar con nuestro servicio a empresas clientes estabilidad y control de costos de las prestaciones de servicios que se necesiten.

+ Se tiene una visión en el circulo de empresas prestadoras una visión de crecimiento de sus servicios.

## Historias de usuario:

+ El empresario cliente x quiere llevar control de sus finanzas mediante el reporte de gastos en servicios.

+ El empresario cliente y necesita que halla un grupo de profesionales preferidos para nunca perder la disponibilidad de nuestro servicio.

+ El empresario prestador x quiere medir el redimiento de sus profesionales.

+ El empresario prestador y quiere posicionarse mejor en el mercado para obtener más clientes

## Requerimientos:

+ **Reportes**
  
    Gastos por período, por el tipo de servicio contratado, ingresos, horas trabajadas por el profesional por período y tipo de servicio prestado.

+ **Autorización**

    + Gestión de usuario: El tipo de empleado que va a tener la empresa.
    
    + Roles

    + Permisos asociado a accines del sistema

    + Posicionamiento y comunicación: Ranking de prestadores por evaluación, lista priorizada de prestadores por tipo de prestación.

## Riesgo

+ Las empresas clientes no tienen como extraer información del sistema debido a que estas manejan sus propia información.

+ Los juicios hechos por las misma empresas prestadoras de acuerdo con los fraudes.

## Restricciones

+ Cumplir con estándares de auditoría profesional para que nuestro software sea seguro.

+ Garantizar la privacidad de datos de consumo

Con todo esto se decide que el estilo arquitectónico en la estructura cliente servidor pasa su transacciones en lote secuencial a los reportes teniendo en 