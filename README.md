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


# Project Titl

host fisico donde se almacenan las instancias
cunado se selecciona una AMI se tiene que enlazar un volumen de arranque
Cuando se lanza una instancia EC2  se comunica con una EBS cuando se pierde la conexion se pierde el host y se despliega en otro host y se conecta con el EBS.

otro tipo de instancia de conexion tienen junto un almacen de instancias dentro de un host esto es peligroso asi que se debe tenerlo con datos que no interesan perder 

EBS = IOPS

instance store = Millones

[ ¿Cuáles son las mejores prácticas para acceder a mi instancia EC2 Linux de forma segura usando SSH y evitando el acceso no autorizado ?](https://repost.aws/es/knowledge-center/ec2-ssh-best-practices)
[Ejecutar comandos en su instancia de Linux durante el lanzamiento .](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/user-data.html)

Detención/inicio de instancia: cuando detiene su instancia, ingresa al estado Detención y luego al estado Detenido . Cuando detiene e inicia su instancia, pierde todos los datos de los volúmenes de almacenamiento de instancias en el equipo host anterior. Sin embargo, la instancia conserva su dirección IPv4 privada, lo que significa que una dirección IP elástica asociada con la dirección IPv4 privada o la interfaz de red aún está asociada con su instancia. Si su instancia tiene una dirección IPv6, también conserva su dirección IPv6.

Reinicio de instancia: también puede reiniciar su instancia mediante la consola de Amazon EC2. Reiniciar una instancia equivale a reiniciar un sistema operativo. La instancia permanece en el mismo equipo host y conserva su nombre DNS público, su dirección IP privada y todos los datos en sus volúmenes de almacenamiento de instancias. Por lo general, el reinicio demora unos minutos en completarse, pero el tiempo que demora depende de la configuración de la instancia.

Hibernación de instancia: cuando hiberna una instancia, le indicamos al sistema operativo que realice la hibernación (suspensión en disco), que guarda el contenido de la memoria de la instancia (RAM) en su volumen raíz de Amazon EBS. Conservamos el volumen raíz de Amazon EBS de la instancia y cualquier volumen de datos de Amazon EBS adjunto. Cuando inicia su instancia, el volumen raíz de Amazon EBS se restaura a su estado anterior y el contenido de la RAM se vuelve a cargar. Los volúmenes de datos adjuntos anteriormente se vuelven a adjuntar y la instancia conserva su ID de instancia. Su instancia también conserva su dirección IPv4 privada, lo que significa que una dirección IP elástica asociada con la dirección IPv4 privada o la interfaz de red aún está asociada con su instancia. Si su instancia tiene una dirección IPv6, conserva su dirección IPv6.

Terminación de instancia: cuando haya decidido que ya no necesita una instancia, puede terminarla. Tan pronto como el estado de una instancia cambie a apagado o terminada, dejará de incurrir en cargos por esa instancia. Después de terminar una instancia, permanece visible en la consola por un breve tiempo y luego la entrada se elimina automáticamente.

### gateway

### gateway NAT

## Amazon VPC routing

Servicio GuardDuty(invest)
Servicio defensi(invest)
Elastic benistalk(invest)
Curso -> crear una vpc con igw -> crear subredes -> dentro de la zona de disponibilidad -> crear 4 subres con ip diferentes -> Generar una propia tabla de rutas  -> 

## Network acces control list and security groups

### NACL = Network acces control list
consiste en reglas, entrada y salida. 

exiten 2 estipos de cortafuegos
Stateless
con estado: 
sin estado: es capaz de recordar la conexion, permiten reglas allow y deny, 
### security groups
#### Estos es creando VPC -> configurar security groups
caracteristicas: cortafuegos con estado(state full), reglas solo Allow.
caracteristicas del grupo default: deniega todo el trafico entrante, permite el trafico del mismo grupo default (hablando de las instacias) 

## security at every layer

buenas parcticas de red: hacer que el entorno sea disponible, permitir los puertos que se utilicen, utilizar IAM, utilizar flow  logs 

# module 3 
#Laboratorios
lauching amazon EC2 instance

creating a VPX and lauching a web application in an Amazon EC2 instance



# Modulo 4

- AmazonS3 (para examen)
- 4 tipos de cifrado (para examen)
### storage types
- block storage
- file storage
- object storage
#### block storage
#### file storage
#### object storage (inmutabilidad )

inmutabilidad es una caracteristica que hace que tu tengas que descomprimir.
### Amazon file sistem (EFS)

- IAM policy
- bucket policy
- S3 block public access
- Amazon S3 encryption

ACLs se usa para un caso en concreto, metodo antiguo.
### Amazon s3 storage classes

- Amazon s3 standar
- Amazon S3 infrequent Access
- Amazon S3 one zone-infrequent Access
- Amazon S3 Glacier

    - instant retrival
    - Flexible retrival
    - Deep archive
### Amazon s3 versioning 

un objeto cuando se versiona puede actualizar y se sobrescribe una nueva version y es la que se muestra en la lsta pero puedes observarlo activando todas las versiones. 

- EBS
- EFS
- S3

# Module 5, Databases

### beneficios de BBDD de AWS
- Purpose-built
- Performance at scale
- Fully managed
- Secure and highly available
#### Tipos Database
- Relacionales -> amazon Aurora, amazon RDS, amazon redshit
- key-value -> amazon dynamoDB
- In-memory -> amazon elasticache for memcached, Amazon Elsticache for redis
- document -> Amazon documentDB
-  wide column -> Amazon keyspaces
- Graph 
- Time series
- ledger

#### Base de datos Relacionales
Beneficios:

Complex SQL, Reduced redundancy, Familiarity, ACID principle
# 
**Amazon RDS**

### DB instances clases 
- Standard
- Memory optimized
- Birstable Performance

### DB instances storage

- general ssd
- hdd

### Database backup

Automatic<----Snapshot----> Manual

### Redundancy with Amazon RDS Multi-AZ
-   Despliegue mediante red replicas, se suben los datos de forma asyncrona

### Conceptos de Aurora | es RDS -> (Examen) 

Motor de despliegue que tiene una compatibilida Mysql(x5 de rendimiento) o postSQL (X3 rendimiento).

cada maquina lleva maquina computacional y tambien tiene su volumen, Aurora funciona con cluster

Se puede montar una replica que son solo de Lectura (read), diferencia -> conmutan por error (si existe un error en la principal) max -> 15 replicas

Replicas de RDS se autoescalan vs aurora 

existe la posibilida de crear aurora multiMaster

## Laboratorios 
Introduction to Amazon EC2

### Laboratorio

#### introduction to amazon ec2 auto scaling

### (LAB) Developing on AWS - Supplemental Lab Playlist
### (Course) Digital classroom developing on AWS

Requisitos para developing 

- AWS cloud practitioner Essentials
- AWS Technical Essentials
- Bassic 


### Accesing AWS services programmatically


autentificacion -> Consola (usuario/contraseña) o programatica -> 

(http)
(SigV4)-> protocolo de acceso es para firmar tu identidad
IAM, Access Key (ID, Secret)


Cliente application
                                            
                                          |-----
AWS managenement--|                       |
AWS CLI-----------|---Aws REST API -------|-----
SDKs--------------|                       |
                                          |-----


Herramienta de desarrollos para
(acceder con SDKs)
- `python`
- `.NET`
- `Java`
- `C++`
- `Ruby`
- `JavaScrip`
- `GO`
- `Node JS`
- `PHP`

### Conectarse a la CLI de AWS
- `EC2 over SSH/PuTTY`
- `AWS cloud9`
- `AWS cloud Shel`
- `AWS systems manager session`

### Kit de desarrollo y patrones programaticas

### Amazon Q Developer ---ANTES---> Amazon code Whisperer

# IAM

## [How IAM work](https://online.vitalsource.com/reader/books/200-DODEVA-45-EN-SG-E/pageid/96)
Casos de uso de IAM
- asignacion de roles
- roles entre cuentas
-
(movaterm)
como determinar la politicas aplicables, crear un rol on id,

## Como otorgar permisos IDE / IDE configuration

cognito vs IAM??? contexto: quiero desplegar una app movil o una web que servicio escoger??

### Lab 
[Lab 1 (Python) - Configure the Development Environment](https://us-east-1.student.classrooms.aws.training/class/9SmATHY6nQ1rBZTHAdWkMV)

### puntos de control

**cifrado de datos**

transito -> Protocolo transito , certificado TLS, Cs3(cloud side encrypton) -> ( VPN )

Repososo

- CSE
- SSE (servidor-side encrypton)


### Amazon s3 store and retrive any amount of data from anywhere

#### Primer tipo de cifrado: 
- SSE-S3 usa una clave para una region la cual todos los clientes de la region puede utilizar
- Se comparte la misma clave
#### Segundo tipo de cifrado: SSE-KMS
- SSE-KMS(key management service), servicio para la administracion de material criptografico, se puede custodiar claves maestras utilizadas para un cifrado simetrico y asimetrico.
- KSM encryp, KSM decript y KSM generate data key
- Una master Key puede ser administrada por el cleinte(tiene coste) o por AWS, esta se encarga de rotarlas(ejemplo 'aws/s3', no tiene un coste).
- Se paga por llamadas a la api
- cifra 4kb (data key)
- Habilitar bucket key
#### Tercer tipo de cifrado:  DSSE-KMS
- 
#### Cuarto tipo de cifrado:  
- Cifrado del lado del servidor de doble capa
#### Quinto tipo de cifrado:  SSE-C
- AWS no tiene la custodia de  la Key
- El cliente tiene control sobre la Key (custodia on-promiese)
- Utiliza el protocolo htttps
- Se hace un get desde la app  a S3 para encriptar los ficheros

### Caracteristicas de S3

- Transfer acceleration, se utiliza para cargar objetos en la ubicacion de borde (edge-location) mas cercana las cuales son puntos donde al llegar la informacion los datos se envian por la red privada de AWS
-  Object Lock, se habilita a nuvel de bucket con una politica de acceso WORM, Requiere que el objeto este versionado o creado, una vez realizado no se puede cambiar, se puede habli  la retencion y se puede hababilitar 2 modos, **Governance** o **Compliance**, bloquea la eliminacion de buckets, se define un periodo de retencion.
- bloqueo de bucket (legalbold) 

### CORS 
- S3 nos permite validar las politicas de CORS 
- Entre dominio diferentes, entre mismos dominios no funciona
- Lo implementa los navegadores web
### como interactuar mediante la CLI

### Interacting with Amazon S3 through SDKs
1. Configure Amazon S3 settings for the SDK.
2. Define dependencies. 
3. Create an S3 client (service reference) to make service requests.
4. Perform operations.
5. Close the S3 client connection.

### Conocer a profundidad para el examen

dynamodb
lamda
cognito
s3
IAM
