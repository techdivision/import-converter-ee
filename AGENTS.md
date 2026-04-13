# AGENTS.md - import-converter-ee

## Zweck & Verantwortung

Das `import-converter-ee` Modul bietet **EE-spezifische Converter-Funktionalität**. Es ist ein **Tier 5 Modul** und erweitert `import-converter`.

**Hauptverantwortung:**
- EE-spezifische Konvertierungs-Funktionalität
- Staging Support für Konvertierungen
- Sequence Management für EE
- Observer Pattern für EE-Konvertierungs-Hooks

## Architektur & Design Patterns

### Kern-Klassen
- **EeConverter**: EE-spezifischer Converter
- **EeConverterObserver**: Observer für EE-Hooks
- **StagingConverter**: Converter mit Staging-Support

### Verwendete Patterns
- **Observer Pattern**: Für EE-Hooks
- **Strategy Pattern**: Verschiedene EE-Konvertierungs-Strategien

## Abhängigkeiten

### Externe Pakete
- **Keine**

### TechDivision Dependencies
- **import-ee** ^17.0.0 - EE Functionality
- **import-converter** ^12.0.0 - Converter Framework

### Abhängig von diesem Modul (1 Reverse Dependency)
- **import-cli-simple** - Master CLI

## Wichtige Entry Points

### Converter Klassen
```php
// EE Converter
EeConverter::convert($row): array
EeConverter::getSubject(): SubjectInterface

// Converter Observer
EeConverterObserver::handle($row): void
```

## Events & Extension Points

**Keine Events** - Tier 5 EE-Modul

## Hints für KI-Agenten

### Wichtig zu verstehen
1. **Tier 5 Modul**: Erweitert Converter Framework
2. **EE-fokussiert**: Spezialisiert auf EE Features
3. **Observer Pattern**: Für EE-Hooks
4. **Staging Support**: Für EE Staging

## Bekannte Einschränkungen

- **EE-Only**: Nur für Magento EE Deployments
- **Staging-Abhängig**: Erfordert EE Staging-Funktionalität

## Zusammenfassung

`import-converter-ee` ist ein **Tier 5 Modul**, das EE-spezifische Converter-Funktionalität bietet. Es erweitert den Converter Framework mit EE-Features.

**Für Agenten:** Verstehe dieses Modul als **EE Converter** mit Observer Pattern und Staging Support.
