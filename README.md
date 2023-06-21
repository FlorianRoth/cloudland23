# CloudLand 2023

## Login

```sh
ssh <ip>@5022
```

## Login in CloudFoundry

```sh
cf api localhost --skip-ssl-validation
cf auth cloud-land
```

## Organisationen anzeigen

```sh
cf orgs
```

## Spaces anzeigen

```sh
cf spaces
```


## Space auswählen

```sh
cf target -o tutorial -s dev
```


## Apps im ausgewälten Space anzeigen

```sh
cf apps
```
## Services im ausgewälten Space anzeigen

```sh
cf services
```

## Demp-App clonen

```sh
mkdir <mein Ordner>
cd <mein Ordner>
git https://github.com/cloudfoundry-tutorials/korifi-sample-app
```

## Manifest anpassen

- `manifest.mf` bearbeiten
- App Namen anpassen
- Service `credentials` binden

```yaml
---
  services:
   - credentials
```

## App pushen

```sh
cf push -f manifest.yml
```

## Apps aufrufen

```sh
wget https://<appname>.apps-127-0-0-1.nip.io
```

## Logs anschauen

```sh
cf logs <appname>
```

## Sonstige Commands

- `cf scale`
- `cf delete`
- `cf restart`
