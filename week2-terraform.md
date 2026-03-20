# Semana 2 - Terraform (Infraestructura como código)

##  Qué he aprendido

He aprendido a utilizar Terraform para crear infraestructura mediante código, evitando configuraciones manuales. He trabajado con Docker como provider para desplegar contenedores y entender cómo funciona la automatización de recursos.

---

##  Conceptos clave

### Providers

Son los proveedores con los que trabaja Terraform.

Ejemplo:

* Docker
* Azure
* AWS

 Permiten interactuar con servicios externos

---

### Resources

Son los elementos que queremos crear.

Ejemplo:

* contenedores
* máquinas virtuales
* redes

 Es el núcleo de Terraform

---

### Variables

Permiten hacer el código dinámico.

 En lugar de valores fijos, se pueden reutilizar

---

### Outputs

Muestran información después de ejecutar Terraform.

 Sirven para ver resultados (nombre, IP, etc.)

---

### Terraform State

Archivo donde Terraform guarda el estado de la infraestructura:

```text
terraform.tfstate
```

 Importante:

* guarda lo que se ha creado
* permite saber qué modificar

---

##  Comandos utilizados

```bash
terraform init
```

-> inicializa el proyecto

```bash
terraform plan
```

-> muestra lo que se va a crear

```bash
terraform apply
```

-> ejecuta la infraestructura

```bash
terraform destroy
```

-> elimina todo lo creado

---

##  Ejercicio práctico realizado

Se ha desplegado un contenedor Nginx utilizando Terraform.

Ejemplo de configuración:

```hcl
provider "docker" {}

resource "docker_container" "nginx" {
  name  = "mi-nginx"
  image = "nginx"

  ports {
    internal = 80
    external = 8080
  }
}
```

---

##  Resultado

* Contenedor creado automáticamente
* Acceso vía navegador:

```text
http://localhost:8080
```

 Se comprobó que el servicio web funcionaba correctamente

---

##  Ejercicios realizados

* Creación de infraestructura con Terraform
* Uso de Docker como provider
* Ejecución de contenedores mediante código
* Uso de terraform plan para validar cambios
* Aplicación de infraestructura con terraform apply

---

##  Problemas encontrados

* Error en terraform apply
  -> solucionado revisando sintaxis del archivo .tf

* Conflictos de puertos en Docker
  -> solucionado cambiando puerto externo

* Cambios no reflejados
  -> solucionado usando terraform plan antes de apply

---

##  Conclusión

Terraform permite automatizar completamente la infraestructura.

 Ventajas:

* evita errores manuales
* permite repetir configuraciones
* facilita el trabajo en equipo

 Es una herramienta clave en DevOps junto con Docker y Git
