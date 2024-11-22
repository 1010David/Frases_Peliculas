Front para el ejercicio: https://github.com/alura-es-cursos/2086-java-desafio-front

# Desafío de Aplicación con Base de Datos de Frases de Películas

Este proyecto es un desafío donde hemos creado una aplicación en Java utilizando Spring y una base de datos que contiene frases de películas famosas. El objetivo de este proyecto es desarrollar una API que maneje las frases, integrando el backend con un frontend donde los usuarios pueden visualizar estas frases y disfrutar de algunas de sus citas favoritas.

## Descripción del Proyecto

La aplicación cuenta con un **back-end** construido con **Spring** y un **front-end** que se conecta a este para mostrar frases de películas. Durante el desarrollo, nos enfrentamos a algunos problemas comunes y aprendimos cómo solucionarlos.

Uno de los problemas que resolvimos fue el de **CORS (Cross-Origin Resource Sharing)**, que impide que nuestro frontend pueda acceder a las APIs debido a restricciones del navegador. Para solucionar esto, creamos una clase de configuración que habilita el acceso a orígenes específicos.

## Pasos Seguidos en el Proyecto

1. **Configuración de CORS:**
   Para solucionar el problema de CORS, creamos una clase llamada `CordsConfiguration`, donde configuramos los orígenes permitidos para las peticiones entre el frontend y el backend. Utilizamos la anotación `@Configuration` para que Spring reconociera esta clase como una clase de configuración y `WebMvcConfigurer` para implementar la configuración de CORS.

   Aquí está el código que usamos:

   ```java
   @Configuration
   public class CordsConfiguration implements WebMvcConfigurer {
       @Override
       public void addCorsMappings(CorsRegistry registry) {
           registry.addMapping("/**").allowedOrigins("http://localhost:5501");
       }
   }



### Detalles clave:

1. **Objetivo del proyecto**: Descripción de la base de datos de frases de películas.
2. **Solución CORS**: Explicación del cambio para habilitar CORS entre el frontend y el backend.
3. **Instrucciones de ejecución**: Pasos detallados para clonar, construir y ejecutar el proyecto.
4. **Tecnologías utilizadas**: Las herramientas y tecnologías que se usaron para el desarrollo de la aplicación.
5. **Conclusión y motivación**: Se anima a los usuarios a seguir practicando y aplicando lo aprendido en el proyecto.

Puedes personalizarlo según las necesidades de tu proyecto. ¡Espero que te sea útil!
