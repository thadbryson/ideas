# Security Library

All in one security library for text content, encryption, files, and HTTP requests.

**Encryption**
 - Simple encryption and decryption.
 - Allow one-way hashing.

**Target form**
    - entire form
    - only certain fields

**Flood protection**
    - only so many submissions on same IP
    - only submit X per Y amount of time
    - wait until you can submit again if too many
    - only submit X amount

**CAPTCHA protection**
 - Tokens: unique IDs
 - Session handling
 - Cache handling (Redis, Memcache, file, etc)

**Restrict User**
 - IP
 - browser
 - location: country, region, city

**Time constraint**
- Between certain times
- By a certain time
- Submit within an amount of time

**Filter content**
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

**File handling**
- check for nudity
- face detection
- size restrictions
- extension restrictions
- remove extension from file name and save that (return extension when downloading)
- scan for viruses
- block certain encoding

**Whitelist or Blacklist Things**
- IPs
    - certain areas (countries, states, cities, lat/lon radius)
    - list
- Email addresses
- Browsers
- Operating Systems
- Anonymous users
- Bots
- Callback
