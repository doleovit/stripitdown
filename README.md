````bash
   ____________
  (      ?     )
   ------------
          o   ^__^
           o  (oo)\_______                  s t r i p i t d o w n  ←
              (__)\       )\/\
                  ||----w |
                  ||     ||
````

## firefox user.js

````bash
# download @profile:

tr -d '\n' <<'EOF' | tr -s ' ' | sh
 grep -i --context=1 '^default=1' "$HOME"/.mozilla/f*x/profiles.ini
 | grep -i '^path' | cut -d '=' -f2 | xargs -I{} wget
 https://raw.githubusercontent.com/doleovit/stripitdown/main/user.js
 -P "$HOME"/.mozilla/firefox/{}/
EOF
````
