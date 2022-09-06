# HELM

El siguiente ejemplo muestra un deployment inicial (`sample-deployment.yaml`) convertido en template de Helm

## Probar

Para ver que salida genera se puede utilizar el parametro `--dry-run`

```bash
# VALORES DE DESARROLLO
helm install -f ./myapp/desa.yaml myapp-desa ./myapp  -n clase5 --create-namespace --dry-run
# VALORES DE TEST
helm install -f ./myapp/test.yaml myapp-test ./myapp  -n clase5 --create-namespace --dry-run
```

## Crear un char de cero

Para inicializar un Chart desde cero se pude utilizar el comando

```bash
helm create myapp
```

Este ejemplo es una simplificacion de ese comando inicial
