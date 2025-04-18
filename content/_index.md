---
# Leave the homepage title empty to use the site title
title: ""
date: 2022-10-24
type: landing

design:
  # Default section spacing
  spacing: "6rem"

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
      text: ""
      # Show a call-to-action button under your biography? (optional)
      button:
        text: Download Resume
        url: uploads/resume.pdf
    design:
      css_class: dark
      background:
        color: black
        image:
          # Add your image background to `assets/media/`.
          filename: sfondoic2.png
          filters:
            brightness: 1.0
          size: cover
          position: center
          parallax: false
  - block: markdown
    content:
      title: 'My Research'
      subtitle: ''
      text: |-
        **IceCube:** Leading the cosmic-ray analyses in IceCube since 2006. Co-PI of the current IceCube Cosmic Ray
        Analysis sub-award (funded by NSF; UW–Madison PI: Desiati). I lead a working group on cosmic-ray anisotropy
        analyses at UW-Madison in collaboration with Dr. Juan Carlos Díaz Vélez (WIPAC), Prof. Rasha Abbasi (Loyola
        University Chicago), Prof. Frank McNally (Mercer University).

        Collaboration with Prof. Julia Becker Tjus (University of Bochum, Germany) and the Bochum group on
        the observation of the cosmic-ray shadow cast by the Moon and the Sun using IceCube data and the numerical
        calculation of cosmic-ray particle trajectories around the Sun at different phases of the solar cycle.

        **HAWC:** Combined analysis of 10 TeV cosmic-ray anisotropy with the HAWC and the IceCube neutrino observatories
        (with Dr. Juan Carlos Díaz Vélez). I am working on an overhaul of cosmic-ray anisotropy analysis in the 1-100
        TeV energy range, using eight years of HAWC data. And on the HAWC/IceCube combined analysis in the 10-100 TeV
        energy range (funded by NSF grant; PI: Desiati). An MoU between IceCube and HAWC was established.

        **SWGO:** Collaboration member of the Southern Wide-field Gamma-ray Observatory (SWGO) and member of the Cosmic
        Ray task force aimed to establish requirements for high-energy cosmic anisotropy observations.

        **GRAPES-3:** Collaboration with the GRAPES-3 extensive air shower experiment (located in Ooty, India) aimed to
        perform a combined analysis of cosmic-ray anisotropy with IceCube in the energy range of 10-100 TeV. An MoU
        between IceCube and GRAPES-3 was established.

        **Numerical Calculations:** Paolo Desiati and Juan Carlos Díaz Vélez (UW-Madison) collaborate with Prof.
        Nikolai Pogorelov (Univ. of Alabama - Huntsville), Prof. Zhang Ming (Florida Institute of Technology), and Dr. Vanessa López 
        Barquero (University of Maryland) on the heliosphere’s distortion effects on the arrival direction distribution of TeV cosmic 
        rays and the unfolding of the interstellar diffusion properties.
    design:
      css_class: "my-small-text"
      css_class: "custom-text"
      css_class: "paragraph-text"
      columns: '1'
  - block: collection
    id: papers
    content:
      title: Featured Publications
      filters:
        folders:
          - publication
        featured_only: true
      count: 10
    design:
      view: article-grid
      columns: 3
  - block: collection
    content:
      title: Recent Publications
      text: ""
      filters:
        folders:
          - publication
        exclude_featured: false
    design:
      view: citation
  - block: collection
    id: talks
    content:
      title: Featured Talks
      filters:
        folders:
          - event
    design:
      view: article-grid
      columns: 2
  # - block: collection
  #  id: news
  #  content:
  #    title: Recent News
  #    subtitle: ''
  #    text: ''
  #    # Page type to display. E.g. post, talk, publication...
  #    page_type: post
  #    # Choose how many pages you would like to display (0 = all pages)
  #    count: 5
  #    # Filter on criteria
  #    filters:
  #      author: ""
  #      category: ""
  #      tag: ""
  #      exclude_featured: false
  #      exclude_future: false
  #      exclude_past: false
  #      publication_type: ""
  #    # Choose how many pages you would like to offset by
  #    offset: 0
  #    # Page order: descending (desc) or ascending (asc) date.
  #    order: desc
  #  design:
  #    # Choose a layout view
  #    view: date-title-summary
  #    # Reduce spacing
  #    spacing:
  #      padding: [0, 0, 0, 0]
  
  # - block: cta-card
  #  demo: true # Only display this section in the Hugo Blox Builder demo site
  #  content:
  #    title: 👉 Build your own academic website like this
  #    text: |-
  #      This site is generated by Hugo Blox Builder - the FREE, Hugo-based open source website builder trusted by 250,000+ academics like you.

  #      <a class="github-button" href="https://github.com/HugoBlox/hugo-blox-builder" data-color-scheme="no-preference: light; light: light; dark: dark;" data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star HugoBlox/hugo-blox-builder on GitHub">Star</a>

  #      Easily build anything with blocks - no-code required!
        
  #      From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.
  #    button:
  #      text: Get Started
  #      url: https://hugoblox.com/templates/
  #  design:
  #    card:
  #      # Card background color (CSS class)
  #      css_class: "bg-primary-700"
  #      css_style: ""
---
