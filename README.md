# Demo Log Net Core

### Paquete Nuget - ya instalado

* Serilog.AspnetCore

### Configuración utilizada en el ejemplo

```javascript

{
  "Serilog": {
    "MinimumLevel": {
      "Default": "Information",
      "Override": {
        "Microsoft": "Warning",
        "Microsoft.Hosting.Lifetime": "Information"
      }
    },
    "WriteTo": [
      {
        "Name": "File",
        "Args": {
          "path": "./logs/log-.txt",
          "rollingInterval": "Day",
          "retainedFileCountLimit": "10"
        }
      }
    ]
  },
  "AllowedHosts": "*"
}


```

La rotación de archivos se hace por día *(rollingInterval:"Day")* y se retienen los últimos 10 archivos *(retainedFileCountLimit:"10")*


### Referencias

https://github.com/serilog/serilog-aspnetcore
