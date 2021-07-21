
## PRÁCTICA DE LABORATORIO 
## CARRERA: COMPUTACION 	
## ASIGNATURA: HIPERMEDIAL 
## NRO. PRÁCTICA: 	8
## TÍTULO PRÁCTICA:  Desarrollo de una aplicación de realidad virtual usando la herramienta Unity y desplegada en un dispositivo móvil Android. 
 
## OBJETIVO  
 
•	Experimenta con aplicaciones de realidad virtual. 
•	Experimenta con aplicaciones de realidad aumentada. 
•	Distingue la diferencia entre tecnologías de realidad virtual y realidad aumentada.  

## INSTRUCCIONES  	
Este proyecto es una oportunidad para que combine y practique todo lo que aprendió en el capítulo de Realidad Virtual. Creará una experiencia de realidad virtual totalmente interactiva en forma de laberinto. 

Esto le brinda la oportunidad de aplicar lo que ha aprendido con las secuencias de comandos para brindar una experiencia audiovisual completa. 
Crear la GVR Camera Rig 

Durante este paso, crearemos la cámara VR incluyendo el GvrEditorEmulator en la escena y configurando la cámara. 

1.	Agregue el objeto prefab GvrEditorEmulator a la escena. 

 ![1](https://user-images.githubusercontent.com/49033767/126409656-c260c978-6b2f-4ad2-b36c-6118dc0671d9.png)
 
2.	Convierta el objeto Main Camera en un elemento hijo del objeto GvrEditorEmulator. 

 ![2](https://user-images.githubusercontent.com/49033767/126409660-7e940f59-af54-4c68-b26a-a5136938e40c.png)
 
3.	Restablece el componente Transformar del objeto Main Camera 

 ![3](https://user-images.githubusercontent.com/49033767/126416982-cae0c3e0-3e1f-4039-9670-ced7cfe2e0bf.png)
 
4.	Mueva el objeto GvrEditorEmulator a una ubicación conveniente para el desarrollo, por ejemplo, Posición: 0, 3, 35 y Rotación: 0, 180, 0. 
 
 ![4](https://user-images.githubusercontent.com/49033767/126409662-637a28da-5721-495e-99e0-130106bb6654.png)
 
5.	Ingrese al modo de juego y use Alt + Mouse y Ctrl + Mouse para rotar e inclinar el ángulo de visión de la cámara. 

![5](https://user-images.githubusercontent.com/49033767/126409663-df73b719-697b-4a5c-b8c0-05b684a4730c.png)

## Preparando la escena para la interacción 

Durante este paso, prepararemos la escena para la interacción configurando el puntero, el emisor de rayos y el sistema de eventos, y luego probaremos el sistema de punto de referencia incluido (waypoint). 

1.	Agregue el objeto prefab GvrReticlePointer a la escena como elemento secundario del objeto del Main Camera. 

![6](https://user-images.githubusercontent.com/49033767/126409664-4f542a4d-ed92-46c8-9e0e-1ebd56eec9e9.png)
 
2.	Aumente el valor de Distancia máxima de retícula para el GvrReticlePointer del valor predeterminado de 10 a 20. 

![7](https://user-images.githubusercontent.com/49033767/126409666-024a2507-0c56-473a-a1df-9770f1858d9f.png)



	3.	Agregue el script GvrPointerPhysicsRaycaster como componente en el objeto Main Camera.
  ![8](https://user-images.githubusercontent.com/49033767/126409668-75ac2629-7277-4793-888a-3606ff5e037e.png)

4.	Agregue el objeto prefab GvrEventSystem a la escena. 

 ![9](https://user-images.githubusercontent.com/49033767/126416983-76e306d9-77db-4a92-88c3-8b48ab8cec17.png)
 
 ![10](https://user-images.githubusercontent.com/49033767/126410143-e0329289-5762-4885-8d40-f7e862723ee7.png)
 

5.	Ingrese al modo de juego y navegue por la escena haciendo clic en los puntos de referencia. 

 ![11](https://user-images.githubusercontent.com/49033767/126409672-d563eeca-ad7d-47e1-989b-76b5f67603b4.png)

## Hacer que los objetos del juego sean interactivos 

Durante este paso haremos que la Moneda, la Llave y la Puerta sean interactivas añadiéndoles componentes de disparadores y eventos.

1.	Localiza y selecciona el objeto  Coin en la jerarquía. 

 ![12](https://user-images.githubusercontent.com/49033767/126409673-2b177802-3e75-4934-82a0-ff5fdc4ab0b2.png)
 
 ![13](https://user-images.githubusercontent.com/49033767/126409674-2bb50819-e567-4dc0-9999-2e598d7ff316.png)
 
2.	Verifique que tenga un componente Collider. 

![14](https://user-images.githubusercontent.com/49033767/126409675-7ec2c801-f4af-4b76-bc1f-2f86d1038627.png)

 
3.	Agregue el script Coin proporcionado como componente. 

![15](https://user-images.githubusercontent.com/49033767/126409676-1e79ce29-a2e5-4e70-bfab-8897f54c529d.png)
 
4.	Agregue un dispardor de evento (Event Trigger) como componente. 

![16](https://user-images.githubusercontent.com/49033767/126409679-e1061613-5a33-4730-9d4b-0ab16752620a.png)
 
5.	Agregue el evento PointerClick al componente Event Trigger.

![17](https://user-images.githubusercontent.com/49033767/126409682-6ed1f68f-a123-4cd1-a816-da7de9760da5.png)
 
6.	Asigne el componente del script Coin al campo de objeto del evento Pointer Click. 

![18](https://user-images.githubusercontent.com/49033767/126409683-91206dff-66eb-4bc1-9fa1-00583876e197.png)
 
7.	Asigne el método Coin.OnCoinClicked () como la función para el evento Pointer Click. 

![19](https://user-images.githubusercontent.com/49033767/126409684-84b12fe0-b7a7-47ce-a0b0-1a976db34259.png)
 
8.	Ingrese al modo de juego, haga clic en la moneda y verifique que el mensaje 'Coin.OnCoinClicked ()' esté impreso en la ventana de la consola. 
 
 ![20](https://user-images.githubusercontent.com/49033767/126409685-6b4915c7-7bf0-42f1-a4a6-535db314b857.png)

9.	Repita el mismo proceso para el objeto del juego Key pero use el script Key y el método Key.OnKeyClicked (). 
 
 ![21](https://user-images.githubusercontent.com/49033767/126409686-9e0f2d85-90e2-4c99-ac6d-ecdfb9631023.png)
 
![22](https://user-images.githubusercontent.com/49033767/126409689-104c55d9-31bf-40b2-8dba-aca6935edf8f.png)
 
10.	Repita el mismo proceso para el primer objeto principal del juego de Puerta, pero use el script de Puerta y el método Door.OnDoorClicked (). 

 ![23](https://user-images.githubusercontent.com/49033767/126409690-c05902af-087c-4232-b8b1-d48d45c64af6.png)
 
![24](https://user-images.githubusercontent.com/49033767/126409691-7f6dbc0e-5462-4295-9738-b554fcbc7c74.png)
 
## Hacer la interfaz de usuario interactiva 

Durante este paso, haremos que el objeto SignPost sea interactivo al agregarle componentes de disparadores y eventos. El proceso es casi idéntico al que hicimos con la moneda, la llave y la puerta en el paso anterior, pero no necesitamos un colisionador para interactuar con los objetos del juego de la interfaz de usuario. En su lugar, debemos verificar que el objeto del juego Canvas tenga un componente Graphic Raycaster, y debido a que estamos usando GVR, reemplazaremos el Graphic Raycaster de Unity con el GvrPointerGraphicRaycaster de Google VR. 

1.	Localiza y selecciona el objeto del juego SignPost en la jerarquía. 

![25](https://user-images.githubusercontent.com/49033767/126409693-5514e51e-ba07-4b34-b82f-4de79e2417a5.png)
 
2.	Elimine el componente Graphic Raycaster que se agrega automáticamente al crear un nuevo objeto. 
 
![26](https://user-images.githubusercontent.com/49033767/126409695-d838d918-50ae-4918-b501-aa54a2eb3564.png)

![27](https://user-images.githubusercontent.com/49033767/126416979-2fa71e61-5ecf-4994-bfa2-974c640a8f2c.png)
 
3.	Agregue el script GvrPointerGraphicRaycaster como componente. 

 ![28](https://user-images.githubusercontent.com/49033767/126409697-995e1815-2b8e-4180-a286-fe750fd9bb05.png)

4.	Agregue el script SignPost proporcionado como componente.  

![29](https://user-images.githubusercontent.com/49033767/126409698-b00e7654-5d37-4a32-ba05-9ed7f9922bc9.png)

	5.	Agregue un Event Trigger como componente. 
 
 ![30](https://user-images.githubusercontent.com/49033767/126409699-285d3bdf-d5e8-4318-a25c-9d78be60c7a2.png)
 
6.	Agregue el evento PointerClick al componente Event Trigger. 

![31](https://user-images.githubusercontent.com/49033767/126409701-6c376ea3-1414-441a-b8dd-28cf8325744d.png)
 
7.	Asigne el componente script SignPost al campo de objeto del evento Pointer Click. 

![32](https://user-images.githubusercontent.com/49033767/126409702-248de88d-e522-4c88-8f66-47572c84793b.png)
 
8.	Asigne el método SignPost.ResetScene () como la función para el evento Pointer Click. 

![33](https://user-images.githubusercontent.com/49033767/126409704-b6ef207f-0cbc-44ac-be3f-9b3a603a1cbd.png)
 
9.	Ingrese al modo de juego, haga clic en SignPost y verifique que el mensaje 'SignPost.ResetScene ()' esté impreso en la ventana de la consola. 



## Programando el comportamiento de la moneda (coin) 
Durante este paso, programaremos el comportamiento de la moneda para que, cuando se haga clic en una moneda (coin), se reproduzca un sonido, muestre un efecto de "poof" y desaparezca. 
1.	Hay un mínimo de cinco monedas en el laberinto. Cuando se hace clic en una moneda, se reproduce un efecto de sonido en la ubicación de esa moneda.Cuando se hace clic en una moneda, esa moneda se elimina de la jerarquía de la escena. 
2.	Abra el script de Coin y lea todo el script, incluidos todos los comentarios. 
 
![34](https://user-images.githubusercontent.com/49033767/126409706-cda7d7e9-383f-498f-a321-de7422cefe10.png)
 
3.	Dedique un tiempo a comprender el comportamiento del objeto prefab CoinPoof proporcionado. Puede hacer esto, por ejemplo, ingresando al modo de juego y arrastrando un objeto prefab CoinPoof a la escena. 

![35](https://user-images.githubusercontent.com/49033767/126409707-4b99708c-9658-46ed-be41-004ad1e6d21e.png)
 
4.	Programe el comportamiento de la moneda completando todos los comentarios TODO en el script. 
 
![36](https://user-images.githubusercontent.com/49033767/126409709-be80cf43-d71d-49e1-bb5b-9d4a33199adf.png)

![37](https://user-images.githubusercontent.com/49033767/126409710-f0e8e92c-f7bb-4b53-a323-489265c06b47.png)
 
## Programando el comportamiento de la llave (key) 
Durante este paso, programaremos el comportamiento de la llave (key) para que, cuando se haga clic en la llave, reproduzca un sonido, muestre un efecto de "poof" y desaparezca. 
1.	Hay un mínimo de una llave en el laberinto. Cuando se hace clic en la llave, se reproduce un efecto de sonido en la ubicación de la llave. Cuando se hace clic en la llave, la llave se elimina de la jerarquía de la escena. Cuando se hace clic en la llave, la puerta se desbloquea. 
2.	Abra el script key y lea completo, incluidos todos los comentarios. 
3.	Dedique un tiempo a comprender el comportamiento del objeto prefab KeyPoof proporcionado. Puede hacer esto, por ejemplo, ingresando al modo de juego y arrastrando un objeto prefab KeyPoof a la escena. 
4.	Programe el comportamiento key completando todos los comentarios TODO en el script. 
 
 ![38](https://user-images.githubusercontent.com/49033767/126416192-adcdddd5-d2a8-4642-8f40-aa495c0879e6.png)
 
 
![39](https://user-images.githubusercontent.com/49033767/126409712-2062d8b0-5918-4097-90fc-d1ac03c45ec1.png)

## Programando el comportamiento de la puerta (door) 
Durante este paso, programaremos el comportamiento de la puerta (door) para que cuando se haga clic en la llave (key), la Puerta se desbloquee y cuando se haga clic en la Puerta, se escuche un sonido y comience a girar a una posición de apertura. 
1.	La puerta evita que el usuario navegue al objeto SignPost hasta que se haya abierto. Cuando comienza el juego, la puerta está bloqueada y cerrada. La puerta no se puede abrir cuando está bloqueada. La puerta solo puede desbloquearse haciendo clic en la llave. Cuando se hace clic y se desbloquea la puerta, la puerta comienza a abrirse. Cuando la puerta comienza a abrirse, se reproduce un efecto de sonido en la ubicación de la puerta. La puerta se anima a una posición de abierta solo por código, es decir, no mediante el uso de animación y controlador de animador. 
2.	Abra el script Door y lea todo el script, incluidos todos los comentarios. 
3.	Agregue un componente AudioSource al primer objeto padre Door y desactive la propiedad Play On Awake. 
4.	Asigne el audio Door_Opening al campo AudioClip. 
 
![40](https://user-images.githubusercontent.com/49033767/126409714-b9d6248f-7067-4526-bfcb-bb49b510d2dc.png)

5.	Programe el comportamiento de la puerta completando todos los comentarios TODO en el script. 
 
 ![41](https://user-images.githubusercontent.com/49033767/126416134-bcd8cd3c-806c-4d13-9903-60a6bd8f2958.png)
 ![42](https://user-images.githubusercontent.com/49033767/126409717-f4691f81-9c6f-48d2-b2b6-1d044024c009.png)
 
## Programando el comportamiento del SignPost 
Durante este paso, programaremos el comportamiento de SignPost para que cuando se haga clic en SignPost se reinicie el juego. 
1.	El SignPost no se puede ver ni interactuar antes de que se abra la puerta. Cuando se hace clic en SignPost, la escena se restablece a su estado inicial para que el juego se pueda volver a jugar. 
2.	Abra el script SignPost y lea todo el script, incluidos todos los comentarios. 
3.	Programe el comportamiento SignPost completando todos los comentarios TODO en el script. 

 ![43](https://user-images.githubusercontent.com/49033767/126409719-aafc2920-4baf-4488-bc55-fb769efe05bf.png)
 
## Crear la funcionalidad del juego 
Durante este paso, armaremos todo y convertiremos nuestro proyecto en un juego real. 
Laberinto 
• 	El laberinto está diseñado de tal manera que el usuario no puede identificar una ruta a la llave desde la posición de inicio. 
Waypoints 

Los puntos de referencia se colocan en todo el laberinto de tal manera que los usuarios pueden navegar desde la posición inicial a todos los objetos del juego con los que se puede interactuar, es decir, todas las monedas, la llave, la puerta y el SignPost. 
Monedas 
•	Hay un mínimo de cinco monedas en el laberinto. 
Llave 
•	Hay un mínimo de una clave en el laberinto. 
Puerta 
1.	La puerta evita que el usuario navegue hasta SignPost hasta que se haya abierto. 
SignPost 
•	El cartel no se puede ver ni interactuar antes de que se abra la puerta. 
1.	Use los objetos de juego  Maze para diseñar un laberinto. 

![44](https://user-images.githubusercontent.com/49033767/126409720-10ce2e34-a6de-43a0-9226-3b877f6fbe33.png)
 
2.	Mueva el jugador, es decir, el objeto del juego GvrEditorEmulator, a la ubicación de inicio deseada. 
3.	Agregue más Waypoints para que el jugador pueda navegar a todas las partes del Laberinto. 
 
 ![45](https://user-images.githubusercontent.com/49033767/126409721-9b480723-f4ca-460a-be82-76875c4e67ad.png)
 
4.	Agrega más monedas para que el jugador tenga muchas monedas para coleccionar. 
 
 ![46](https://user-images.githubusercontent.com/49033767/126409722-b2fd6753-0779-4fbe-842c-0090dcbf5ab5.png)
 
5.	Mueva la llave a una ubicación para que sea un tanto difícil para el jugador encontrarla. 
 
 ![47](https://user-images.githubusercontent.com/49033767/126409723-3498175f-7dbb-43b0-8692-491bf3821caa.png)
 
6.	Agregue paredes (cubos) para asegurarse de que los usuarios tengan que navegar para encontrar la llave y las monedas. 

![48](https://user-images.githubusercontent.com/49033767/126409724-28806837-e16d-4265-87db-c670f32abef1.png)
 
 
 	
	## ACTIVIDADES POR DESARROLLAR 
 
1. 	Crear un repositorio en GitHub con el nombre “Practica08 – Laberinto VR” 


 ![49](https://user-images.githubusercontent.com/49033767/126409727-987ae7f4-d211-464e-b8fc-ad00b4d8c3a9.png)
 
2. 	Realizar un commit y push por cada requerimiento de los puntos antes descritos. 
a.	Ignorar las carpetas Temp y Library 
b.	Agregar el archivo apk comprimido en .zip

![50](https://user-images.githubusercontent.com/49033767/126409728-53c762cb-9c4b-4cb7-99e7-5e16d9c9ed6a.png)

3. 	Luego, se debe crear el archivo README del repositorio de GitHub. 
4. 	Generar informe de los resultados en el formato de prácticas. Debe incluir: 
a.	El desarrollo de cada uno de los requerimientos antes descritos.  
b.	La evidencia del correcto diseño de la escena 
c.	La evidencia del correcto funcionamiento de la aplicación 
d.	El informe debe incluir conclusiones apropiadas.  
e.	En el informe se debe incluir la información de GitHub (usuario y URL del repositorio de la práctica)  
f.	En el informe se debe incluir la firma digital de los estudiantes. 
5. En el archivo README del repositorio debe constar la misma información del informe de resultados de la práctica que se indica en el punto anterior. 

## RESULTADO(S) OBTENIDO(S): 
	• 	Desarrolla e integra módulos interactivos virtuales. 
 
## CONCLUSIONES:  
Como conclusión se puede decir que con esta práctica mejoramos nuestros conocimientos vistos en clases, creando un entorno mucho mas creativo y sobre todo interactivo, para aquello que lo están usando, aprendimos a usar las animaciones, iteraciones, etc.. 
 
## RECOMENDACIONES:  
Revisar las clases, saber para que sirve cada herramienta en unity ya que es muy importante al momento de realizar nuestra práctica.
 
 
## REALIZADO POR: Carmen Bravo
## FIRMA:

![51](https://user-images.githubusercontent.com/49033767/126409729-b3e50090-e1a5-499f-8eba-3f3010bc4c57.png)
