# Registry Service

Servicio de registro y descubrimiento de microservicios usando Netflix Eureka.

## Funcionalidades

- **Registro automático**: Microservicios se registran al iniciar
- **Descubrimiento dinámico**: Localización automática de servicios
- **Balanceo de carga**: Distribución de requests entre instancias
- **Monitoreo de salud**: Detección automática de servicios caídos
- **Dashboard web**: Interfaz visual para ver servicios registrados

## Dashboard

- **URL**: `http://localhost:8761`
- **Vista**: Lista de aplicaciones registradas con instancias
- **Estados**: UP (activo), DOWN (inactivo), STARTING (iniciando)

## Configuración Docker

- **Puerto**: 8761
- **Modo**: Servidor Eureka (no cliente)
- **Hostname**: `registry-service`
- **Perfil**: docker

## Configuración

```yaml
server:
  port: 8761
eureka:
  instance:
    hostname: registry-service
  client:
    register-with-eureka: false
    fetch-registry: false
```

## Servicios Registrados

- **GATEWAY-SERVICE**: API Gateway
- **MS-PRODUCTOS**: Microservicio de productos
- **MS-PEDIDOS**: Microservicio de pedidos (futuro)
- **CONFIG-SERVER**: Servidor de configuración

## Despliegue

```bash
docker-compose up --build registry-service
```

## Health Check

- Endpoint: `http://localhost:8761`
- Estado: Dashboard accesible = Servicio saludable

## Notas

- Debe iniciarse antes que otros microservicios
- No se registra a sí mismo en Eureka
- Es independiente de la base de datos