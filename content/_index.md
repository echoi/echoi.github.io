---
# Leave the homepage title empty to use the site title
title: ''
date: 2023-12-13
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  # - block: skills
  #   content:
  #     title: Skills
  #     text: ''
  #     # Choose a user to display skills from (a folder name within `content/authors/`)
  #     username: admin
  #   design:
  #     columns: '1'
  - block: experience
    id: experience
    content:
      title: Experience
#       # Date format for experience
#       #   Refer to https://docs.hugoblox.com/customization/#date-format
#       date_format: Jan 2006
#       # Experiences.
#       #   Add/remove as many `experience` items below as you like.
#       #   Required fields are `title`, `company`, and `date_start`.
#       #   Leave `date_end` empty if it's your current employer.
#       #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
      - title: Associate Professor
        company: The University of Memphis
        company_url: 'https://memphis.edu'
        company_logo: 
        location: Memphis, TN, USA
        date_start: '2018-08-01'
        date_end: ''
        description: #|2-
            # Responsibilities include:
            
            # * Analysing
            # * Modelling
            # * Deploying

      - title: Assistant Professor
        company: The University of Memphis
        company_url: 'https://memphis.edu'
        company_logo: 
        location: Memphis, TN, USA
        date_start: '2013-01-01'
        date_end: '2018-07-31'
        description: 

      - title: Post-doctoral Researhcer
        company: University of Texas Institute for Geophysics
        company_url: 'https://www.ig.utexas.edu'
        advisor: Luc L. Lavier
        location: Austin, TX, USA
        date_start: '2012-01-01'
        date_end: '2012-12-31'
        description: 

      - title: Post-doctoral Researhcer
        company: Lamont-Doherty Earth Observatory of the Columbia University
        company_url: 'https://ldeo.columbia.edu'
        advisor: W. Roger Buck
        location: Palisades, NY, USA
        date_start: '2008-10-01'
        date_end: '2011-12-31'
        description: 
    design:
      columns: '2'
  - block: markdown
    id: gallery
    content:
      title: Gallery
      subtitle: ''
      text: |-
        {{< gallery album="cerigeodyn" >}}
    design:
      columns: '1'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        # - name: All
        #   tag: '*'
        # - name: Deep Learning
        #   tag: Deep Learning
        # - name: Other
        #   tag: Demo
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '1'
      view: showcase
      # For Showcase view, flip alternate rows?
      flip_alt_rows: true

#   - block: collection
#     id: featured
#     content:
#       title: Featured Publications
#       filters:
#         folders:
#           - publication
#         featured_only: true
#     design:
#       columns: '2'
#       view: card
#   - block: collection
#     content:
#       title: Recent Publications
#       text: |-
#         {{% callout note %}}
#         Quickly discover relevant content by [filtering publications](./publication/).
#         {{% /callout %}}
#       filters:
#         folders:
#           - publication
#         exclude_featured: true
#     design:
#       columns: '2'
#       view: citation
#   - block: collection
#     id: talks
#     content:
#       title: Recent & Upcoming Talks
#       filters:
#         folders:
#           - event
#     design:
#       columns: '2'
#       view: compact
#   - block: tag_cloud
#     content:
#       title: Popular Topics
#     design:
#       columns: '2'
  - block: contact
    id: contact
    content:
      title: Contact
      subtitle:
      text:
      # Contact (add or remove contact options as necessary)
      email: echoi2@memphis.edu
      phone: +1 901 678 4923
      appointment_url: #'https://calendly.com'
      address:
        street: 3890 Central Ave
        city: Memphis
        region: TA
        postcode: '38152'
        country: United States
        country_code: US
      directions: Enter House 3 and find Office 106 on Floor 1
      office_hours:
        # - 'Monday 10:00 to 13:00'
        # - 'Wednesday 09:00 to 10:00'
      # Choose a map provider in `params.yaml` to show a map from these coordinates
      coordinates:
        latitude: '35.123516'
        longitude: '-89.932473'  
      contact_links:
        # - icon: twitter
        #   icon_pack: fab
        #   name: DM Me
        #   link: 'https://twitter.com/Twitter'
        # - icon: skype
        #   icon_pack: fab
        #   name: Skype Me
        #   link: 'skype:echo123?call'
        # - icon: video
        #   icon_pack: fas
        #   name: Zoom Me
        #   link: 'https://zoom.com'
      # Automatically link email and phone or display as text?
      autolink: true
      # Email form provider
      form:
        provider: netlify
        formspree:
          id:
        netlify:
          # Enable CAPTCHA challenge to reduce spam?
          captcha: false
    design:
      columns: '2'
---
