# Refugios de Largo Plazo (RLP)

## Introducción

Este indicador está basado originalmente en un soft fork del Indicador Multi-Timeframe Recursive Zigzag de ©Trendoscope. Hemos utilizado la tecnología de sus librerías para la generación de Zigzags de manera que el usuario tenga la libertad de escoger cuál de los diferentes Zigzags que se calculan por Trendoscope como "Niveles" es el más adecuado para adaptarse a la generación de las fases ideales para su evaluación y selección como fases "más preponderantes", en períodos de largo plazo, de cualquier activo de acuerdo a su comportamiento en particular según su volatibilidad y ritmo de variación del precio.

## Fundamento Teórico del Indicador

Muchos de los inversores institucionales tradicionales utilizan la última fase de mercado de grado mayor que sobresale de las demás (mayor duración y mayor cambio de precio en temporalidad diaria), para basar un Fibonacci en cuyos niveles abren posiciones de largo plazo. Esas posiciones pueden quedar abiertas para activarse en el futuro hasta con años de antelación. Se considera que la fase tiene vigencia hasta que en el futuro se desarrolla otra nueva fase más preponderante; con la cual se repite la misma estrategia.

## Objetivos del Indicador

1. **Encontrar automáticamente** la última fase más preponderante de un activo, analizándolo en temporalidad diaria y tomando en cuenta si la tendencia del mercado a largo plazo es alcista o bajista.

2. **Trazar un Retroceso de Fibonacci** sobre la fase preponderante (revertido si la fase es alcista).

3. **Identificar las 3 fases más preponderantes**, de las cuales el indicador escoge a la Top-1 para el trazado.

4. **Selección manual opcional**: Si el usuario no concuerda con la selección automática del indicador, tiene la libertad de escoger a cualquiera de las otras 2 fases Top para el trazado del Fibo y sus niveles.

5. **Ajuste de parámetros**: Si el usuario no concuerda con la amplitud o la frecuencia de las fases del Zigzag trazado, puede modificar los parámetros del cálculo del Zigzag del algoritmo de ©Trendoscope hasta que una de las Top-3 coincida con la fase que tiene mentalizada.

6. **Concurso de Popularidad (CP)**: Como bonus experimental, el indicador ejecuta un concurso de tiro al blanco de coincidencias de precios (OHLC) diarios con todos los niveles Fibo de las Top 3 fases seleccionadas, para comprobar cuál es la fase que están validando los precios del mercado como la más popular para colocar operaciones. Los resultados del concurso se despliegan en la columna CP de la tabla Top-3 fases. Si como resultado del concurso se detecta que hay un cambio en la fase ganadora, se puede habilitar un switch para que se active una alerta que el usuario puede utilizar con el creador de alertas de TradingView para que le muestre una alarma, le mande un email, etc.

7. **Captura de coordenadas**: Este indicador fue diseñado para que el usuario encuentre la fase preponderante de largo plazo de sus activos y registre a mano las coordenadas fecha, precio de las anclas i0-i1 de la fase preponderante. Las coordenadas de la fase Top-1 se muestran en la tabla Top-3 fases de donde la puede capturar el usuario. Las coordenadas fecha, precio de todos los pivots HH y LL, de todas las fases del Zigzag, aparecen mediante un switch. Con los pivots, el usuario puede buscar o seleccionar otra fase diferente a las encontradas automáticamente por el indicador, de acuerdo a su investigación propia. Posteriormente, el usuario se olvida por un buen rato de este indicador RLP y pasa a aplicar en su operativa normal nuestro indicador RLPS (Refugios de Largo Plazo Simplificado), en el cual puede trazar y dar seguimiento simultáneo a los refugios de largo plazo de hasta 5 diferentes activos, con tan sólo introducir sus correspondientes coordenadas fecha, precio, las que fueron calculadas con este indicador RLP.

## Notas Adicionales

### 1. Configuración por Defecto
A la fecha de publicación de la versión v1.0 de RLP (12/2025), los parámetros de generación del Zigzag de ©Trendoscope se ajustaron por defecto para encontrar las fases preponderantes de largo plazo de Bitcoin y Ethereum (Pandemia 2020-2021). Los niveles mostrados en el gráfico corresponden a los resultados obtenidos usando los datos diarios del exchange Bitstamp, BTCUSD:BITSTAMP (popular en Europa).

### 2. Versión en Español y Mejoras
Debido a las estrictas reglas de publicación de TradingView relacionadas con el uso de lenguajes diferentes al inglés, la versión en español (román paladino) completa, con todas las entradas, ayudas (tooltips) y referencias bibliográficas, estará próximamente disponible en nuestro repositorio de GH: **aj-poolom-maasewal**. 

Cualquier corrección o mejora que se le puedan hacer a los algoritmos de selección de fases o al algoritmo del concurso CP de fases, serán altamente apreciados (las ciencias estadísticas, matemáticas y financieras, entre otras muchas, no son particularmente nuestro fuerte).

---

## Ecosistema de Refugios

**RLP forma parte de un ecosistema completo de análisis de acción del precio basado en refugios:**

• **RLP (Refugios de Largo Plazo)**: Identifica automáticamente la fase preponderante del Zigzag que los inversores institucionales utilizan como base para niveles de Fibonacci que proyectan la colocación de órdenes durante los siguientes meses y años.

• **RLPS (Refugios de Largo Plazo Simplificado)**: Versión simplificada de RLP donde las coordenadas conocidas de fases preponderantes de uno o múltiples activos pueden introducirse fácilmente para operativa permanente de largo plazo en diferentes temporalidades e intercambios.

• **RSCP (Refugios Semanales de Corto Plazo)**: Para análisis táctico de corto plazo (4H, 1H, Diario) basado en fases seleccionadas del Zigzag que definen niveles de Fibonacci efectivos durante la semana actual y próxima(s).

• **RID (Refugios Intra-Día)**: Para operaciones intra-día basadas en niveles calculados desde precios de apertura diaria, diseñado para temporalidades de 1H o menores, incluyendo estrategias de scalping.

Al combinar RLP, RLPS, RSCP y RID, obtienes un marco multi-temporal que proporciona claridad en cualquier horizonte de tiempo—desde posiciones de scalping hasta inversiones que abarcan meses y años.

---

**Desarrollado por**: aj p'óolom máasewal
