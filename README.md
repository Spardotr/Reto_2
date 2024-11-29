    classDiagram
        class Libro {
            +String titulo
            +String autor
            +String isbn
            +String estado
            +Libro(titulo, autor, isbn)}
        class Usuario {
            +String nombre
            +int id_usuario
            +Usuario(nombre, id_usuario)}
        class Biblioteca {
            +List<Libro> libros
            +List<Usuario> usuarios
            +Biblioteca()
            +registrar_libro(libro)
            +registrar_usuario(usuario)
            +prestar_libro(libro, usuario)
            +devolver_libro(libro, usuario)
            +consultar_estado_libro(libro)
        }
        Biblioteca "0..*" --> "0..*" Libro : contiene
        Biblioteca "0..*" --> "0..*" Usuario : tiene
