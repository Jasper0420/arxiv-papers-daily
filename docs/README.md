<p align="center">
  <h1 align="center"><br><ins>ARXIV-PAPERS-DAILY</ins><br>Automatically Update Arxiv Papers Daily using Github Actions</h1>

</p>



## Overview

This codebase is composed of the following parts:

- `daily_arxiv.py`: main scripts to processing given configurations
- `config.yaml`: configuration file of papers' keywords etc.

## Usage

<details open>
  <summary>Table of Contents</summary>


1. Fork this [repo](https://github.com/Jasper0420/arxiv-papers-daily)

2. Edit configs:

   - Change `GITHUB_USER_NAME` and `GITHUB_USER_EMAIL` in [arxiv-papers-daily.yml](../.github/workflows/arxiv-papers-daily.yml) and [update_paper_links.yml](../.github/workflows/update_paper_links.yml)
   - Change `user_name` in [config.yaml](../config.yaml)![image-20240718141343837](https://s2.loli.net/2024/07/18/JIy9H4ULl17uFOq.png)
   - Change `keywords` to search.And the content of the `.md `file should match the keywords

   ![image-20240718141601815](https://s2.loli.net/2024/07/18/lGTNwy6g1FcpHf3.png)

   ![image-20240718141651166](https://s2.loli.net/2024/07/18/o8uXqwb2lir6Tpg.png)

   - If you want to delete my content , please delete the`json file`content ! Otherwise the content will be messed up !

     ![image-20240718141112333](https://s2.loli.net/2024/07/18/QrXytnSqPjCMxLv.png)

   - Push changes to remote repo

3. Config Github Actions

   - Enable read and write permissions: Setting -> Actions -> Workflow permissions, select `Read and write permissions` and save.
     ![](../assets/4-ga-2-1.png)

   - Enable workflows: Actions -> `I understand my workflows, go ahead and enable them` -> Select `Run Arxiv Papars Daily` in right sidebar and click `Enable workflow` -> click `Run workflow` wait about 1 min until the job update done. The same for the job `Run Update Paper Links Weekly`.
     ![](../assets/4-ga-3-1.png)

     ![](../assets/4-ga-7.png)
     ![](../assets/4-ga-8.png)
     ![](../assets/4-ga-9.png)

4. Setting Gitpages (optional)

   - Setting -> Pages -> Build an deployment. Source: `Deploy from a branch`; Branch select `main` and `/docs` folder, then save.
     ![](../assets/5-pages-1.png)
   - Now you can open gitpage: https://your_github_usrname.github.io/arxiv-papers-daily

5. Add new keywords (optional)

   - Edit `keywords` in [config.yaml](../config.yaml), you can add more filters or keywords.
   - Push changes to remote repo and re-run Github Actions Manually.

</details>

## Release plan

 We are still in the process of fully releasing. Here is the release plan:

- [x] Configuration file
- [x] Update code link
- [ ] Subscribe & Update alerting
- [ ] Support more `arxiv` filters
- [ ] Archive old papers
- [ ] Language translation ([`ChatGPT`](https://chat.openai.com/chat))
- [ ] Usefull comments
- [ ] ...

## Acknowledgement

:heart::heart::heart:This project is based on the original author @[Vincentqyw](https://github.com/Vincentqyw) implementation, for more details please learn about this [rope](https://github.com/Vincentqyw/cv-arxiv-daily)!