# Ejemplo Documentación 
![Tinkercad](./img/ArduinoTinkercad.jpg)


## Integrantes 
- Lautaro Torres Distefano


## Proyecto: Montacarga.
![Tinkercad](./img/montacarga proyecto.png)



## Vista esquematica: Montacarga.
![Tinkercad](./img/diagrama.png)

## Descripción
Este trabajo es un modelo de montacarga funcional para un hospital.Implementa un sistema que puede recibir ordenes de subir, bajar o pausar
desde diferentes pisos y muestra el estado actual del montacargas en el display 7 segmentos.

## Función principal
Esta funcion funciona a la par de 3 botones cada uno con una funcion especifica como lo son:Subir, bajar y frenar.

void loop()
{
  Serial.println("Estas en el piso: ");
  Serial.println(piso);
  mostrar_piso();
  lectura_subida = digitalRead(2);
  lectura_bajada = digitalRead(3);
  lectura_pausado = digitalRead(4);
  
  if(lectura_pausado == HIGH)
  {
    frenar_montacarga();
  }
  
  if(lectura_subida == HIGH || flag_subir == true)
  {
    subir_piso();
  }
  
  if(lectura_bajada == HIGH || flag_bajar == true)
  {
    bajar_piso();
  }
}

~~~ C++ (lenguaje en el que esta escrito)
~~~ 

## :robot: Link al proyecto
- [Proyecto](https://www.tinkercad.com/things/8p1YMZTkh9U-bodacious-fulffy/editel?sharecode=WCmV9uyg2jmYj6c_9tedtd7QnhAr0YYr8h_rPs0T7Ks)
---
