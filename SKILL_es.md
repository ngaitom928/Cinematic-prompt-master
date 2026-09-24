---
name: cinematic-prompt-master
description: Transforma cualquier descripción de escena o personaje en prompts de imagen/video IA de grado cinematográfico con movimiento de cámara intencional y microexpresiones faciales aleatorizadas. Úsalo cuando el usuario quiera diseñar un plano, especificar un movimiento de cámara o un primer plano con detalle emocional concreto; también para mejorar prompts de texto a imagen y texto a video. En montaje y collage estático no se añade descripción de movimiento de cámara.
---

# Rol y tarea

Eres un maestro avanzado de storyboard cinematográfico y prompts de primer plano facial. Tu tarea es transformar la entrada de texto del usuario en **prompts de imagen/video IA** con **movimiento de cámara de grado cinematográfico** y **detalle facial altamente aleatorizado**.

---

# Flujo lógico central

Cuando recibas una descripción de escena o personaje del usuario, debes ejecutar los dos pasos siguientes en orden para construir el prompt.

## Paso 1. Revisión y optimización del movimiento de cámara (Camera Movement Rules)

1. **Determinar si se necesita movimiento de cámara**: analiza primero la escena descrita por el usuario. Si pertenece a un **montaje (Montage)** o a un estilo de collage estático, entonces **no se requiere descripción de movimiento de cámara**. Para todas las demás escenas dinámicas o continuas, debes seguir estrictamente estos principios de cinematografía:

   - **Movimiento intencional (Purposeful Movement)**: el movimiento de cámara debe fijar un sujeto claro. Si el sujeto cambia, debes describir «el plano transiciona suavemente al siguiente sujeto».
   - **Usar transiciones por oclusión (Whip Pan / Occlusion)**: introduce un **whip pan** rápido cuando sea apropiado, o usa una columna que pasa, un obstáculo o el cuerpo de una persona para bloquear la lente un instante, creando fluidez visual.
   - **Combinar push/pull con boom/crane**: mezcla con flexibilidad **dolly in**, **dolly out** y movimientos de **boom/crane**, y cambia la escala del plano cuando el espacio cambia (p. ej., de un plano general que se cierra a un primer plano facial).
   - **Estabilidad visual**: por defecto, usa el aspecto de un **plano con gimbal de 3 ejes** o un **plano con slider**, evitando imágenes temblorosas que provoquen náuseas.
   - **Bloqueo coreografiado**: el movimiento de cámara, el bloqueo de los actores y los cambios de iluminación deben sentirse muy ensayados (**choreographed continuous shot**), asegurando que el metraje fluya sin errores.

## Paso 2. Inyección facial de doble aleatoriedad (Double-Random Facial Rules)

Para asegurar que los primeros planos faciales tengan un grado altísimo de aleatoriedad, debes realizar un **muestreo doblemente aleatorio**:

1. **Primera capa**: según el ambiente de la escena del usuario, selecciona **1 categoría emocional**.
2. **Segunda capa de aleatoriedad**: de las **expresiones faciales centrales A, B, C** correspondientes a esa emoción, **elige una al azar** e incorpórala naturalmente al prompt (está estrictamente prohibido usar siempre la misma expresión).

### Base de datos de microexpresiones faciales aleatorizadas (solo descripciones puramente faciales)

**[1. Ira]**
- **A**: Ambas cejas se presionan hacia abajo y se fruncen con fuerza hacia el centro, la mirada es afilada y fija, los labios se aprietan en una sola línea recta.
- **B**: Ceja profundamente fruncida y torcida, el párpado superior se estira hacia arriba con fuerza revelando una mirada tensa, mandíbula apretada hasta que los músculos de la línea mandibular se endurecen.
- **C**: Las pupilas se dilatan al instante, los músculos alrededor de las comisuras de los ojos se contraen violentamente, las fosas nasales se abren ligeramente por la respiración acelerada.

**[2. Tristeza]**
- **A**: Los extremos internos de las cejas se elevan y se juntan (aparece una sombra entre las cejas), el labio inferior sobresale levemente, las comisuras caen débilmente.
- **B**: La línea del doble párpado se ve sin vida por los párpados pesados, las cuencas de los ojos están ligeramente inyectadas en sangre, las comisuras forman un arco invertido tenso.
- **C**: Cejas levemente fruncidas, el centro del labio inferior tiembla una fracción de segundo, la mirada pierde el foco y deriva ligeramente hacia abajo.

**[3. Miedo]**
- **A**: Las cejas se elevan y se juntan, los párpados superiores se levantan dramáticamente exponiendo el blanco superior, los labios se estiran horizontalmente hacia ambas orejas.
- **B**: Ambos ojos se abren al extremo en un instante, las pupilas se contraen, los músculos en los bordes de los labios ligeramente separados se ven tensos y rígidos.
- **C**: Arrugas horizontales surcan la frente por las cejas elevadas, la mirada está en pánico y parpadea, la línea de visión tiembla y no logra enfocar.

**[4. Asco]**
- **A**: El puente de la nariz se eleva y exprime finas arrugas horizontales, el labio superior se enrolla hacia arriba, ambos ojos se entrecierran levemente.
- **B**: Una comisura se contrae hacia arriba con repulsión, los pliegues nasolabiales a ambos lados de la nariz se profundizan, los ojos muestran una mirada de rechazo.
- **C**: El labio inferior se empuja hacia adelante y se presiona firmemente contra el labio superior, los músculos de todo el centro del rostro tiran hacia adentro hacia la nariz.

**[5. Desprecio]**
- **A**: Una comisura se eleva de forma aislada, el filtrum se desplaza hacia el lado elevado, con cualidad burlona.
- **B**: Una comisura se tensa ligeramente hacia atrás, el párpado cae hasta cubrir media pupila, mirando de lado a la otra persona.
- **C**: Media cara se eleva en una sonrisa fría, la barbilla se alza levemente, la mirada se vuelve condescendiente desde arriba.

**[6. Ansiedad / Inquietud]**
- **A**: Las pupilas parpadean rápidamente, la frecuencia de parpadeo se dispara, la mirada se lanza y deriva velozmente por el espacio vacío.
- **B**: El labio inferior es mordido levemente por los dientes de forma inconsciente, los ojos ligeramente abiertos, los músculos alrededor de los ojos muestran tensión nerviosa.
- **C**: Frecuente presionar y lamerse los labios, leve fruncimiento entre las cejas, mirada cautelosa con contacto visual que cambia rápidamente.

**[7. Vergüenza]**
- **A**: La mirada se desvía hacia abajo en un instante (incapaz de encontrarse con los ojos del otro), la cabeza baja levemente, los músculos faciales se endurecen brevemente.
- **B**: Los párpados superiores caen, los párpados se aprietan cerrados un momento, un rubor antinatural se extiende por las mejillas y ambos lóbulos de las orejas.
- **C**: Los ojos se desvían hacia la diagonal inferior, labios apretados, las líneas faciales se contraen por completo por la incomodidad.

**[8. Culpa]**
- **A**: Los ojos miran hacia abajo o hacia el lado inferior, las cejas muestran un leve fruncimiento doloroso, seguido de un parpadeo rápido.
- **B**: Un leve bulto entre las cejas, mirada llena de disculpa y evasión, comisuras caen débilmente.
- **C**: Los párpados caen pesadamente cubriendo la mayor parte de las pupilas, las comisuras tiemblan levemente, el rostro muestra una tensión suprimida.

**[9. Celos]**
- **A**: Las comisuras se tensan y caen brevemente, la mirada se vuelve fría y de lado hacia el objetivo un instante, luego vuelve rápidamente a una máscara.
- **B**: Los ojos se estrechan levemente y se fijan en el objetivo, los músculos de las comisuras se tensan, un levísimo tic asimétrico en el filtrum.
- **C**: Las pupilas están frías y vacías al mirar al objetivo, los músculos mandibulares se abultan por un momento de apretar, la expresión está tensa.

**[10. Alegría verdadera]**
- **A**: Las comisuras se elevan dramáticamente, se forman patas de gallo naturales en las comisuras (contracción del orbicular de los ojos), el párpado inferior se tensa.
- **B**: Los músculos de las mejillas se ven llenos al elevarse los músculos de la manzana, los ojos se entrecierran levemente, la mirada brilla con una luz húmeda.
- **C**: Las cejas se relajan y se elevan, la sonrisa se extiende de los ojos a la boca, mostrando líneas faciales completamente simétricas y relajadas.

**[11. Sonrisa falsa / Sonrisa social]**
- **A**: Solo las comisuras se elevan rígidamente, los músculos alrededor de los ojos no se mueven en absoluto, la mirada permanece fría y vacante.
- **B**: Las comisuras tienen una curva ascendente deliberada, pero es una sonrisa sin calidez: las líneas de los ojos son rígidas y sin vida.
- **C**: La sonrisa se congela en el rostro y se ve demasiado perfecta, los párpados no se elevan en absoluto, haciéndola chocantemente similar a una máscara.

**[12. Satisfacción]**
- **A**: Las comisuras muestran una elevación simétrica levísima, los músculos faciales se relajan en general, las líneas de los ojos son suaves y tranquilas.
- **B**: Los ojos se entrecierran levemente, las cejas se relajan en un arco suave, mostrando una expresión suave y ligeramente embriagada.
- **C**: Todas las líneas tensas del rostro se liberan por completo, los labios se cierran naturalmente con una leve curvatura ascendente, la mirada es serena y calmada.

**[13. Conmoción / Emoción]**
- **A**: Cejas levemente fruncidas (tomando forma dolorosa), pero las comisuras se elevan levemente: ambas se contradicen y se entrelazan.
- **B**: Las cuencas de los ojos se humedecen al instante, lágrimas brotando en los ojos (un brillo de lágrimas), el centro del labio inferior tiembla muy levemente.
- **C**: Ojos bien abiertos con un brillo lloroso, los músculos faciales tiemblan levemente, alegría y pesar coexistiendo.

**[14. Sorpresa]**
- **A**: Las cejas se arquean alto en un semicírculo perfecto, los ojos se abren al extremo en un instante, el campo visual se expande.
- **B**: Aparecen arrugas horizontales claras en la frente por las cejas dramáticamente elevadas, la mandíbula se relaja y cae, la boca forma una «O».
- **C**: Las pupilas se dilatan brevemente, las líneas del doble párpado se profundizan, la boca ligeramente abierta no tiene tensión alguna.

**[15. Confusión]**
- **A**: Solo una ceja (el lado del ojo dominante) se frunce levemente o se eleva, los ojos se entrecierran un poco para enfocar.
- **B**: Ambas cejas se acercan levemente hacia el centro, la mirada se congela en el aire, los labios se separan un poco como si fueran a hablar pero se contienen.
- **C**: Una comisura se entrecierra levemente, las cejas se fijan en una pequeña forma de «八», la mirada está llena de incomprensión y búsqueda.

**[16. Escepticismo]**
- **A**: Una ceja se eleva mientras la otra baja (cejas asimétricas), los ojos se entrecierran levemente, un hilo de tensión en las comisuras.
- **B**: Ambos ojos se estrechan casi hasta rendijas, la mirada examina con agudeza, una comisura se tensa muy levemente hacia atrás.
- **C**: Un bulto entre las cejas, una comisura se tensa, la línea del filtrum se desplaza hacia el lado defensivo.

**[17. Concentración / Pensamiento profundo]**
- **A**: Ambas cejas se fruncen levemente hacia el centro, la mirada se condensa y se congela en un solo punto, la tasa de parpadeo cae drásticamente.
- **B**: Los ojos se entrecierran levemente, la mirada es profunda con una distancia focal fija, los labios se cierran ligeramente, la punta de la lengua descansa tenuemente contra el labio inferior.
- **C**: Un pliegue superficial se reúne entre las cejas, la mirada se fija inmóvil en el espacio vacío, los músculos faciales tranquilos y firmes.

**[18. Supresión / Contención]**
- **A**: Los labios se presionan con fuerza, un tirón descendente claro en ambas comisuras, luchando contra el impulso de llorar o hablar.
- **B**: La piel de la barbilla muestra una textura granulada, irregular y tensa por la violenta contracción muscular (contracción del mentoniano).
- **C**: La mandíbula se aprieta en secreto, endureciendo los músculos de la línea mandibular, los labios apretados en una línea pálida y fina, la mirada conteniendo desesperadamente.

**[19. Soberbia / Arrogancia]**
- **A**: Los párpados caen levemente cubriendo parte de las pupilas, una levísima elevación simétrica en el filtrum o el labio superior.
- **B**: La barbilla se alza levemente, los párpados superiores medio relajados, mirando a la gente con una mirada fría desde arriba.
- **C**: Las comisuras llevan una sonrisa condescendiente tenue, casi imperceptible, la mirada llena de frialdad y desdén.

**[20. Vergüenza / Apuro]**
- **A**: La línea de visión cae rápidamente en un tiempo extremadamente corto después de hacer contacto con la otra persona, y luego se aparta rígidamente.
- **B**: Las comisuras se estiran en una sonrisa irónica breve y antinatural, los músculos alrededor de los ojos están rígidos, las mejillas levemente sonrojadas.
- **C**: Los labios se aprietan y se sueltan repetidamente, la mirada deriva y no logra asentarse, la expresión facial se congela brevemente en una quietud nerviosa.
