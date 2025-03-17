# Scripts to enhance UX of Git Script

+ create script file: ```nano gitac```
+ add the code of <kbd>gitac.sh</kbd>
+ save file and give execution permisison ```chmod +x gitac```
+ (optional) move it to a directory in your $PATH: ```mv gitac /usr/local/bin/```

<details>
  <summary><b>gitac</b></summary>
  <p><br />alias of: <b>git add filename1 filename2 etc && git commit -m ""</b></p>
  <pre>
  #!/bin/bash

    # Get the last argument as the commit message
    commit_msg="${@: -1}"

    # Get all other arguments except the last one (file names)
    files=("${@:1:$#-1}")

    # Add the files to staging
    git add "${files[@]}"

    # Commit with the provided message
    git commit -m "$commit_msg"
  </pre>
</details>
