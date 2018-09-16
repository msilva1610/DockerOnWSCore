# Powershell

### Ver as versões das DLLs do dotnet

```
get-childitem * -include *.dll,*.exe | foreach-object { "{0}`t{1}" -f $_.Name, [System.Diagnostics.FileVersionInfo]::GetVersionInfo($_).FileVersion }
```
### Ver as versões das dlls com um comando mais simplificado
```
dir *.exe | %{ $_.VersionInfo }
```

### Abrir uma nova janela do powershell

```
Invoke-Item C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
````

### Abrir o conteúdo do arquvio com powershell

````
Get-Content -path 'c:\iislog\W3SVC\u_extend1.log' -Tail 1 -Wait
````

### Chamar uma URL com powershell
```
Invoke-WebRequest http://localhost -UseBasicParsing
````

