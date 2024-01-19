# Barcodeapp

## Create Docker image

>```podman build -t barcodeapp_backend .```

## Running image

>```podman run -p 9000:9000 --name barcodeapp_backend -v /Users/neuronacreativa/developer/php/barcodeapp/backend:/var/www/html barcodeapp_backend```

## Entering container

>```podman exec -it barcodeapp_backend bash```

## Starting containers composer via

>```podman compose up -d```
