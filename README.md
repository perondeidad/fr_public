¡Hola!
Aquí está. Básicamente, la historia de las herramientas de Farbrausch entre 2001 y 2011.
Llevábamos una eternidad queriendo publicar todo esto de diversas formas,
pero siempre acabábamos no haciéndolo porque decíamos: "primero tendríamos que darle una limpieza...".

Se acabó. Esto no está limpio. Es el material tal cual: 
algo proviene de discos duros viejos y otra parte es reciente de varios repositorios SVN.
Es código escrito para un montón de versiones distintas de Visual Studio. 
Algunas partes son muy difíciles de compilar y otras muy fáciles. 
Hay cosas que están bien estructuradas y otras que son un completo desastre.

El código original sin modificar (con algunas correcciones de errores) está archivado bajo la etiqueta "original",
por si existe un interés histórico;
pero a partir del 16 de abril de 2012, la rama principal (master) de este repositorio contiene código que compila con Visual Studio 2010 (lo cual suponemos es más útil para la gente).
Originalmente anticipamos que hacer que todo funcionara con un compilador reciente sería difícil,
pero resultó ser bastante sencillo y solo requirió pequeños cambios en la base del código, por lo que no tiene mucho sentido mantener las dos ramas separadas.

Todo esto se publica bajo una licencia BSD o se pone en el dominio público (según se indique por proyecto). 
No es que sea probable que quieras usar la mayor parte de este código, pero si quieres hacerlo,
no vemos razón para impedírtelo.

Entonces, ¿qué tenemos aquí? Esta es la estructura de directorios básica:

```
  altona_wz4/           - Altona and Werkkzeug4. Our most recent code foundation and tool.
    altona/             - The framework libraries (includes base Werkkzeug4 GUI).
    wz4/                - Wz4FRlib (demo ops) and Wz4Player.
  altona2/              - successor of altona
    altona2/            - The framework libraries (Werkkzeug5 is not yet released)
  genthree/             - GenThree. Used for Candytron and nothing else.
    data/               - Candytron data files.
  kkrunchy/             - kkrunchy 0.23alpha code (latest we could find)
  kkrunchy_k7/          - kkrunchy_k7 0.23a4/asm07 (most recent version)
  ktg/                  - OpenKTG texture generator. See below.
  lekktor/              - May summon Eldritch Abominations. Handle with care.
  RG2/                  - RauschGenerator 2. Used for several 64k intros.
    dopplerdefekt/      - data files for fr-029: dopplerdefekt
    einschlag/          - data files for fr-022: ein.schlag
    flybye/             - data files for fr-013: flybye
    welcome_to/         - data files for fr-024: welcome to...
  v2/                   - V2 synthesizer system. Used for all our intros, kkrieger and debris.
  werkkzeug3/           - Werkkzeug3. Used for tons of demos and intros.
    data/               - Source data for kkrieger and some test projects.
      debris/           - Source data for fr-041: debris.
      theta/            - Source data for fr-038: theta.
    w3texlib/           - Werkkzeug 3 texture lib. Used for fr-033.
    wz_mobile/          - Werkkzeug Mobile. Never got used for anything.
  werkkzeug3_kkrieger/  - kkrieger branch. Game mode in here might work. :)
```

Así que, aquí tienen algunos consejos para "turistear" por el código:

"ktg" es OpenKTG, una propuesta para un subconjunto de funciones de generación de texturas simple pero relativamente potente y ortogonal, diseñado alrededor de 2007. Es un código muy limpio y agradable.
Si quieres generar texturas para WebGL o algo parecido, convertir esto a pixel shaders + código JS debería funcionar bastante bien. (Eso sí, no tiene un editor amigable).

GenThree contiene varios archivos de texto en alemán con diversas ideas de la época de Candytron; la mayoría escritos por Chaos. Es un pedazo interesante de historia :)

werkkzeug3 es un desastre, pero vamos, es el de debris... saben que lo quieren... :)

werkkzeug3_kkrieger proviene de una rama llamada "kkrieger" de nuestro repositorio SVN. No es el código exacto de kkrieger e incorpora cambios realizados más de un año después del lanzamiento original del juego. Sin embargo, se separó en una rama antes de que dejáramos de preocuparnos por romper la compatibilidad con kkrieger al hacer cambios. Tienen más posibilidades de compilar el juego desde aquí que desde el árbol "regular" de werkkzeug3, aunque es poco probable que cualquiera de los dos funcione a la primera. Si alguien realmente quiere un árbol de werkkzeug3 cercano al original de 2004, debería ser posible desenterrar algo. :)

altona_wz4 debería ser totalmente funcional. Ha sido probado y existen binarios que deberían funcionar como un "demomaker" completo sin necesidad de tocar el código. Además, es una buena base para escribir tu propio motor, juego, herramienta o lo que sea. Este material ha sido usado intensamente en varias empresas y ha pasado por departamentos de control de calidad (QA) reales. Funciona.

Colaboradores (en orden alfabético):

Fabian "ryg" Giesen: GenThree, kkrunchy, kkrunchy_k7, ktg, lekktor, RG2, werkkzeug3, werkkzeug3_kkrieger, altona, werkkzeug4.

Sebastian "Wayfinder" Grillmaier: RG2, dopplerdefekt, ein.schlag, debris, kkrieger.

Tammo "kb" Hinrichs: V2, RG2, altona, werkkzeug4, flybye, "welcome to", easterparty.

Thomas "fiver2" / "theunitedstatesofamerica" Mahlke: werkkzeug3, werkkzeug4, debris, kkrieger.

Christoph "giZMo" Muetze: genthree, Candytron, RG2, flybye, "welcome to", werkkzeug3, wz_mobile, debris, kkrieger.

Dierk "Chaos" Ohlerich: GenThree, lekktor, werkkzeug3, werkkzeug3_kkrieger, wz_mobile, altona, werkkzeug4.

Kai "cp" Poethkow: dopplerdefekt, ein.schlag, theta.

Ronny Pries: debris.

Dennis "Exoticorn" Ranke: RG2, flybye, werkkzeug3_kkrieger.

Leonard "paniq" Ritter: V2, theta.

Bastian "Tron" Zuehlke: werkkzeug3, werkkzeug4.

Tanto altona_wz5 como altona2 contienen varias de las librerías stb_??? de Sean Barret (nothings.org).

¡Que se diviertan! (Publicado en abril de 2012) (Actualizado en octubre de 2014 para Altona2)
