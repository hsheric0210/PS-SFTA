# PowerShell SFTA

[![Latest Version](https://img.shields.io/badge/Latest-v1.2.0-green.svg)]()
[![MIT License](https://img.shields.io/github/license/mashape/apistatus.svg)]()
[![Made with Love](https://img.shields.io/badge/Made%20with-%E2%9D%A4-red.svg?colorB=11a9f7)]()


PowerShell Set File/Protocol Type Association Default Application Windows 10/11


## Features
* Set File Type Association.
* Set Protocol Association.
* Get File Type Association.
* List File Type Association.
* Get Protocol Type Association.
* List Protocol Type Association.
* Register Application.
* Unregister Application.

## Usage
##### Type Get-Help command for information
```powershell
Get-Help .\SFTA.ps1 -full
```

## How to import?
```powershell
. .\SFTA.ps1
```

## Basic Usage

##### Set Acrobat Reader DC as Default .pdf reader:
```powershell
Set-FTA AcroExch.Document.DC .pdf

```

##### Set Sumatra PDF as Default .pdf reader:
```powershell
Set-FTA Applications\SumatraPDF.exe .pdf

```


##### Set Google Chrome as Default for http Protocol:
```powershell
Set-PTA ChromeHTML http

```

##### Register Application and Set as Default for .pdf reader:
```powershell
Register-FTA "C:\SumatraPDF.exe" .pdf -Icon "shell32.dll,100"

```

## Additional Instructions

##### Set Sumatra PDF as Default .pdf reader from Windows Command Processor (cmd.exe):
```powershell
powershell -ExecutionPolicy Bypass -command "& { . .\SFTA.ps1; Set-FTA 'Applications\SumatraPDF.exe' '.pdf' }"

```

## Warning!
### This tool can't change file type description!
#### To change file type description, open regedit and edit <u>default value</u> of **HKEY_CLASSES_ROOT\\{ProgID}**


## Release History
See [CHANGELOG.md](CHANGELOG.md)


<!-- ## Acknowledgments & Credits -->


## License

Usage is provided under the [MIT](https://choosealicense.com/licenses/mit/) License.

Copyright © 2022, [Danysys.](https://www.danysys.com)