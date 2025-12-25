# Usuario sin acceso a Internet

## Síntomas
Situacion donde un o varios usuarios indican que no puede navegar por Internet.
Nos indican que los equipos están encendidos y conectados a la red WiFi o cableada correctamente.

## Posibles causas
- Problema de conectividad local, implicaria cables desconectados, WI-FI desactivando o hardware dañado.
- Dirección IP incorrecta, conficlo de IP, mascara de subred erronea o falta de respueta DHCP.
- Fallo en DNS, el equipo no puede traducir URLs en direcciones IP.
- Problema con el router o gateway, el router no responde a las solicitudes de salida hacia internet.

## Diagnóstico - basado en modelo OSI
Capa 1 (Fisica)- Falla de medio fisico, cable dañado, tarjeta de red desactivada o falta de señal WI-Fi
Capa 3 (Red) - Fallo de direccionamiento, el equipo tiene una IP APIPA (169.254.x.x) o un conflico con la IP estatica.
Capa 3 (Red) - Fallo de Getaway, el equipo tiene IP, pero la puerta de enlace (router) no responde o esta mal configurada.
Capa 7 (Aplicacion) - Fallo de resolucion DNS, la conexion es funcional, pero el sistema no puede traducir nombres.

## Solución
1. Verificar capa fisica, revisar estado de la interfaz
2. Validacion de IP, comprobar que la direccion sea valida. 
3. Prueba de salto local, realizar ping al gateway, ping a la ip de router, si falla aca, el problema esta en la red local o el router mismo.
4. Prueba de conectividad externa, ping a la IP publica, si este ping funciona pero el navegador no, el problema es del DNS
5. Realizar un nslookup a una direccion, si no devuelve IP, el servidor DNS configurado esta caido o es incorrecto.

## Prevención
- Checklist básico de conectividad, verificar que otros dispositivos en la misma red funcionen
- Documentar configuración correcta de red, registrar la solucion para futuros incidentes similares
- Capacitar al usuario en detección básica del problema, verificar si el firmware del router o drivers de red estan actualizados.
