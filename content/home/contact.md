---
# An instance of the Contact widget.
# Documentation: https://sourcethemes.com/academic/docs/page-builder/
widget: contact

# This file represents a page section.
headless: true

# Order that this section appears on the page.
weight: 130

title: Contact
subtitle: Feel free to send me an email.

content:
  # Automatically link email and phone or display as text?
  autolink: true
  
  # Email form provider
  form:
    provider: netlify
    formspree:
      id: arlie.coles@gmail.com
    netlify:
      # Enable CAPTCHA challenge to reduce spam?
      captcha: false
  
design:
  columns: '2'
---
