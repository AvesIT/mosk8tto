# THIS IS NOT DONE YET

# Mosquitto

This helm chart installs mosquitto version v1.5.1
https://github.com/eclipse/mosquitto

## ConfigMap customization
Since we want to have a customizable chart it's important that the configmap is a template and not a static file.
To do this we add the keyword `tpl` when reading the file
- {{ (tpl (.Files.Glob "configuration/").AsConfig .) | indent 2 }}


### Configuration
Please change the values.yaml according to your setup

Parameter | Description | Default | Required
--- | --- | --- | ---
`example` | Example parameter  | `nil` | yes

## How to
```
helm install --name mqtt --namespace mosquitto .
```

