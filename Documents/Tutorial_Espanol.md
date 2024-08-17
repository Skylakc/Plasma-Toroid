# Instrucciones de bricolaje del toroide de plasma

Este documento fue actualizado el 22 de julio de 2024.

Autor: *Tienda de Magia del Callejón Diagon*

Todos los componentes utilizados en este documento se pueden encontrar en la tienda de Aliexpress ***Tienda de Magia del Callejón Diagon***. 

[Principio del toroide de plasma](https://www.youtube.com/watch?v=GbMAvn7nRWo)

[Video de demostración del producto terminado 1](https://www.bilibili.com/video/BV1Lm411z7tf)

[Video de demostración del producto terminado 2](https://www.bilibili.com/video/BV12f421o7rf) 

[Plataforma de código abierto LCEDA](https://oshwhub.com/skylake/plasmatoroid-drive-circuit)

Grupo de telegram de tecnología de código abierto del toroide de plasma:
https://t.me/+eRFEajIG6_RiMTY1

<img src=../imgs/imgs_24_7_22\cover.jpg width=74% />

## Aviso de derechos de autor©

Este documento es solo para aprendizaje personal y fabricación de toroides de plasma. Sin el consentimiento del autor, nadie puede modificar, republicar o distribuir el contenido de este documento. Está estrictamente prohibido utilizar este documento para cualquier actividad comercial.

## Descargo de responsabilidad  
Antes de usar este documento para hacer un toroide de plasma, lea atentamente las siguientes advertencias de seguridad importantes y descargos de responsabilidad. El uso de este documento significa que comprende y acepta completamente los siguientes términos:
- Peligros de los toroides de plasma: La botella de vidrio generará altas temperaturas cuando el toroide de plasma esté funcionando, y existe el riesgo de quemaduras a baja temperatura. Nunca se recomienda tocar directamente la botella de vidrio en funcionamiento con las manos para evitar quemaduras.
- Advertencia de campo magnético: El toroide de plasma generará un fuerte campo magnético durante el funcionamiento. Para las personas que usan marcapasos y otros dispositivos médicos, los campos magnéticos fuertes pueden afectar el funcionamiento normal de los dispositivos. Recomendamos que estos usuarios se mantengan alejados de los toroides de plasma en funcionamiento para evitar posibles riesgos para la salud.  
- Riesgo de alto voltaje: El circuito de accionamiento del toroide de plasma generará alto voltaje durante el funcionamiento. El alto voltaje representa un peligro de descarga eléctrica o quemaduras. No toque ningún componente, incluida la bobina primaria, mientras el circuito esté funcionando para evitar descargas eléctricas o quemaduras.
- Temperatura de los componentes: Tenga en cuenta que algunos componentes del circuito pueden calentarse mucho durante el funcionamiento, lo que puede causar quemaduras. Cuando el dispositivo esté funcionando, especialmente después de funcionar durante mucho tiempo, no toque estos componentes.  
- Interferencia electromagnética: El toroide de plasma emitirá ondas electromagnéticas alrededor de 10 MHz cuando esté funcionando. Esta banda no dañará el cuerpo humano, pero puede interferir con algunos dispositivos electrónicos que operan en esta banda, como paneles táctiles y lectores de tarjetas. Mantenga estos dispositivos alejados del circuito de accionamiento en funcionamiento.

El uso de este documento significa que comprende y acepta asumir los riesgos de uso. El autor no se hace responsable de los daños directos o indirectos causados por no seguir las pautas de seguridad.

¡Hágalo usted mismo con precaución, la seguridad es lo primero!

## Análisis del principio de funcionamiento de los toroides de plasma

- Fenómeno de descarga luminiscente: Bajo ciertas condiciones, el gas experimentará una descarga luminiscente bajo la acción de un fuerte campo eléctrico. En este proceso, los electrones de las moléculas de gas se estimulan y saltan a órbitas de nivel de energía más alto. Como estos electrones son inestables en el estado de alta energía, volverán espontáneamente a la órbita original de baja energía mientras liberan fotones correspondientes a la diferencia de energía de acuerdo con la ley de conservación de la energía. Este fenómeno se llama descarga luminiscente y se aplica a dispositivos como luces de neón. El proceso de luminiscencia de los toroides de plasma es similar a esto.

- Propiedades del plasma: Además de los estados comunes de sólido, líquido y gaseoso, el plasma es otro estado de la materia que existe en el universo, y las llamas son un ejemplo que contiene plasma. Cuando el gas se ve afectado por altas temperaturas, las colisiones entre moléculas harán que los electrones exteriores escapen de sus órbitas, formando un plasma compuesto de partículas cargadas. Esta mezcla de iones cargados tiene conductividad eléctrica.

- Generación de campo electromagnético toroidal: Al pasar una corriente alterna de alta frecuencia a través de una bobina toroidal, se puede derivar de las ecuaciones de Maxwell que la distribución del campo eléctrico a su alrededor es toroidal. Usamos un circuito oscilador Clase E autoexcitado para generar una corriente alterna con una frecuencia de aproximadamente 10 MHz. 

- Proceso de generación del toroide de plasma: En una botella de vidrio esférica llena de gas xenón a baja presión, el gas xenón se ioniza bajo la acción de un fuerte campo eléctrico para formar un plasma. Estos plasmas de gas xenón conductores forman una estructura toroidal estable bajo la influencia de un campo eléctrico toroidal externo. En el plasma, las colisiones de partículas cargadas producen una descarga luminiscente, que emite una luz violeta pálida, haciendo visible el toroide de plasma.

**Cuando use y demuestre el toroide de plasma, asegúrese de comprender su principio de funcionamiento y las medidas de seguridad correspondientes para garantizar la seguridad de los usuarios.**

## Preparación de materiales

<img src=../imgs/imgs_24_4_13/compress/FullComponents.jpg width=88% />

- Botella de vidrio de 80 mm llena de gas xenón (disponible en la tienda de Aliexpress **Tienda de Magia del Callejón Diagon**, las esferas de vidrio más grandes no se pueden instalar en el soporte de este proyecto)  
- Alambre esmaltado de 1.2 mm - para enrollar bobinas
- Inductor de anillo negro 10uH
- Placa de circuito impreso PCB (se puede hacer usando los archivos en la carpeta de hardware)
- Soporte de bobina, incluida la placa base y cinco piezas de soporte  
- Disipador de calor y ventilador
- MOSFET IRFP260N
- Almohadilla de silicona para disipador de calor MOSFET
- Potenciómetro 1k
- Resistencia 1k * 3
- Resistencia 1.8k, 3k  
- Condensador SMD 100pf * 4
- Condensador SMD 4,7nF * 2
- TVS 15V P6KE15CA
- Diodo regulador de voltaje 9.1V
- Condensador electrolítico de filtro de entrada 63V 220uf
- Interruptor de palanca  
- Bloque de terminales verdes - para conectar la bobina
- Conector de ventilador blanco
- Interfaz de alimentación CC
- Diodo emisor de luz
- Tornillos y columnas de nylon
- Cerámica piezoeléctrica extraída de un encendedor (para encendido inicial)
- Módulo limitador de corriente XL4015 (este módulo no es necesario si tiene una fuente de alimentación ajustable)
- Adaptador de corriente de 24V (4A o superior, o puede usar una fuente de alimentación ajustable)

## Tutorial de producción
Dificultad ★★★☆☆

### Herramientas
- Multímetro
- Soldador  
- Alambre de soldadura
- Cuchillo multiusos
- Alicates diagonales
- Juego de destornilladores hexagonales
- Pinzas (para soldar condensadores SMD)

<img src=../imgs/tools.jpg width=50% />

### Pasos
- Prepare los cinco soportes de bobina, insértelos en la base, caliente el soldador y suéldelos en su lugar con soldadura. Intente asegurarse de que los soportes estén perpendiculares a la placa base. (Las cinco piezas del soporte de la bobina necesitan algo de fuerza para encajar)

<img src=../imgs/imgs_24_4_13/compress/Coil1.jpg width=45% /> <img src=../imgs/imgs_24_4_13/compress/Coil2.jpg width=45% />

- Doble el cable esmaltado de acuerdo con el diámetro del marco de la bobina, no enderece el cable esmaltado, mantener el cable esmaltado doblado ayuda con el enhebrado, una vez enderezado no se puede enhebrar.

<img src=../imgs/imgs_24_4_13/compress/Coil3.jpg width=80% />

- Enhebre el cable esmaltado a través de los pequeños agujeros de arriba hacia abajo, un total de cuatro vueltas. Los agujeros son relativamente pequeños y el enhebrado se puede hacer empujando y tirando.
  
<img src=../imgs/imgs_24_4_13/compress/Coil4.jpg width=32% /> 
<img src=../imgs/imgs_24_4_13/compress/Coil5.jpg width=32% />
<img src=../imgs/imgs_24_4_13/compress/Coil6.jpg width=32% />


- Haga una fuente de alimentación con protección de limitación de corriente (este paso se puede omitir si ya tiene una fuente de alimentación ajustable), prepare una fuente de alimentación de 24V y un módulo limitador de corriente XL4015, corte el cable de alimentación, conecte el módulo en serie en el medio, gire el potenciómetro para ajustar el voltaje de salida del módulo XL4015 en sentido horario hasta el final (habrá un sonido de clic cuando se gira hasta el final), y gire el potenciómetro de limitación de corriente a la posición de 3.5A. El método para determinar la posición del potenciómetro limitador de corriente es: configure el multímetro en el rango de corriente de 10A, inserte los cables de prueba en el orificio de 10A, toque los dos cables de prueba en la salida (en este momento, la salida está en cortocircuito, puede haber chispas eléctricas pero está bien), el valor que se muestra en el multímetro es el valor de límite de corriente del módulo limitador de corriente. Tenga en cuenta que el uso de una fuente de alimentación sin limitación de corriente puede quemar fácilmente el MOSFET, debe conectar el módulo XL4015 en serie antes de conectar la alimentación. Si ya tiene una fuente de alimentación ajustable, puede omitir este paso. En la siguiente imagen, el potenciómetro en el lado izquierdo del módulo es para ajustar el voltaje de salida, y el potenciómetro en el lado derecho es para ajustar el límite de corriente. Girar en sentido horario aumenta el valor.
  
- Si está utilizando una fuente de alimentación ajustable, utilice el modo de limitación de corriente (CC), ajuste el voltaje de salida a 24V y el límite de corriente a 3.5A.


<img src=../imgs/imgs_24_3_1/XL4015.jpg width=64% />
<img src=../imgs/imgs_24_3_1/power_source.jpg width=32% />


- Inserte los componentes en la placa de circuito según su tipo (no instale el MOSFET todavía). Para facilitar la soldadura, puede doblar ligeramente las patillas para fijarlas. Tenga en cuenta que **el conector del ventilador debe montarse en la parte posterior del PCB, y también se debe soldar un diodo emisor de luz y una resistencia de 1k en el PCB del soporte de la bobina**.
Las posiciones de instalación de cada componente se muestran en la tabla a continuación.

| Nombre del componente   | Posición de instalación      |
|-------------------------|------------------------------|
| Resistencia 1k * 3      | R1, R4, PCB soporte de bobina|
| Diodo emisor de luz     | PCB soporte de bobina        | 
| Resistencia 3k          | R2                           |
| Resistencia 1.8k        | R3                           |
| Diodo regulador voltaje | D2                           |
| TVS (negro)             | D1                           |
| Bloque terminal verde   | P1                           |
| Bloque terminal blanco  | Q3 (montado en la parte posterior)|
| Condensador electrolítico 220uf| C5                   |
| Condensador 100pf * 4   | C1, C2, C3, C4               |
| Condensador 4.7nf * 2   | C6, C7                       |
| Inductor 10uH           | L1                           |
| IRFP260                 | Q1 (no instale esto todavía) |
| Interruptor             |                              |
| Conector de alimentación DC5525 negro|               |   
| Potenciómetro B1K simple|                             |

- Se recomienda soldar primero los componentes más cortos, luego los componentes más altos, como soldar primero los condensadores SMD, resistencias, reguladores de voltaje, bloques de terminales, etc., y finalmente soldar los condensadores electrolíticos y el interruptor. Si no tiene experiencia en soldadura, asegúrese de buscar tutoriales de soldadura en Bilibili para aprender primero. Según estadísticas históricas, el 60% de las personas que tuvieron problemas después de fabricarlo se debió a un mal contacto entre los componentes y el PCB causado por no dominar el método de soldadura correcto.
  
  > Identificación de resistencias
  > - La resistencia de 1k tiene una línea marrón   
  > - La resistencia de 1.8k tiene una línea marrón y una línea gris
  > - La resistencia de 3k tiene una línea naranja
  > Si realmente no puede distinguirlas, simplemente mida con un multímetro ^_^

  > Identificación de condensadores
  > - Los condensadores de 4.7nF son relativamente más delgados
  > - Los condensadores de 220pF/100pF son relativamente más gruesos
  > - Para los condensadores resonantes, puede elegir dos de 220pF o cuatro de 100pF
  
  > Identificación de la dirección del diodo
  > - El TVS negro no es direccional
  > - El diodo regulador de voltaje rojo debe ser direccional, la línea negra en el diodo regulador de voltaje debe coincidir con la posición de la línea blanca en la serigrafía del PCB.

  > Puede que algunos amigos no sepan soldar componentes SMD, puedes buscar tutoriales de soldadura de componentes SMD en Youtube para aprender. En pocas palabras, soldar primero un lado para fijar el componente SMD y luego soldar el otro lado.
  
  > 【Cómo soldar SMD correctamente - Parte 1 / Tutorial de soldadura SMD - Youtube】 https://www.youtube.com/watch?v=EW9Y8rDm4kE

  > Asegúrese de prestar atención a la dirección del condensador electrolítico, soldarlo al revés puede causar un calentamiento intenso o incluso una explosión. La pata más larga del condensador electrolítico es el electrodo positivo y el lado con la marca de la raya es el electrodo negativo. Consulte la siguiente imagen para instalar correctamente el condensador electrolítico.

<img src=../imgs/imgs_24_7_22\assembled_front.jpg width=70% />

- Cuando suelde, **tenga cuidado con la alta temperatura del soldador para evitar quemaduras.**

- Después de soldar todos los componentes, corte las patillas. Intente asegurarse de que las juntas de soldadura estén llenas y sean suaves, y comience desde la raíz al quitar las patillas.

<img src=../imgs/imgs_24_4_13/assemble_back.jpg width=70% /> 

- Atornille columnas de cobre de 6 mm (o columnas de nylon de 6 mm) en los orificios para tornillos alrededor del disipador de calor.

<img src=../imgs/imgs_24_4_13/compress/Heatsink0.jpg width=60% />

- Instale el MOSFET. Coloque el lado del MOSFET con texto **hacia arriba**, acolche el otro lado con una almohadilla de silicona y fíjelo en el disipador de calor con tornillos, con las patillas **hacia abajo**. En este momento, las patillas de izquierda a derecha son los polos G, D y S respectivamente.

<img src=../imgs/imgs_24_4_13/compress/Heatsink1.jpg width=40% />

<img src=../imgs/imgs_24_4_13/compress/Heatsink2.jpg width=45% />

- Doble las patillas e insértelas en el PCB. **Primero alinee los orificios del PCB y el disipador de calor para asegurarse de que los cuatro tornillos se puedan apretar**, luego suelde el MOSFET.

<img src=../imgs/imgs_24_4_13/assemble_new.jpg width=60% />

- Fije el ventilador. La conexión de todas las capas se muestra en la figura a continuación. El flujo de aire del ventilador sopla hacia el disipador de calor (soplando hacia arriba).

<img src=../imgs/imgs_24_4_13/compress/Fan1.jpg width=30% />

<img src=../imgs/imgs_24_4_13/compress/Fan2.jpg width=30% />

<img src=../imgs/imgs_24_4_13/compress/Fan3.jpg width=30% />

- Use tornillos para montar el soporte de la bobina en la parte superior, con los dos cables orientados hacia el bloque de terminales verde de la bobina.

<img src=../imgs/imgs_24_4_13/compress/assemble3.jpg width=40% />
<img src=../imgs/imgs_24_4_13/compress/Assemble2.jpg width=48% />

- Corte el cable esmaltado adecuadamente para que se pueda insertar en el bloque de terminales.
- Use un cuchillo multiusos para raspar el esmalte en el extremo del cable para exponer el núcleo de cobre dentro del cable esmaltado.
- **Nota: ¡Asegúrese de raspar bien el esmalte en el extremo del cable, de lo contrario, un contacto deficiente puede impedir que funcione!**

<img src=../imgs/imgs_24_4_13/compress/Assemble1.jpg width=60% />

- Inserte los dos cables de la bobina en los pines 1 y 3 del bloque de terminales verde (el orificio del medio no se usa) e inserte el cable de alimentación del ventilador en la interfaz del ventilador en la parte posterior del PCB.

- Después de confirmar nuevamente que todas las piezas están conectadas correctamente, puede prepararse para encender o(*￣▽￣*)ブ

- Si está utilizando una fuente de alimentación ajustable, utilice el modo de limitación de corriente (CC), ajuste el voltaje de salida a 24 V y el límite de corriente a 3,5 A.
- Coloque la botella y asegúrese de que el potenciómetro esté en la posición máxima en sentido antihorario.

- Antes de encender, lea atentamente las instrucciones de seguridad:
  > Manténgase alejado de la bobina cuando el circuito esté funcionando, ya que la alta temperatura de la bobina puede causar quemaduras.
  
  > Puede girar la botella, pero la botella también se calentará. Tenga cuidado y mantenga las manos alejadas de la bobina (al menos a 1 cm de distancia) al girar la botella.
  
  > Puede girar el potenciómetro mientras el circuito esté funcionando, pero no sostenga la botella con una mano y toque el potenciómetro en el circuito con la otra mano, porque la electricidad estática de alto voltaje en la botella puede dañar el circuito.
  
  > El circuito se calentará. No se recomienda hacer funcionar el circuito durante mucho tiempo. Se recomienda trabajar continuamente durante no más de dos minutos.

  > Después del uso, recuerde apagar el interruptor y desconectar la fuente de alimentación.

- Después de asegurarse de que ha leído las instrucciones de seguridad, enchufe la fuente de alimentación y encienda el interruptor. En este momento, el ventilador debería comenzar a girar.

- Gire el potenciómetro en sentido horario. Cuando se gira aproximadamente hasta la mitad, el circuito comenzará a funcionar. Cuando el circuito comienza a funcionar, el LED junto a la bobina se encenderá. En este punto, use un encendedor para apuntar a la botella y haga clic en él para generar el toroide. Si el encendedor no logra generar el toroide, puede girar el potenciómetro un poco más en sentido horario y volver a intentarlo.

<img src=../imgs/imgs_24_3_1/excite.jpg width=40% />

<img src=../imgs/imgs_24_3_1/ring.jpg width=40% />

- A veces, su botella puede brillar en blanco sin generar un toroide (como se muestra a continuación). Ajustar la posición de la botella y volver a encenderla algunas veces generalmente lo soluciona.

<img src=../imgs/imgs_24_3_1/white.jpg width=40% />

- Después de generar el toroide, girar ligeramente el potenciómetro provocará algunos cambios en la forma del toroide. Si el toroide desaparece, volver a encenderlo lo generará nuevamente.

<img src=../imgs/imgs_24_4_13/Xe2.jpg width=70% />

### Diagrama de circuito de referencia
Dado que el hardware de este proyecto aún se está actualizando, el diagrama del circuito es solo de referencia. El circuito real debe basarse en el PCB.

<img src=../imgs/imgs_24_3_1/sch.jpg width=80% />

### Preguntas frecuentes
Si tiene alguna pregunta, únase al grupo de telegram: 
https://t.me/+eRFEajIG6_RiMTY1.

<img src=../imgs\tg.jpg width=30% />

Todos los desarrolladores del proyecto están en el grupo y puede obtener respuestas a la velocidad más rápida. (Intentamos responder todas sus preguntas dentro de las 24 horas).

#### Agradecimientos:
Tate McAluney