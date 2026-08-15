<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:1a1b27,50:7aa2f7,100:bb9af7&height=170&section=header&text=Navid&fontSize=58&fontColor=ffffff&animation=fadeIn&fontAlignY=34&desc=Data%20Scientist%20%E2%80%94%20Machine%20Learning%20%7C%20Deep%20Learning%20%7C%20Computer%20Vision&descAlignY=55&descSize=15" width="100%" />
</div>

<div align="center">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=21&duration=3200&pause=900&color=7AA2F7&center=true&vCenter=true&width=680&lines=Turning+raw+data+into+decisions.;Deep+Learning+%7C+NLP+%7C+Computer+Vision;Research-driven%2C+production-minded." alt="Typing SVG" />
</div>

<br>

<div align="center">

  <a href="mailto:your.email@example.com"><img src="https://img.shields.io/badge/Email-1a1b27?style=for-the-badge&logo=gmail&logoColor=7aa2f7" /></a>
  <a href="https://linkedin.com/in/your-handle"><img src="https://img.shields.io/badge/LinkedIn-1a1b27?style=for-the-badge&logo=linkedin&logoColor=7aa2f7" /></a>
  <a href="https://kaggle.com/your-handle"><img src="https://img.shields.io/badge/Kaggle-1a1b27?style=for-the-badge&logo=kaggle&logoColor=7aa2f7" /></a>
  <img src="https://komarev.com/ghpvc/?username=navidml&style=for-the-badge&color=7aa2f7&label=PROFILE+VIEWS" />

</div>

<br>

## About

```python
class Navid:
    role     = "Data Scientist"
    focus    = ["Deep Learning", "NLP", "Computer Vision"]
    working  = "predictive modeling, image processing, applied research"
    building = "AI-powered solutions for real-world problems"
    learning = "always"
```

I work end-to-end: framing the problem, cleaning the data, training and evaluating the model,
and shipping something that actually holds up outside a notebook. Most of my time goes to
computer vision and language models, with a steady interest in the research side of both.

<br>

## Tech Stack

<div align="center">

**Languages & Data**

<img src="https://skillicons.dev/icons?i=python,mysql,postgres,git,github,linux&theme=dark" />

**Machine Learning & Deep Learning**

<img src="https://skillicons.dev/icons?i=pytorch,tensorflow,sklearn,opencv&theme=dark" />

<img src="https://img.shields.io/badge/Pandas-1a1b27?style=for-the-badge&logo=pandas&logoColor=7aa2f7" />
<img src="https://img.shields.io/badge/NumPy-1a1b27?style=for-the-badge&logo=numpy&logoColor=7aa2f7" />
<img src="https://img.shields.io/badge/SciPy-1a1b27?style=for-the-badge&logo=scipy&logoColor=7aa2f7" />
<img src="https://img.shields.io/badge/Hugging%20Face-1a1b27?style=for-the-badge&logo=huggingface&logoColor=7aa2f7" />
<img src="https://img.shields.io/badge/Matplotlib-1a1b27?style=for-the-badge&logo=plotly&logoColor=7aa2f7" />
<img src="https://img.shields.io/badge/Jupyter-1a1b27?style=for-the-badge&logo=jupyter&logoColor=7aa2f7" />

</div>

<br>

## Stats

<div align="center">

  <img height="165" src="https://github-readme-stats.shion.dev/api?username=navidml&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=7aa2f7&icon_color=bb9af7&include_all_commits=true&count_private=true" />
  <img height="165" src="https://streak-stats.demolab.com/?user=navidml&theme=tokyonight&hide_border=true&background=0d1117&ring=7aa2f7&fire=bb9af7&currStreakLabel=7aa2f7" />

  <img width="49%" src="https://github-readme-stats.shion.dev/api/top-langs/?username=navidml&theme=tokyonight&hide_border=true&bg_color=0d1117&title_color=7aa2f7&include_all_commits=true&count_private=true&layout=compact&langs_count=8" />

</div>

<div align="center">
  <img width="98%" src="https://github-readme-activity-graph.vercel.app/graph?username=navidml&theme=tokyo-night&bg_color=0d1117&color=7aa2f7&line=bb9af7&point=ffffff&hide_border=true&area=true" />
</div>

<br>

## Contribution Graph

<div align="center">
  <img src="https://raw.githubusercontent.com/navidml/navidml/output/snake.svg" alt="Snake animation" width="98%" />
</div>

<br>

## Achievements

<div align="center">
  <img src="https://github-profile-trophy.vercel.app/?username=navidml&theme=tokyonight&no-frame=true&no-bg=true&column=7&margin-w=8&margin-h=8" />
</div>

<br>

<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:bb9af7,50:7aa2f7,100:1a1b27&height=120&section=footer" width="100%" />
</div>

name: Generate Snake Animation

on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
  push:
    branches:
      - main

jobs:
  generate:
    runs-on: ubuntu-latest
    permissions:
      contents: write
    steps:
      - name: Generate snake
        uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: navidml
          outputs: |
            dist/snake.svg?palette=github-dark&color_snake=#7aa2f7&color_dots=#1a1b27,#2f3b54,#4c6099,#7aa2f7,#bb9af7

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
