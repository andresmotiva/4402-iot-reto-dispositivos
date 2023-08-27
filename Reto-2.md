# Reto 2: Capa de Dispositivos

`BRAYAN SEBASTIÁN HERNÁNDEZ BARRERA`
`ANDRÉS RAMÍREZ RESTREPO`



#### Componentes Utilizados:

- ESP8266 NodeMCU
- Sensor de Temperatura y Humedad DHT11
- Fotoresistor GL5516 (Sensor de Luz)

#### Requisitos:

1. **Caracterización de la Intensidad Lumínica:**
   La intensidad lumínica se monitorea utilizando el fotoresistor GL5516. La resistencia del sensor cambia con la intensidad de la luz, proporcionando una señal analógica para la medición.

2. **Selección del Sensor:**
   Se elige el fotoresistor GL5516 para monitorear la intensidad lumínica debido a su capacidad para proporcionar lecturas de resistencia variable proporcionales a los niveles de luz.

3. **Adición del sensor a la placa:**
   - El sensor de luz se conecta a un pin de entrada analógica (por ejemplo, A0) en el NodeMCU.
   - Se lee el valor analógico del fotoresistor GL5516 y los datos de temperatura y humedad proporcionados por el Sensor de Temperatura y Humedad DHT11.
   - Los datos se envían a los temas MQTT "temperatura," "humedad" y "luminosidad."

#### Ejemplo de Salida:

Ejemplo de mensaje JSON enviado a los temas MQTT:
```json
{
  "temperatura": <float>,
  "humedad": <float>,
  "luz": <valor_analógico>
}
