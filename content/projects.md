---
title: 'Projects'
date: 2025-02-01
type: landing

design:
  # Section spacing
  spacing: '5rem'

# Page sections
sections:
  - block: collection
    content:
      title: My Projects
      text: These are the projects I am working on.
      filters:
        folders:
          - project
      count: 10
      sort_by: 'Params.tags'
    design:
      view: article-grid
      fill_image: false
      columns: 4
---
