# Guía de Configuración y Uso de Terraform en AWS

Este repositorio contiene ejemplos y guías para configurar y utilizar Terraform en AWS.

## Requisitos Previos

Antes de comenzar, asegúrate de tener instalados los siguientes elementos:

1. [Terraform](https://developer.hashicorp.com/terraform/install?product_intent=terraform)
2. [AWS CLI](https://aws.amazon.com/es/cli/)

## Configuración del Entorno AWS

Para configurar tu entorno AWS, sigue los siguientes pasos:

1. Crea un usuario específico para Terraform.
2. Crea un grupo para el usuario con permisos sobre EC2, S3, DynamoDB, Route53, IAM y RDS.
3. Genera una clave de acceso para el AWS CLI.
4. Desde el directorio de configuración, ejecuta:
    ```
    aws configure
    ```
    - Introduce el identificador de la clave del CLI.
    - Introduce la clave del CLI.
    - Elige la región del servidor de AWS.
    - Elige el formato de archivo JSON.

## Uso de Terraform

Sigue estos pasos para ejecutar Terraform:

1. Sitúate en la ubicación de tu código `.tf`.
2. Ejecuta el comando:
    ```
    terraform init
    ```
    Esto generará un backend ubicado en la carpeta `.terraform`.
3. Luego, ejecuta:
    ```
    terraform plan
    ```
    Esto generará un plan con los detalles especificados en el fichero.
4. Para aplicar el plan, ejecuta:
    ```
    terraform apply
    ```
    Confirma los datos obtenidos en el plan para crear la instancia.
5. Si deseas eliminar la instancia previamente creada, ejecuta:
    ```
    terraform destroy
    ```

## Repositorio de Ejemplo

Este repositorio se ha creado como parte del curso de Terraform en DevOps Directive. Puedes encontrar el código de ejemplo y ejercicios relacionados [aquí](https://github.com/sidpalas/devops-directive-terraform-course).
