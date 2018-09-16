# Powershell

Ver as versões das DLLs do dotnet

```
get-childitem * -include *.dll,*.exe | foreach-object { "{0}`t{1}" -f $_.Name, [System.Diagnostics.FileVersionInfo]::GetVersionInfo($_).FileVersion }
```
### Abrir uma nova janela do powershell

```
Invoke-Item C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe
````

