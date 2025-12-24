# ZebraPuma-Packages
This repository hosts the NuGet packages for ZebraPuma libraries via GitHub Packages.

[![.NET Framework 4.8](https://img.shields.io/badge/.NET%20Framework-4.8-blue.svg)](https://dotnet.microsoft.com/download/dotnet-framework/net48)
[![.NET](https://img.shields.io/badge/.NET-10.0-purple.svg)](https://dotnet.microsoft.com/download/dotnet/10.0)

## 📦 Available Packages

- **ZebraPuma.Plugins** - Base plugin system library
- **ZebraPuma.System.ServiceProcess** - Windows Services and Windows Forms management

## 🔧 Installation

### 1. Configure GitHub Packages source
dotnet nuget add source https://nuget.pkg.github.com/ZebraPumaOrg/index.json 
-n "ZebraPuma" 
-u "YOUR_GITHUB_USERNAME" 
-p "YOUR_GITHUB_TOKEN" 
--store-password-in-clear-text


Replace `YOUR_GITHUB_USERNAME` and `YOUR_GITHUB_TOKEN` with your GitHub credentials.

### 2. Install packages

dotnet add package ZebraPuma.Plugins --version 2.0.0 dotnet add package ZebraPuma.System.ServiceProcess --version 2.0.0


## 🔑 GitHub Personal Access Token

To access these packages, you need a GitHub Personal Access Token with `read:packages` scope.

Create one here: https://github.com/settings/tokens

## 📚 Documentation

For more information, see the [ZebraPuma repository](https://github.com/ZebraPumaOrg/ZebraPuma).






## Licensing / Licence / Licentie

**Proprietary — All rights reserved.**  
Commercial use requires a paid license.

**Propriétaire — Tous droits réservés.**  
Toute utilisation commerciale nécessite une licence payante.

**Proprietair — Alle rechten voorbehouden.**  
Commercieel gebruik vereist een betaalde licentie.

[📄 Voir le fichier de licence complet / See full license file / Zie volledig licentiebestand](LICENSE)

---


