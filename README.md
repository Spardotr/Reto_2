# reto_02

Este diagrama de clases, hecho con Mermaid, representa un sistema de gestión de biblioteca. En él, se muestra cómo están relacionadas las clases de usuarios, libros, y las operaciones de préstamo y devolución.

Usuario: puede tomar prestado y devolver libros.

Libro: tiene atributos como título, autor, ISBN y estado.

Biblioteca: gestiona los libros y los usuarios, y maneja las operaciones de préstamo y devolución.

```mermaid
  classDiagram
    Biblioteca  -->  Libro : contiene
    Biblioteca  -->  Usuario : registra
    Usuario  -->  Libro : toma prestado

    class Biblioteca {
        - libros: List<Libro>
        - usuarios: List<Usuario>
        + registrar_libro(libro: Libro)
        + registrar_usuario(usuario: Usuario)
        + prestar_libro(libro: Libro, usuario: Usuario)
        + devolver_libro(libro: Libro, usuario: Usuario)
        + consultar_estado_libro(libro: Libro)
    }
 
    class Libro {
        + titulo: String
        + autor: String
        + isbn: String
        + estado: String
    }

    class Usuario {
        + nombre: String
        + id_usuario: int
    }
