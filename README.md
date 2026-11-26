# VP Engineering Tool — Releases

Dieses Repository trägt ausschließlich die gebauten, notarisierten Archive des
VP Engineering Tool. Der Quellcode liegt in einem privaten Repository.

Der Grund für die Trennung: Release-Assets eines privaten Repositories sind nicht
öffentlich abrufbar. Ein Homebrew-Cask, der dorthin zeigt, antwortet für jeden mit 404.
Also bleibt der Code privat und nur das Artefakt wird öffentlich.

## Installation

```sh
brew install --cask steinandreas/tap/vp-engineering-tool
```

Ohne Homebrew: das ZIP des neuesten [Releases](../../releases) laden, entpacken, die App
nach `/Applications` legen.

## Was in einem Release steckt

`VPEngineeringTool-<version>.zip` — die App, signiert mit einer Developer ID, von Apple
notarisiert und mit gehefteten Ticket. Sie startet damit auf jedem Mac ab macOS 26, ohne
Rechtsklick-Umweg und ohne Gatekeeper-Warnung.

Die App braucht ein Firebase-Projekt und eine Google-Anmeldung. Ohne Zugang zu dem
Projekt, für das sie gebaut ist, zeigt sie nach der Anmeldung einen leeren
Arbeitsbereich: die Firestore-Regeln geben jedem Konto nur seine eigenen Daten.
