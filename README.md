# Registry Service

Eureka Server para service discovery y registro de microservicios.

## Descripción
Servicio de registro y descubrimiento de microservicios que permite:
- Registro automático de servicios en el ecosistema
- Descubrimiento dinámico de instancias de servicios
- Load balancing y alta disponibilidad
- Health monitoring de servicios registrados

## Funcionalidades
- **Service Registry**: Registro automático de todos los microservicios
- **Service Discovery**: Resolución de nombres de servicios
- **Health Monitoring**: Verificación del estado de servicios registrados
- **Dashboard**: UI web para visualizar servicios registrados

## Ejecutar

### Desarrollo Local
```bash
./gradlew bootRun --spring.profiles.active=dev
