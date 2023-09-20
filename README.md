# MonBun.github.io
Welcome to MonBun – a digital sanctuary where the timeless red threads of fate and Chinese lore entwine with the hidden world of adoptees. Explore the pages of our website as you discover and learn more about ancient Chinese Legends and modern Chinese Adoptees.

name: Build and deploy to GitHub Pages

on:
  push:
    branches: [ master ]
  pull_request:
    branches: [ master ]

jobs:
  github-pages:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: helaili/jekyll-action@v2
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
          target_branch: 'gh-pages'
