# Diseño - Relaciones por colaboración

## ¿Por qué?

Código escrito sin una reflexión sobre las relaciones de los componentes que lo conforman produce complejidad arbritraria.

## ¿Qué?

|Encontrar clases|Organizarlas mediante relaciones justificadas|Describirlas en código
|:-:|:-:|:-:|

El objetivo no es llegar a un diagrama correcto. Es **justificar cada decisión** y ser capaz de defenderla ante una decisión alternativa igualmente razonada.

No se evalúan documentos, diagrama ni código (aunque son imprescindibles). Se evalúa la coherencia entre las decisiones de dominio, las relaciones elegidas y el código resultante. Una justificación sólida de una decisión discutible vale más que una decisión convencional sin justificación.

## ¿Para qué?

Ver cómo detenerse a pensar en los criterios de ciclo de vida, exclusividad y temporalidad antes de codificar evita refactorizaciones costosas. Una relación mal elegida se paga cada vez que el código cambia.

## ¿Cómo?

### Escenarios propuestos

- Ecosistema musical
- Decisión
- Identidad
- Conversación

### Identificar

Escribir **en lenguaje natural** los elementos del dominio. Si hay descartes, justifique.

### Relacionar

Para cada par de clases, identificar:

- ¿Quién controla el ciclo de vida de quién?
- ¿La relación es permanente o puntual?
- ¿Es exclusiva o compartida?

Usar la relación más débil posible que responda las tres preguntas. Justificar por qué no se eligió la inmediatamente más fuerte.

### Codificar *parcialmente*

Implementar en Java las clases identificadas. No es necesario implementar todos los métodos: sí es obligatorio que el constructor refleje las decisiones de relación tomadas en cuenta en la iteración anterior.

El `main` principal debe instanciar al menos una situación del dominio en el que estén involucradas todas las entidades identificadas.

### Cuestionar

- Cuestionaremos diagramas de otros para observar si *la(s) relación(es) elegida(s) sobrevive(n) a cambio(s) de decisión(es) de dominio*.
