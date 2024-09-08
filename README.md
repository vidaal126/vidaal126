## Bem-vindo(a) ao perfil do Arthur Vidal 😁

 <div>
   <a href="https://github.com/vidaal126">
   <img height="180em" src="https://github-readme-stats.vercel.app/api?username=vidaal126&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true"/>
   <img height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=vidaal126&layout=compact&langs_count=6&theme=tokyonight"/>
</div>

<div style="display: inline_block"><br>
  <img align="center" alt="Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="Pandas" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg">
  <img align="center" alt="Numpy" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/numpy/numpy-original.svg">
  <img align="center" alt="Jupyter" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/jupyter/jupyter-original.svg">
  <img align="center" alt="SQL" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/mysql/mysql-original.svg">
  <img align="center" alt="Data Science" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/docker/docker-original.svg">
</div>

<br>

### Entre em Contato comigo nas redes abaixo!!

<div> 
  <a href="https://instagram.com/_vidaal?igshid=YmMyMTA2M2Y=" target="_blank"><img src="https://img.shields.io/badge/Instagram-E4405F?style=for-the-badge&logo=instagram&logoColor=white"></a> 
  <a href = "mailto:avidal826@gmail.com"><img src="https://img.shields.io/badge/-Gmail-%23333?style=for-the-badge&logo=gmail&logoColor=white" target="_blank"></a>
  <a href="https://www.linkedin.com/in/arthur-vidal-1860b6269/" target="_blank"><img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" target="_blank"></a> 
</div>

<br>

![Snake animation](https://github.com/vidaal126/vidaal126/blob/output/github-contribution-grid-snake.svg)

name: Generate Snake

on:
  schedule:
    - cron: "0 0 * * *"  # Executa diariamente à meia-noite
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: vidaal126  # Substitua pelo seu nome de usuário
          svg_out_path: dist/github-contribution-grid-snake.svg
          # Gera a cobra com base em todos os commits históricos
          global_range: true

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
