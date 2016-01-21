# Security Library

Target form
    - entire form
    - only certain fields

CSRF protection

Flood protection
    - only so many submissions on same IP
    - only submit X per Y amount of time
    - wait until you can submit again if too many
    - only submit X amount

CAPTCHA protection

Filter content
    - potential spam
    - remove HTML
    - fix bad HTML
    - links
    - swear words
    - Javascript
    - nudity in images
    - face detection
    - custom callbacks
    - specific languages (spoken)

File handling
    - size restrictions
    - extension restrictions
    - remove extension from file name and save that (return extension when downloading)
    - scan for viruses
    - block certain encoding

Whitelist or Blacklist Things
     - IPs
          - certain areas (countries, states, cities, lat/lon radius)
          - list
    - Email addresses
    - Browsers
    - Operating Systems
    - Anonymous users
    - Bots
    - Callback
