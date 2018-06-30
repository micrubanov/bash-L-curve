# Bash is AWESOME!

There is no need to improve `bash`. It's fine, the people are f@#$ked.

## Bash CAN be safeifsh~

### Add bash script file template for `vim` with some safety defaults in context of bash as a language.

```
▶ cat << EOF | tee -a ~/.vim/templates/bash_header.txt
:insert
#!/usr/bin/env bash

# to trace what gets executed
set -x

# to exit when your script tries to use undeclared variables
set -u

# to make your script exit when a command fails.
set -e
# Then add || true to commands that you allow to fail.

# Set magic variables for current file & dir

__dir="$(cd "$(dirname "${BASH_SOURCE[0]}")" && pwd)"
__file="${__dir}/$(basename "${BASH_SOURCE[0]}")"
__base="$(basename ${__file} .sh)"
__root="$(cd "$(dirname "${__dir}")" && pwd)" # <-- change this as it depends on your app

arg1="${1:-}"

.
EOF

```


# ZSH is AWESOME! 2

With:

* `.oh-my-zsh`
* `vim`
  * `vundle`
    * and subsets of __vim plugins__ that fits into specific use-case profilei on the instance.






