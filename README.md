<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:FF6AC1,50:8A2BE2,100:00F5FF&height=230&section=header&text=I'm%20Denji%20⚡&fontSize=46&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Full-Stack%20Dev%20%7C%20Code%20Devil%20Hunter&descAlignY=58&descSize=18" width="100%"/>

<a href="https://github.com/emmanuelmwangi88-ui">
  <img src="https://readme-typing-svg.demolab.com/?font=Fira+Code&weight=600&size=24&duration=3000&pause=800&color=FF6AC1&center=true&vCenter=true&width=600&lines=Building+things+that+bite+back.;Python+%2F+Django+%2F+JavaScript+dev;Turning+bugs+into+contracts...+one+by+one.;Welcome+to+my+terminal." alt="Typing SVG" />
</a>

<img src="https://komarev.com/ghpvc/?username=emmanuelmwangi88-ui&label=Profile%20Views&color=FF6AC1&style=for-the-badge" alt="profile views"/>
<img src="https://img.shields.io/github/followers/emmanuelmwangi88-ui?label=Followers&style=for-the-badge&color=00F5FF&logo=github&logoColor=white" alt="followers"/>
<img src="https://img.shields.io/badge/Status-Available%20for%20work-8A2BE2?style=for-the-badge&logo=statuspage&logoColor=white" alt="status"/>

</div>

## ⛓️ About Me

```python
class Denji(Developer):
    def __init__(self):
        self.real_name   = "Emmanuel Mwangi"
        self.alias       = "Denji"
        self.role        = "Full-Stack Developer"
        self.stack       = ["Python", "Django", "JavaScript", "SQL", "HTML", "CSS"]
        self.weapon      = "Jupyter Notebook ⚙️"
        self.status      = "Hunting bugs, signing contracts with clean code"
        self.location    = "Kenya 🇰🇪"

    def goals(self):
        return "Ship projects worth showing off, level by level."
```

* 🩸 I write code the way Denji swings a chainsaw — fast, fearless, and a little chaotic until it works.
* 🛠️ Currently leveling up my **backend** game with **Django** and sharpening my **JS** for the frontend fights.
* 🧪 I prototype and explore data in **Jupyter** before bringing it into real projects.
* 📡 Always open to collabs, gigs, and devil-contracts (a.k.a. interesting projects).

## ⚔️ Tech Arsenal

<div align="center">
<img src="https://skillicons.dev/icons?i=python,django,javascript,html,css,mysql,jupyter,git,github,vscode&theme=dark&perline=10" alt="skills"/>
</div>

## 🎯 Currently Leveling Up

<div align="center">

`Django`&nbsp;&nbsp;![](https://img.shields.io/badge/%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88-85%25-8A2BE2?style=flat-square&labelColor=141321)
`JavaScript`&nbsp;&nbsp;![](https://img.shields.io/badge/%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88-75%25-FF6AC1?style=flat-square&labelColor=141321)
`SQL`&nbsp;&nbsp;![](https://img.shields.io/badge/%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88-70%25-00F5FF?style=flat-square&labelColor=141321)
`Python`&nbsp;&nbsp;![](https://img.shields.io/badge/%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88%E2%96%88-90%25-8A2BE2?style=flat-square&labelColor=141321)

<sub>(edit the % anytime — these are just static bars, not auto-tracked)</sub>

</div>

## 📈 Coding Activity

<div align="center">
<img src="https://github-readme-activity-graph.vercel.app/graph?username=emmanuelmwangi88-ui&bg_color=141321&color=00F5FF&line=FF6AC1&point=ffffff&area=true&hide_border=true&area_color=8A2BE2" alt="activity graph" width="95%"/>
</div>

## 📊 Battle Stats

<table align="center">
  <tr>
    <td><img src="https://github-readme-stats.vercel.app/api?username=emmanuelmwangi88-ui&show_icons=true&hide_border=true&bg_color=141321&title_color=FF6AC1&icon_color=00F5FF&text_color=e0e0e0&border_radius=10" alt="GitHub Stats" width="100%"/></td>
    <td><img src="https://github-readme-streak-stats.herokuapp.com/?user=emmanuelmwangi88-ui&hide_border=true&background=141321&ring=8A2BE2&fire=FF6AC1&currStreakLabel=00F5FF&border_radius=10" alt="GitHub Streak" width="100%"/></td>
  </tr>
</table>

<div align="center">
<img src="https://github-readme-stats.vercel.app/api/top-langs/?username=emmanuelmwangi88-ui&layout=compact&hide_border=true&bg_color=141321&title_color=FF6AC1&text_color=e0e0e0&border_radius=10" alt="Top Languages" width="320"/>
</div>

## 🐍 Contribution Snake

<div align="center">
<img src="https://raw.githubusercontent.com/emmanuelmwangi88-ui/emmanuelmwangi88-ui/output/github-contribution-grid-snake-dark.svg" alt="snake animation" width="95%"/>
</div>

<details>
<summary>⚙️ One-time setup (click to expand)</summary>

This image is blank until you add the workflow below. Create a file at `.github/workflows/snake.yml` in this repo with this content, push it, then run it once from the **Actions** tab:

```yaml
name: Generate Snake Animation

on:
  schedule:
    - cron: "0 */12 * * *"   # every 12 hours
  push:
    branches:
      - main
  workflow_dispatch: {}

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    steps:
      - name: Generate snake animation SVG
        uses: Platane/snk@v3
        with:
          github_user_name: emmanuelmwangi88-ui
          outputs: |
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark
            dist/github-contribution-grid-snake.svg

      - name: Push to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

Once the Action finishes, an `output` branch appears with the SVG and the image above will populate automatically.

</details>

## 🏆 Trophy Case

<div align="center">
<img src="https://github-profile-trophy.vercel.app/?username=emmanuelmwangi88-ui&theme=radical&no-frame=true&margin-w=10&row=1&column=7" alt="trophies"/>
</div>

## 🗂️ Featured Projects

<!--
  Once you have real repos pushed, replace this block with pin cards like:

  <table align="center">
    <tr>
      <td><a href="https://github.com/emmanuelmwangi88-ui/YOUR_REPO"><img src="https://github-readme-stats.vercel.app/api/pin/?username=emmanuelmwangi88-ui&repo=YOUR_REPO&hide_border=true&bg_color=141321&title_color=FF6AC1&icon_color=00F5FF&text_color=e0e0e0&border_radius=10" /></a></td>
    </tr>
  </table>
-->

<div align="center">

🚧 *Project showcase loading — first contracts in progress.* 🚧

</div>

## 💬 Quote of the Visit

<div align="center">
<img src="https://quotes-github-readme.vercel.app/api?type=horizontal&theme=radical" alt="quote"/>
</div>

## 📡 Open Contracts (Let's Connect)

<div align="center">

<a href="https://www.instagram.com/itadori_manu/" target="_blank">
  <img src="https://img.shields.io/badge/Instagram-141321?style=for-the-badge&logo=instagram&logoColor=E1306C"/>
</a>
<a href="https://github.com/emmanuelmwangi88-ui" target="_blank">
  <img src="https://img.shields.io/badge/GitHub-141321?style=for-the-badge&logo=github&logoColor=ffffff"/>
</a>

</div>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:00F5FF,50:8A2BE2,100:FF6AC1&height=120&section=footer" width="100%"/>

<div align="center">
<sub>⚡ "I don't fear bugs. Bugs fear me." — Denji, probably ⚡</sub>
</div>