1. **¿Qué problema busca resolver Clean Architecture en el desarrollo de software?**  
   Busca reducir el acoplamiento y aumentar la mantenibilidad, permitiendo que la lógica de negocio sea independiente de frameworks, bases de datos o interfaces externas.

2. **¿Cuáles son las principales capas de Clean Architecture y qué responsabilidad tiene cada una?**  
   - **Domain:** reglas y entidades del negocio.  
   - **Application (Use Cases):** orquesta casos de uso y coordina el flujo.  
   - **Interface/Adapters:** adapta datos entre capas internas y externas.  
   - **Infrastructure:** implementa detalles técnicos (DB, frameworks, controladores).

3. **¿Qué relación tiene Clean Architecture con el principio de Inversión de Dependencias (DIP) en SOLID?**  
   Las dependencias apuntan hacia el dominio; las capas externas dependen de las internas mediante interfaces, siguiendo el DIP.

4. **¿Por qué es importante desacoplar la lógica de negocio de la infraestructura en una aplicación?**  
   Permite cambiar tecnologías sin afectar el núcleo del sistema y facilita pruebas unitarias y mantenimiento.

5. **¿Cómo Clean Architecture facilita la escalabilidad y mantenibilidad de un sistema?**  
   Al separar responsabilidades y evitar dependencias rígidas, permite extender funcionalidades o reemplazar componentes sin modificar el dominio.

6. **¿Qué diferencia hay entre la capa de dominio y la capa de aplicación en Clean Architecture?**  
   El **dominio** define reglas del negocio; la **aplicación** define cómo se ejecutan esas reglas mediante casos de uso.

7. **¿Por qué los controladores (controllers) y la base de datos deben estar en la capa de infraestructura?**  
   Porque son detalles externos y reemplazables; no deben influir en la lógica del negocio.

8. **¿Qué ventajas tiene usar una interfaz en la capa de dominio para definir repositorios en lugar de usar directamente JpaRepository?**  
   Evita acoplar el dominio a JPA, frameworks o anotaciones; permite cambiar la tecnología de persistencia sin afectar el dominio.

9. **¿Cómo interactúan los casos de uso (UseCases) con las entidades de dominio en Clean Architecture?**  
   Los casos de uso invocan reglas del dominio y usan repositorios definidos por interfaces para obtener o persistir entidades.

10. **¿Cómo se puede aplicar Clean Architecture en una aplicación de microservicios con Spring Boot?**  
   Separando módulos por capas, usando interfaces para puertos, implementaciones en infraestructura, controladores como adaptadores y cada microservicio con su propio dominio y casos de uso.
