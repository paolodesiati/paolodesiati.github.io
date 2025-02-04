---
title: 'Projects'
date: 2025-02-01
type: landing

design:
  # Section spacing
  spacing: '5rem'

---

## Summary
### Science Projects
- High Altitude Water Cherenkov (HAWC) Gamma-Ray Observatory
- IceCube Neutrino Observatory
- Southern Wide-field Gamma-ray Observatory (SWGO)
## Analysis Projects
- Cosmic-ray anisotropy
- Sun & Moon cosmic-ray shadow
## Technology Projects
- CREW-HaT active magnetic shielding

# Page sections
sections:
  - block: collection
    content:
      title: Science projects
      text: These are the science projects I work on.
      filters:
        folders:
          - project
    design:
      view: article-grid
      fill_image: false
      columns: 3
  - block: collection
    content:
      title: Analysis projects
      text: These are the analysis projects I work on.
      filters:
        folders:
          - analysis
    design:
      view: article-grid
      fill_image: false
      columns: 2
  - block: collection
    content:
      title: Technology projects
      text: Here are the technology projects I work on.
      filters:
        folders:
          - technology
    design:
      view: article-grid
      fill_image: false
      columns: 1
---
