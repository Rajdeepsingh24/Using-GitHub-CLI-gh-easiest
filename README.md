# Using-GitHub-CLI-gh-easiest
# 1) Create a project folder and init git
mkdir my-project && cd my-project
git init -b main

# 2) Add starter files
echo "# My Project" > README.md
cat > .gitignore <<'EOF'
# common ignores
node_modules/
.env
__pycache__/
.DS_Store
EOF

# 3) First commit
git add .
git commit -m "chore: initial commit"

# 4) Create GitHub repo and push in one go
# --public can be --private if you want
gh repo create my-project --public --source=. --remote=origin --push
