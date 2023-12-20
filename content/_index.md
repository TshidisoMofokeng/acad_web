---
date: "24-10-2022"
sections:
- block: hero
  content:
    cta:
      label: '**Get Started**'
      url: https://wowchemy.com/templates/
    cta_alt:
      label: Ask a question
      url: https://discord.gg/z8wNYzb
    cta_note:
      label: '<div style="text-shadow: none;"><a class="github-button" href="https://github.com/wowchemy/wowchemy-hugo-themes"
        data-icon="octicon-star" data-size="large" data-show-count="true" aria-label="Star">Star
        Wowchemy Website Builder</a></div><div style="text-shadow: none;"><a class="github-button"
        href="https://github.com/wowchemy/starter-hugo-academic" data-icon="octicon-star"
        data-size="large" data-show-count="true" aria-label="Star">Star the Academic
        template</a></div>'
    image:
      filename: hero-academic.png
    text: |-
      

      **Easily build anything with blocks - no-code required!**

      From landing pages, second brains, and courses to academic resumés, conferences, and tech blogs.

      <!--Custom spacing-->
      <div class="mb-3"></div>
      <!--GitHub Button JS-->
      <script async defer src="https://buttons.github.io/buttons.js"></script>
    title: Hugo Academic Theme
  demo: true
  design:
    background:
      gradient_end: '#1976d2'
      gradient_start: '#004ba0'
      text_color_light: true
- block: about.biography
  content:
    title: 
    username: admin
  id: about
- block: collection
  content:
    count: 5
    filters:
      author: ""
      category: ""
      exclude_featured: false
      exclude_future: false
      exclude_past: false
      folders:
      - post
      publication_type: ""
      tag: ""
    offset: 0
    order: desc
    subtitle: ""
    text: ""
    title: Recent Posts
  design:
    columns: "2"
    view: compact
  id: posts
- block: portfolio
  content:
    buttons:
    - name: All
      tag: '*'
    - name: Deep Learning
      tag: Deep Learning
    - name: Other
      tag: Demo
    default_button_index: 0
    filters:
      folders:
      - project
    title: Projects
  design:
    columns: "1"
    flip_alt_rows: false
    view: showcase
  id: projects  
title: "Projects"  
type: landing
---
