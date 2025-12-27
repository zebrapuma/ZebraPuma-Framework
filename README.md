# Zebra Puma Framework

[![Documentation](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](https://zebrapumaorg.github.io/ZebraPuma-Framework/)
[![NuGet Plugins](https://img.shields.io/badge/NuGet-Plugins-blue)](https://github.com/orgs/ZebraPumaOrg/packages?repo_name=ZebraPuma-Framework)
[![NuGet ServiceProcess](https://img.shields.io/badge/NuGet-ServiceProcess-blue)](https://github.com/orgs/ZebraPumaOrg/packages?repo_name=ZebraPuma-Framework)
[![License](https://img.shields.io/badge/License-Proprietary-red)](LICENSE)

> Services & Plugins pour Windows et .NET

Framework .NET pour créer des applications modulaires avec système de plugins et services Windows avancés.

## 📚 Documentation

**[📖 Consultez la documentation complète →](https://zebrapumaorg.github.io/ZebraPuma-Framework/)**

## 📦 Packages Disponibles

| Package | Version | Description |
|---------|---------|-------------|
| **ZebraPuma.Plugins** | ![Version](https://img.shields.io/badge/version-2.0.6-green) | Système de plugins extensible |
| **ZebraPuma.System.ServiceProcess** | ![Version](https://img.shields.io/badge/version-2.0.6-green) | Extensions pour services Windows |

## 🚀 Installation

### 1. Configurer le Source NuGet

```bash
dotnet nuget add source https://nuget.pkg.github.com/ZebraPumaOrg/index.json \
  --name ZebraPuma \
  --username VOTRE_USERNAME \
  --password VOTRE_GITHUB_PAT
```

**Créer un Personal Access Token (PAT) :**
1. GitHub → Settings → Developer settings → [Personal access tokens](https://github.com/settings/tokens)
2. Generate new token (classic)
3. Sélectionner : `read:packages`
4. Copier le token

### 2. Installer les Packages

```bash
# Plugins
dotnet add package ZebraPuma.Plugins --version 2.0.6

# Services Windows
dotnet add package ZebraPuma.System.ServiceProcess --version 2.0.6
```

### 3. Configuration `nuget.config` (Optionnel)

```xml
<?xml version="1.0" encoding="utf-8"?>
<configuration>
  <packageSources>
    <add key="nuget.org" value="https://api.nuget.org/v3/index.json" />
    <add key="ZebraPuma" value="https://nuget.pkg.github.com/ZebraPumaOrg/index.json" />
  </packageSources>
  <packageSourceCredentials>
    <ZebraPuma>
      <add key="Username" value="VOTRE_USERNAME" />
      <add key="ClearTextPassword" value="VOTRE_PAT" />
    </ZebraPuma>
  </packageSourceCredentials>
</configuration>
```

## 🎯 Démarrage Rapide

### ZebraPuma.Plugins

```csharp
using ZebraPuma.Plugins;

// Charger les plugins
var loader = new PluginLoader();
var plugins = loader.LoadPlugins<IPlugin>();

foreach (var plugin in plugins)
{
    plugin.Initialize(context);
    plugin.Execute();
}
```

### ZebraPuma.System.ServiceProcess

```csharp
using ZebraPuma.System.ServiceProcess;

public class MonService : ServiceBaseExtended
{
    public override string Name => "MonService";
    
    protected override void OnStartCore(string[] args)
    {
        Logger.Information("Service démarré");
    }
    
    protected override void OnStopCore()
    {
        Logger.Information("Service arrêté");
    }
}

// Installation du service
ServiceManager.InstallService(new MonService());
```

## 📖 Guides

- [Guide Plugins](https://zebrapumaorg.github.io/ZebraPuma-Framework/articles/plugins.html) - Architecture, chargement, cycle de vie
- [Guide Services Windows](https://zebrapumaorg.github.io/ZebraPuma-Framework/articles/serviceprocess.html) - Création, déploiement, gestion
- [Référence API](https://zebrapumaorg.github.io/ZebraPuma-Framework/api/) - Documentation complète de l'API

## 🔗 Liens Utiles

- 📦 [Packages NuGet](https://github.com/orgs/ZebraPumaOrg/packages?repo_name=ZebraPuma-Framework)
- 📚 [Documentation](https://zebrapumaorg.github.io/ZebraPuma-Framework/)
- 📄 [Licence](LICENSE)
- 🐛 [Issues](https://github.com/ZebraPumaOrg/ZebraPuma-Framework/issues)

## 🛠️ Technologies

- **.NET Framework 4.8** - Support des applications legacy
- **.NET 10.0** - Support moderne et cross-platform
- **Windows Services** - Services natifs Windows
- **Plugin Architecture** - Système modulaire extensible

## 📄 Licence

**Propriétaire** - © 2025-2026 Régis SCYEUR, Zebra Puma Services

Tous droits réservés. L'utilisation commerciale nécessite une licence payante.

Voir [LICENSE](LICENSE) pour plus de détails.

## 👤 Auteur

**Régis SCYEUR** - Zebra Puma Services - [![Régis SCYEUR](https://img.shields.io/badge/GitHub-Regis--Scyeur-181717?style=flat&logo=github)](https://github.com/Regis-Scyeur)

