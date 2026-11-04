# QC-core: Software-Intensive Quantum Computing Core

### Propósito del repositorio QC-core 

La finalidad de este proyecto/repositorio es utilizar el paradigma de Sistemas Intensivos en Software en computación cuántica.

QC-Core busca mantener un orden al momento de hacer proyectos de computación cuántica, tomando un enfoque diferente al enfoque monolítico que se usa en la computación cuántica actual, donde la principal función de esta tecnología es analizar y verificar modelos matemáticos. Este repositorio busca crear una estructura en la ejecución cuántica, para así, tomarlo como un sistema modular, mantenible, y desacoplado, siguiendo el diseño de software conocido como Arquitectura Hexagonal[1], donde el dominio del sistema, los puertos y adaptadores son componentes separados que se relacionan, pero no se modifican, además de usar el patrón Pipes and Filters[2] para organizar el procesamiento de datos cuánticos, garantizando su resiliencia.

## Pilares arquitectónicos

### 1. Arquitectura hexagonal

La arquitectura hexagonal es una forma de organización caracterizada por crear desacoplamiento en las partes de un producto software. Su finalidad en el repositorio es poder crear componentes independientes conocidos como: 

1) Dominio: El conocimiento científico, matemática agnóstica y determinista, funcionando como contenedor de los algoritmos cuánticos y las reglas del negocio. 
2) Puertos: Interfaces abstractas que definen la forma y estructura con la que se debe trabajar en el repositorio. 
3) Adaptadores: Funcionalidad concreta del producto, nacido de los puertos; es decir, las aplicaciones puntuales de los puertos en problemas específicos. Se comunican entre sí pero no 
   
se modifican directamente, garantizando resiliencia en cambios de entorno, ya sea simulado o hardware real, sin tener que cambiar completamente los componentes.

### 2. Pipes and filters

Es un patrón arquitectónico que permite desglosar un flujo de datos complejos en una serie de pasos modulares e independientes[5]. Su finalidad en el repositorio es poder reutilizar filtros en las distintas aplicaciones que usen el esquema propuesto por el repositorio para generar mejora en rendimiento y escalabilidad, permitiendo a su vez cumplir con el ciclo de vida de los algoritmos cuánticos[6].

### 3. Resiliencia y tolerancia a fallos

Es la capacidad que tiene un sistema o producto software para mantener su funcionamiento ante errores inesperados, fallos en componentes, o picos de tráfico digital[7]. Es importante tener en cuenta esto, puesto que uno de los principios que se busca con este repositorio es mantener resiliencia ante situaciones inesperadas, teniendo alternativas para que cuando ocurran estos errores, no se pierda progreso, no haya colas de espera, o se retrase en general una salida de sistema. 

### 4. Observabilidad y telemetría

La observabilidad en un producto software es la capacidad de inferir, por medio de las salidas/resultados externos, el funcionamiento interno de un sistema. Junto con la telematría, que es el proceso de recolección y transmisión de datos desde fuentes remotas a una central para análisis y monitoreo[8], buscan garantizar trazabilidad en las distintas aplicaciones o pruebas que sucedan en el entorno del repositorio, para así lograr un claro rastreo y documentación a lo largo de su ciclo de vida.

## Estructura del repositorio

## Referencias

[1] A. Cockburn, "Hexagonal Architecture (Ports and Adapters)," 2005. [Online]. Available: https://alistair.cockburn.us/hexagonal-architecture/
[2] L. Bass, P. Clements, and R. Kazman, Software Architecture in Practice, 4th ed. Boston, MA: Addison-Wesley, 2021. 
[3] M. Piattini et al., "The Talavera Manifesto for Quantum Software Engineering and Programming," Software Quality Journal, 2020. 
[4] D. Deutsch, "Quantum theory, the Church-Turing principle and the universal quantum computer," Proceedings of the Royal Society of London. A, vol. 400, no. 1818, pp. 97–117, 1985.
[5] Microsoft Corporation, "Patrón Pipes and Filters," Microsoft Learn: Centro de Arquitectura de Azure, 2023. [En línea]. Disponible en: https://learn.microsoft.com/es-es/azure/architecture/patterns/pipes-and-filters. [Accedido: Nov. 02, 2026].
[6] A. Gómez y E. Moguel, "Ingeniería de software cuántico: ciclo de vida para el desarrollo de software cuántico," Tecnalia Blog, 2023. [En línea]. Disponible en: https://www.tecnalia.com/blog/ingenieria-software-cuantico-ciclo-vida. [Accedido: Nov. 02, 2026].
[7] IBM Corporation, "¿Qué es la resiliencia de las aplicaciones?," IBM Think Topics, 2024. [En línea]. Disponible en: https://www.ibm.com/think/topics/application-resiliency. [Accedido: Nov. 02, 2026].
[8] N. Sharma, "Observability vs. Telemetry vs. Monitoring: Differences and Synergies," Last9 Blog, Sep. 04, 2023. [En línea]. Disponible en: https://last9.io/blog/observability-vs-telemetry-vs-monitoring/. [Accedido: Nov. 03, 2026].