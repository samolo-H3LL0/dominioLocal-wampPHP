# Como hacer un dominio local
SOLO PARA WINDOWS JSJSJSJJJSJSSJJSJSJSJSJS.js

- lo primero de todo es mirar este gato:
![gato ejecutivo](../img/gatoejecutivo.png)

vale ya puedes

## 1. Tener el wamp
tienes que tener el wamp

## 2. Tener el notepad++
tienes que tener el notepad++

## 3. ir al fichero host en system32
toma ruta sovago: [clicka aquii](C:\Windows\System32\drivers\etc\host) host no es un dir ok
si no va copia y pegaa: `C:\Windows\System32\drivers\etc\host`

### si eeres digno tienes que tener esto ya hecho:
```
#
127.0.0.1 localhost
::1 localhost
```

ahora señor mire este ejemplo:
```
#
127.0.0.1 localhost
::1 localhost
569.238.1.34 dominiochulo.local
```

ahora complete esta plantilla:

```
#
127.0.0.1 localhost
::1 localhost
TUIP TUDOMINIO.local
# deja el local :)
```

ahora ve a httpd-vhosts.conf xdxd
toma ruta trivago: `C:\d\s\wamp64\bin\apache\apache2.4.46\conf\extra\httpd-vhosts.conf` (el local no iba xdxd)

y tambien si eres digno pues tendras esto predefinido:

```conf
<Directory "${INSTALL_DIR}/www/">
    Options +Indexes +Includes +FollowSymLinks +MultiViews
    AllowOverride All
    Require local
  </Directory>
</VirtualHost>


```

ahora rellena:
```conf
<
<VirtualHost *:80>
  ServerName TUDOMINIO.local # pon tu dominio. ejemplo: miguelpana.local
  DocumentRoot "C:PON RUTA DE DIR"  # aqui pon el directorio de los archivos php ok
  <Directory "C:PON RUTA DE DIR">
  # aqui lo mismoooo (pon la ruta otra ves)
    AllowOverride All
	Require all granted
	Allow from all
  </Directory>
</VirtualHost>
```
--- 

ahora reinicia wamp o xamp mejor wamp ok 
entonces si sigues leyendo esto programa con php en el directorio lo que te de la gana y escribe en el navegador tu dominio y ya B)


