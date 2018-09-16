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

Versoes
```
ProductVersion   FileVersion      FileName
--------------   -----------      --------
1.0.20105.407    1.0.20105.407    C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\System.web.helpers.dll
3.0.20105.0      3.0.20105.0      C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\System.web.mvc.dll
1.0.20105.407    1.0.20105.407    C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\system.web.razor.dll
1.0.20105.407    1.0.20105.407    C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\system.web.webpages.deployment.dll
1.0.20105.407    1.0.20105.407    C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\System.web.webpages.dll
1.0.20105.407    1.0.20105.407    C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\System.web.webpages.razor.dll
1.0.20105.407    1.0.20105.407    C:\vagrant\sitedocker\dll\ICareCustomerInteractionUI\bin\microsoft.web.infrastructure.dll
```

