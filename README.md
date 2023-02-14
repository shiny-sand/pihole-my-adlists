# pihole-my-adlists
In here I have my Pihole adlists.

Pihole servers fetch lists outside gravity by using the pihole-updatelists service > https://github.com/jacklul/pihole-updatelists

This resolves the following problem.

pihole-updatelists runs on schedule so all lists are updated once a day. This needs to be done manually in Pihole.

pihole-updatelists allows me to pull whitelists, which is not possible in stock Pihole.



***


Here is the content of my configuration file > /etc/pihole-updatelists.conf

<pre><code>
ADLISTS_URL="https://raw.githubusercontent.com/shiny-sand/pihole/main/adlist.txt"

; Remote list URL containing exact domains to whitelist
WHITELIST_URL="https://raw.githubusercontent.com/shiny-sand/pihole/main/whitelist-personal.txt"

; Remote list URL containing regex rules for whitelisting
REGEX_WHITELIST_URL=""

; Remote list URL containing exact domains to blacklist
; This is specifically for handcrafted lists only, do not use regular blocklists here!
BLACKLIST_URL=""

; Remote list URL containing regex rules for blacklisting
REGEX_BLACKLIST_URL=""
</code></pre>
