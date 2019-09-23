# LARAVEL 5.5

### Instalar Laravel
 ```
    composer global require "laravel/installer"
```

### Crear proyecto
 ```
    composer create-project laravel/laravel[="5.1"] nomProyecto
    cd nomProyecto
```
ó
 ```
    laravel new nomProyecto
    cd nomProyecto
    php artisan key:generate
```
 
### Laravel Mix
 ```
    npm install
    npm run dev    /    npm run watch
```

### Rutas
En el fichero \routes\web.php

### Model
 ```
    php artisan make:model nomModel [-mfcr]
```
		nomModel en singular y mayuscula
		m - migration
		f - factory
		c - controller
		r - resource controller
		a - =mfr
		p - pivot table
		
En el modelo hay que definir los registros accesibles desde el exterior. En la clase:

    protected $fillable = ['name', 'position', ...];

### Migration
 ```
    php artisan make:migration create_nomtabla_table
```
*nomtabla* en minuscula plural

Para modificar una tabla ya creada (por ejemplo añadir nuevo campo *avatar* a tabla *users*):
 ```
    php artisan make:migration add_avatar_to_users
 ```
 y en el fichero de migracion:
```
    $table->string('avatar')->nullable()->after('password');
```



