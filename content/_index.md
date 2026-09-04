---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-09-03
type: landing

sections:
  - block: resume-biography-3
    id: about
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      # `|` keeps the line breaks. A blank line starts a new paragraph;
      # two spaces at the end of a line force a break inside one.
      text: |
        I'm a Computer Science and Physics undergraduate at UCLA.

        I'm really interested in working on low level projects, despite not having much experience in them. More recently over the summer, I've been working on full-stack development. 
      # Show a call-to-action button under your biography? (optional)
      # button:
      #   text: Download CV
      #   url: uploads/resume.pdf
      headings:
        about: 'About Me'
    design:
      name:
        size: md # Options: xs, sm, md, lg (default), xl
      avatar:
        size: medium # Options: small, medium (default), large, xl, xxl
        shape: circle # Options: circle (default), square, rounded
  - block: resume-experience
    id: experience
    content:
      username: me-cv
    design:
      css_class: section-alt
      is_education_first: false
      date_format: 'Jan 2006'
  - block: research-roles
    id: research
    content:
      title: Research
      section: research
      # Intro text lives in content/snippets/research-intro.md
      text_from: 'snippets/research-intro'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - projects
      buttons:
        - name: All
          tag: '*'
      archive:
        enable: false
    design:
      css_class: section-alt
      align: center
      columns: 1
      fallback_icon: code-bracket
  - block: notes
    id: notes
    content:
      title: Notes
      section: notes
      # Intro text lives in content/snippets/notes-intro.md
      text_from: 'snippets/notes-intro'
      # Teaser only - the full, grouped list lives at /notes/
      count: 5
      button:
        text: 'All notes'
        url: '/notes/'
---
