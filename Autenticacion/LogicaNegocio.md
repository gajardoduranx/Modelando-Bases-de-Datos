## Listado de Entidades 

### usuarios **(ED)**

- usuario_id **(PK)**
- username **(UQ)**
- password
- email **(UQ)**
- nombre
- apellido
- avatar
- activo
- fecha_creacion
- fecha_actualizacion

### roles **(EC)**

- rol_id **(PK)**
- nombre
- description

### permisos

- permiso_id **(PK)**
- nombre
- description

### roles_x_usuarios **(EP)**

- rxu_id **(PK)**
- usuario_id **(FK)**
- rol_id **(FK)**

### permisos_x_roles **(EP)**

- pxr_id **(PK)**
- rol_id **(FK)**
- permiso_id **(FK)**

## Relaciones

1. **Usuarios** tiene **roles** (_M - M_)
1. **roles** tiene **permisos** (_M - M_)

### Modelo Relacional de la BD

![Modelo Relacional](./ModeloRelacional.drawio%20(1).png)

## Reglas de Negocio

### usuarios

1. Crear un usuario.
2. Leer todos los usuarios.
3. Leer un usuario en particular.
4. Actualizar un usuario.
5. Validar un usuario.
6. Habilitar un usuario.
7. Inhabilitar un usuario.
8. Actualizar datos de un usuario.
9. Actualizar password de un usuario.
10. Eliminar un usuario.

### roles

1. Crear un rol.
2. Leer todos los roles.
3. Leer un rol en particular.
4. Actualizar un rol.
5. Eliminar un rol.

### permisos

1. Crear un permiso.
2. Leer todos los permisos.
3. Leer un permiso en particular.
4. Actualizar un permiso.
5. Eliminar un permiso.

### roles_x_usuarios

1. Crear un rxu.
1. Leer todos los rxu.
1. Leer un rxu en particular.
1. Leer todos los rxu de un usuario.
1. Eliminar un rxu.

### permisos_x_roles

1. Crear un pxr.
1. Leer todos los pxr.
1. Leer un pxr en particular.
1. Leer todos los pxr de un rol.
1. Eliminar un pxr.