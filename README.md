El server se corre con npm start.
Cree un sistema de login con passport y de register en un controller, a su vez en la vista de login agregue ultimamente la opcion de restablecer la contraseña
La opcion de restablecer la contraseña te manda un correo al mail que vos pones y dentro del correo un link para poner la nueva contraseña
Mi sistema de roles son: user, premium y admin; para registrarse teniendo cada rol tiene que terminar el mail en @admin.com o @premium.com
Ya con el usuario creado para cambiar de rol solo se puede optar en pasar de user a premium o al reves, nunca a admin.
El cambio de rol se encuentra dentro del perfil de cada user o premium.
Hice un middleware de actualizacion de las credenciales en cada request que hay una vez iniciada sesion
Dentro de la vista perfil muestra toda la info incluyendo carrito y productos previamente agregados
Si es admin tiene la opcion exclusiva de ver todos los usuarios registrados en la aplicacion y de a su vez borrar cualquier usuario
En la vista de productos muestra todos los productos agregados y quien los agrego, solo pueden ser agregados por premium o admin.
El producto agregado solo puede ser comprado por otra persona, es decir no lo puede agregar al carrito el propietario del producto
A su vez tampoco se puede borrar un producto de otra persona solo propio
Al apretar finalizar compra se genera un ticket en la base de datos y se resta el stock de los productos disponibles

