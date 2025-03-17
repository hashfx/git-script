#!/bin/bash

# Get the last argument as the commit message
commit_msg="${@: -1}"

# Get all other arguments except the last one (file names)
files=("${@:1:$#-1}")

# Add the files to staging
git add "${files[@]}"

# Commit with the provided message
git commit -m "$commit_msg"
