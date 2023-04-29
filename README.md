# InvokeSQL

🍴 from https://github.com/Tervis-Tumbler/InvokeSQL. Described in https://stackoverflow.com/a/18935548/17273131

## Installation
Windows:
```powershell
cd ~/Documents/Powershell/Modules
git clone https://github.com/kkostrzewa-coupa/InvokeSQL
```

## Usage
```powershell
Invoke-MSSQL -Server localhost -database master -SQLCommand "select 1"

($h,$u,$p,$d)=@('>IP<,>PORT<','>USERNAME<','>PASSWORD<','>DATABASE<'); Invoke-MSSQL -Server $h -Credential (New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $u,(ConvertTo-SecureString -String $p -AsPlainText -Force)) -Database $d -SQLCommand 'select @@servername,db_name()'
```
