#!/usr/bin/env bash
# Usage: ./publish.sh USERNAME REPO "Repo Description" GITHUB_TOKEN
USERNAME="$1"
REPO="$2"
DESC="$3"
TOKEN="$4"

if [ -z "$USERNAME" ] || [ -z "$REPO" ] || [ -z "$TOKEN" ]; then
  echo "Usage: ./publish.sh USERNAME REPO DESC GITHUB_TOKEN"
  exit 1
fi

# create repo via GitHub API
curl -H "Authorization: token $TOKEN" \
     -d "{\"name\":\"$REPO\",\"description\":\"$DESC\",\"private\":false}" \
     https://api.github.com/user/repos

# initialize git and push
git init
git add .
git commit -m "Initial website upload"
git branch -M main
git remote add origin https://github.com/$USERNAME/$REPO.git
git push -u origin main

echo "Repository created and pushed. Now enable Pages from repository settings -> Pages -> Branch: main / Root."
