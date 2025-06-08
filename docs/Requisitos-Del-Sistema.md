# Requisitos del Sistema - CloudLab

## 🎯 Objetivo General

Desarrollar un sistema de gestión de infraestructura física que permita a los usuarios aprovisionar y gestionar máquinas físicas de manera similar a Amazon EC2.

## 📋 Requisitos Funcionales

### RF01 - Gestión de Usuarios
- **RF01.1**: El sistema debe permitir registro de usuarios
- **RF01.2**: El sistema debe autenticar usuarios mediante credenciales
- **RF01.3**: El sistema debe gestionar perfiles de usuario
- **RF01.4**: El sistema debe implementar control de acceso por roles

### RF02 - Gestión de Instancias
- **RF02.1**: Los usuarios deben poder listar instancias disponibles
- **RF02.2**: Los usuarios deben poder crear nuevas instancias
- **RF02.3**: Los usuarios deben poder iniciar/parar instancias
- **RF02.4**: Los usuarios deben poder terminar instancias
- **RF02.5**: Los usuarios deben poder acceder a instancias vía SSH

### RF03 - Monitoreo y Logs
- **RF03.1**: El sistema debe mostrar estado en tiempo real de las instancias
- **RF03.2**: El sistema debe registrar logs de operaciones
- **RF03.3**: El sistema debe mostrar métricas de recursos (CPU, RAM, Disco)
- **RF03.4**: El sistema debe generar alertas por problemas

### RF04 - Gestión de Red
- **RF04.1**: El sistema debe asignar IPs dinámicamente
- **RF04.2**: El sistema debe gestionar reglas de firewall básicas
- **RF04.3**: El sistema debe permitir conectividad SSH entre instancias

### RF05 - Interfaz Web
- **RF05.1**: Dashboard principal con vista general
- **RF05.2**: Panel de gestión de instancias
- **RF05.3**: Panel de monitoreo y métricas
- **RF05.4**: Interfaz responsive para dispositivos móviles

## ⚙️ Requisitos No Funcionales

### RNF01 - Rendimiento
- El sistema debe soportar al menos 10 usuarios concurrentes
- Las operaciones de instancia deben completarse en menos de 30 segundos
- La interfaz web debe cargar en menos de 3 segundos

### RNF02 - Disponibilidad
- El sistema debe tener una disponibilidad del 95%
- El servidor maestro debe reiniciarse automáticamente en caso de fallo

### RNF03 - Seguridad
- Todas las comunicaciones deben usar HTTPS/SSH
- Las contraseñas deben estar hasheadas
- Logs de auditoría para todas las operaciones críticas

### RNF04 - Usabilidad
- Interfaz intuitiva que no requiera entrenamiento
- Documentación completa para usuarios finales
- Mensajes de error claros y accionables

## 🖥️ Requisitos de Hardware

### Servidor Maestro
- **CPU**: Mínimo 4 cores
- **RAM**: Mínimo 8GB
- **Almacenamiento**: 500GB SSD
- **Red**: Puerto Gigabit Ethernet
- **OS**: Ubuntu Server 22.04 LTS

### Máquinas Físicas (20 unidades)
- **CPU**: Mínimo 2 cores
- **RAM**: Mínimo 4GB
- **Almacenamiento**: 250GB HDD
- **Red**: Puerto Ethernet
- **OS**: Ubuntu Server 22.04 LTS (instalación automática)

### Infraestructura de Red
- Switch gestionable 24 puertos
- Router con acceso a internet
- Cableado Cat6

## 🔧 Requisitos de Software

### Stack Tecnológico Recomendado
- **Frontend**: React.js + TypeScript
- **Backend**: Node.js + Express.js o Python + FastAPI
- **Base de Datos**: PostgreSQL o MongoDB
- **Orquestación**: Ansible + Scripts personalizados
- **Monitoreo**: Prometheus + Grafana
- **Contenedores**: Docker (opcional)

### Herramientas de Desarrollo
- **Control de Versiones**: Git + GitHub
- **CI/CD**: GitHub Actions
- **Testing**: Jest (Frontend), Pytest (Backend)
- **Documentación**: Markdown + GitHub Wiki

## ✅ Criterios de Aceptación

1. **Funcionalidad Core**: Usuarios pueden crear, iniciar, parar y terminar instancias
2. **Interfaz Completa**: Dashboard funcional con todas las operaciones básicas
3. **Monitoreo**: Métricas en tiempo real de todas las instancias
4. **Documentación**: Documentación técnica y de usuario completa
5. **Pruebas**: Cobertura de pruebas mínima del 70%
6. **Despliegue**: Sistema desplegado y accesible desde internet

## 🚫 Fuera del Alcance (V1.0)

- Balanceadores de carga
- Auto-scaling
- Snapshots/Backups automáticos
- Almacenamiento distribuido
- Redes virtuales complejas
- Integración con proveedores cloud externos

---
*Documento actualizado: 2025-06-08*
