## `tail -f` for Windows Powershell
`Get-Content ./log.log -Wait -Tail 10`

## Get HASH of file
`certutil -hashfile "filename"`

By default it will return the SHA1 hash, if you want to use a different hash algorithm;

`certutil -hashfile "filename" <hashalgo>`

Where `<hashalgo>` can be one of;
* MD2
* MD5
* SHA1
* SHA256
* SHA384
* SHA512

## Get HASH of every file in directory
`for %F in (*) do @certutil -hashfile "%F"`

## Get password from app pool
```
cd C:\Windows\System32\inetsrv
.\appcmd.exe list apppool "SmartSearch4" /text:*
```