# Visual dependency map

```mermaid
flowchart LR
  Fonts[Display, text and mono font records] --> Hero[Hero wrapping and motion]
  Fonts --> Marketing[Marketing cards, articles and footer]
  Logo[Inline wordmark SVG] --> Nav[Marketing navigation]
  Logo --> Footer[Footer]
  CSS[Grain, gradient and rail geometry] --> Hero
  CSS --> Marketing
  Videos[Two demo streams plus posters] --> Player[Synchronized screencast]
  Player --> Home[Homepage demo]
  Player --> Lessons[Learning/video template candidate]
  HTML[Layered HTML and SVG illustrations] --> Bento[Five linked Orb features]
  Pucks[Puck WebP family] --> Proof[Testimonial field]
  Avatars[Attributed portraits] --> Proof
  Thumb[Four lesson thumbnails] --> Strip[Episode strip]
  CliVideo[Two CLI demo videos] --> Cli[Installer and local/remote section]
  NewsArt[Three announcement AVIFs] --> News[Home news rows]
  ArticleArt[News screenshot and inline images] --> Article[News detail]
```

Changing display fonts can alter every heading wrap and animated measurement layer. HOME-CSSOM-001 confirms font-face source mapping and swap declarations; actual requested subset/load status and reuse rights remain unresolved. Player, sidebar, and transcript states alter page height and downstream comparison scroll positions. Asset license/source approval must precede implementation use. This map records visual dependencies; it does not establish that the reference uses shared source components. Required sources and confidence are in asset-inventory.md.
