#AWS

7 modulos de [AWS technical Essential](https://explore.skillbuilder.aws/learn/course/1851/play/85986/aws-technical-essentials)
- `Intriduccion a AWS`
- `computo AWS`
- `AWS networking`
- `Servicios de almacenamiento` (AWS Storage)
- `Base de datos`: (Amazon dynamoDB)
- `Monitorizacion, servicio de balanceo de carga y autoescalado` (balanceadores de carga)
- `Seguridad en AWS`

### Recursos

builder LABS
BookShelf

## Intriduccion a AWS

#### infraestructura global AWS

Regiones ubicaiones geograficas, para escoger una buena region hay que ver la `data compliance` que la empresa cumpla con el cumplimiento de la region, `Latencia` es la segunda cosa importante, `service alailability`, `Precio`.
las regiones tiene zonas de disponibilidad.
zona de disponibilidad, pensado para que las empresas puedan desplegar su area de trabajo o su solucion.



#### Availability Zones
#### Edge locations
#### Service managent
- AWS management console
- AWS command line Interface (AWS CLI)
- AWS Software development kits (SDKs)

### Security and  the AWS shared responsibility model
### AWS identity and Access management (IAM)
    - IAM
    - IAM features -> global, integrated with AWS services, Shared access to your AWS account, Multi-Factor authentication (MFA), Identity federation, Free to use
    - AWS root user
    - IAM policies -> estructura JSON, principio de minimo privilegio
    - IAM groups 
    - IAM roles (usar credenciales mediante roles, es recomendado), hacer que AWS us servicion en tu nombre, cuando se llama a una api se asume un rol.    
### 
## Modulo 2 aws computing

### amazon EC2

que son los AMI amazon machine image
### Amazon EC2 instance lifecycle
- amazon EC2 instance types: general purpose, compute optimized, memory optimized, accelerated computing y storage optimized.
### amazon EC2 Pricing

- AWS free tier
- saving plans: planes de ahorro que te cobran por un instancia y el tiempo empieza a correr
- dedicated host: es como reservar un host y no ir cambiando un ip diferente, al usar una licencia que solo se ejecute en un predeterminado lugar
- reserved instances: puedes reservar instancias por cierto tiempo limitado, lo usas un cierto tiempo y lo que te sobra de tiempo se sigue guardando
- on-demand instances:
- spot instances: 
te dejan instancia micro t2 o  t3 gratuitas mediante 700 horas
### container services
 - AWS containers orchestration services
### Serveless
- AWS Lambda: se dispara mediante eventos, escala puede atender miles de solicitudes al mismo tiempo, es un servico computacional, se paga por el uso del servicio y no por el tiempo que esta en servicio sino por el uso
- AWS Fargate
### Knowledge check
