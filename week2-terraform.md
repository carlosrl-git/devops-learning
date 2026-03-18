# Semana 2 - Terraform

##  Qué he aprendido

He aprendido a utilizar Terraform como herramienta de Infrastructure as Code (IaC), permitiendo definir y desplegar infraestructura mediante código.

##  Conceptos clave

- Provider -> Define el proveedor (Docker, Azure, etc.)
- Resource -> Elementos que se crean (contenedores, máquinas virtuales…)
- Variables -> Permiten reutilizar código
- Outputs -> Muestran resultados tras la ejecución
- State -> Guarda el estado de la infraestructura

##  Comandos importantes

terraform init -> inicializa el proyecto  
terraform plan -> muestra lo que va a crear  
terraform apply -> crea la infraestructura  
terraform destroy -> elimina la infraestructura  

##  Ejercicio realizado

He desplegado contenedores Docker usando Terraform, creando servicios accesibles desde el navegador.

##  Problemas encontrados

Errores al aplicar cambios debido a conflictos en contenedores existentes, solucionado eliminando recursos previos.