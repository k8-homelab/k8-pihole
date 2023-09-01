# K8-pihole

## What it does
Installs pihole 

## How to configure for you
Be sure to update, or remove, the admin secret [sealed-secret.yaml](helm/templates/sealed-secret.yaml)

Modify the files in [values.yaml](helm/values.yaml) to customize to your environment.  

```
namespace: your-custom-namespace
storageClassName: your-storage-class

timeZone: "America/New_York"
dnsServers: "10.0.10.1;10.0.20.1"

ingressDns: pihole.example.com
ingressTlsSecret: your-custom-tls

# Where DNS port 53 will listen.  metallb.
metallbIP: "10.0.10.250/32"
```

## Install
`skaffold deploy`

