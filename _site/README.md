# Instruction to build the page

1. Open git bash in the root folder,
2. run './script/setting' to make the JekII env (for the first time)
3. run './script/run' to activate the JekyII, go to https://127.0.0.1:4000/ to see the rendered pages.

## Updating contents

### Add publication

- Modify the bib files in '\_bibliography' folder

### Add people

- put the bio photo in assets/images/member/xx.jpg
- Add a md file in the \_team folder with file name of "firstname_lastname" with avatar image name xx.jpg

```markdown
---
name: A B
position: researchstaff/gradstudent/postdoc/intern/visiting/others/alumni
avatar: xx.jpg
twitter:
email: 
scholar: 
web: 
github: 
twitter: 
previous: researchstaff/gradstudent/postdoc/intern/visiting/others/alumni
joined: 2020
left: 2022
current: Samsung
---

<img width="200" src="{{ site.url }}{{site.baseurl}}/assets/images/member/{{page.avatar}}" data-action="zoom">

### Contact

<i class="fa fa-envelope-o"></i> `xx@yy.edu`<br>
<i class="fa fa-building"></i> RIC 1481 <br>
<i class="fa fa-bar-chart"></i> [google scholar](https://scholar.google.com/citations?user=GW6D4ZIAAAAJ&hl=en) <br>
[ari-benjamin.com](https://ari-benjamin.com)

<hr>

### Bio

After graduating from Williams College with a degreee in physics, teaching high school chemistry for a year in Mexico, and obtaining a master's in nanoscale simulation and biomaterials at Northwestern, I joined this awesome lab for computational neuroscience! I'm all about nonlinear life trajectories, which is fair, since the brain is nonlinear too.

<hr>

### Research Interests

What does deep learning have to say about how the brain works? (How does deep learning work?) What is the most fruitful and insightful way to conceptualize the brain?
```

### Add news

- Add an item in \_data/news.yml

```yaml
- date: 2021-02-20
  headline: "Model-based HoloNet got accepted by IEEE TCI!"
  summary: ""
```

### Add co-author

- Add an item in \_data/coauthors.yml

```yaml
Congli:
  url: http://congliwang.github.io
```

## Upload the contents

- On the master branch, commit and push all of the modifications to GitHub
- Open git bash in the root folder, and run './bin/deploy' command, the files will be updated automatically.




## Errors

zsh: permission denied: ./script/deploy

```bash
chmod a+x ./script/deploy
```

env: bash\r: No such file or directory

```bash
change CRLF to LF in VSCode
```