---
# Leave the homepage title empty to use the site title
title: ''
summary: ''
date: 2026-09-03
type: landing

sections:
  - block: resume-biography-3
    content:
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: me
      text: ''
      # Show a call-to-action button under your biography? (optional)
      # button:
      #   text: Download CV
      #   url: uploads/resume.pdf
      headings:
        about: ''
        education: ''
        interests: ''
    design:
      name:
        size: md # Options: xs, sm, md, lg (default), xl
      avatar:
        size: medium # Options: small, medium (default), large, xl, xxl
        shape: circle # Options: circle (default), square, rounded
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
      align: center
      columns: 1
      fallback_icon: code-bracket
---
