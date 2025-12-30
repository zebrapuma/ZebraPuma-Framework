# GitHub Copilot Instructions for ZebraPuma Framework

## Repository Overview

This is the **ZebraPuma Framework** repository - a .NET framework for creating modular applications with plugin systems and Windows services. This repository primarily contains **documentation** and **metadata** for the framework.

### Key Information
- **Primary Language**: French (documentation is in French)
- **Technologies**: .NET Framework 4.8 and .NET 10.0
- **Author**: Régis SCYEUR - Zebra Puma Services
- **License**: Proprietary - Commercial use requires paid license
- **Repository Purpose**: Documentation and package metadata

## Repository Structure

```
/
├── .github/              # GitHub configuration
├── docs/                 # Generated documentation site
│   ├── api/             # API reference documentation
│   ├── articles/        # Guide articles (plugins.html, serviceprocess.html)
│   └── ...              # Other documentation assets
├── README.md            # Main documentation and package installation guide
├── LICENSE              # Proprietary license
└── .gitignore          # Visual Studio/.NET ignore patterns
```

## Working with This Repository

### Documentation Standards
1. **Language**: All documentation MUST be in French
2. **Consistency**: Follow the existing writing style in README.md
3. **Code Examples**: Use C# syntax highlighting for code blocks
4. **Package References**: Always reference packages from GitHub Packages (not nuget.org)
5. **Version Numbers**: Keep version references consistent (currently 2.0.6)

### Key Packages
- `ZebraPuma.Plugins` - Plugin system
- `ZebraPuma.System.ServiceProcess` - Windows services extensions

### Documentation Files
- **README.md**: Main entry point, installation guide, quick start examples
- **docs/**: Pre-generated documentation (DocFX or similar)
- **LICENSE**: Proprietary license - do not modify without author approval

## Code Style and Conventions

### C# Code Examples
- Use modern C# syntax appropriate for .NET 10.0
- Maintain backward compatibility examples for .NET Framework 4.8 when relevant
- Follow standard .NET naming conventions (PascalCase for public members)
- Include `using` statements in examples
- Keep examples concise and focused

### Markdown Documentation
- Use clear, descriptive headings (## for main sections, ### for subsections)
- Include code fences with language identifiers (```csharp, ```bash, ```xml)
- Use badges for visual elements (shields.io format)
- Link to official GitHub Pages documentation: https://zebrapuma.github.io/ZebraPuma-Framework/

## Making Changes

### Documentation Updates
1. **README.md changes**: Ensure all French text is grammatically correct
2. **Version updates**: Update all package version references consistently
3. **Link updates**: Verify all links are functional
4. **Code examples**: Test that examples compile and follow best practices

### What NOT to Change
- **docs/ directory**: This appears to be auto-generated - do not edit manually
- **LICENSE file**: Proprietary license - requires author approval to modify
- **Author attribution**: Must remain "Régis SCYEUR - Zebra Puma Services"

## Build and Validation

### Documentation
- This repository does not have a traditional build process
- Validate Markdown formatting using standard Markdown linters
- Verify links are not broken
- Ensure code examples are syntactically correct

### Testing Changes
- Review README.md rendering on GitHub
- Check that all links work
- Validate code examples compile (if possible)

## Special Considerations

### License Awareness
- This is **proprietary software** with commercial licensing requirements
- Any code examples or documentation must respect the proprietary nature
- Do not suggest open-source alternatives or license changes without explicit request

### Package Installation
- Packages are hosted on GitHub Packages (not nuget.org)
- Users need GitHub Personal Access Token (PAT) with `read:packages` scope
- Installation requires authentication configuration

### Multi-Target Framework Support
- Examples should work for both .NET Framework 4.8 and .NET 10.0
- Note any framework-specific differences in documentation

## Common Tasks

### Updating Package Versions
When updating version numbers:
1. Update all badges in README.md
2. Update version in installation examples
3. Update version in code example comments if present
4. Ensure consistency across all documentation

### Adding New Examples
1. Write in C# with appropriate `using` statements
2. Comment in French or keep technical terms in English
3. Follow existing example formatting
4. Test for syntax correctness

### Fixing Documentation Issues
1. Maintain French language throughout
2. Follow existing Markdown structure
3. Keep consistent with framework's technical style
4. Verify all package references are correct

## Contact and Support

- **Issues**: https://github.com/ZebraPumaOrg/ZebraPuma-Framework/issues
- **Packages**: https://github.com/orgs/zebrapuma/packages
- **Documentation**: https://zebrapuma.github.io/ZebraPuma-Framework/

## Quick Reference

- **Default Branch**: (check repository settings)
- **Primary Files**: README.md, LICENSE, docs/
- **Package Registry**: GitHub Packages (github.com/orgs/zebrapuma/packages)
- **Framework Versions**: .NET Framework 4.8, .NET 10.0
- **Documentation Language**: French
