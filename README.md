# Capa de abstracción para manejo de sesiones en PHP

**Instalación vía composer**

`composer require ligne/session`

**Uso básico:**
En cuanto de instancia la clase se abre una nueva sesión.
```php
$session = new SessionsController();
```
**Para crear una nueva sesión se utiliza el método `set()`**
```php
$session->set('foo','bar');
```
O
```php
$session->set('foo','bar')
        ->set('last_activity', date('Y-m-d h:i:s') )
	->set('user_id','1');
```

**Para acceder a esta sesión se utiliza el método `get()'**
```php
$session->get('foo');
#out
'bar'
```

**Para remover una sesión se utiliza el método `remove()`**
```php
$session->remove('foo');
```
O
```php
$session->remove('foo')
        ->remove('user_id');
```
O puedes remover todas las sesiones, perfecto para un logout:
```php
$session->destroy_all_session();
```
## Otros métodos útiles son:
```php
$session->id(); 		//Retorna el ID de la sesión actual
$session->get_all(); 		// Retorna un array con todas las sesiones existentes
```

