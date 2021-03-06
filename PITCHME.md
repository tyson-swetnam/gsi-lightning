---

<span style="font: fsmall-caps bold 24px/1 sans-serif; font-size: 150%">Cyberinfrastructure for scientific reproducibility in data-intensive geospatial research and education</span>

###### January 29, 2018 
###### Tyson Lee Swetnam
###### CyVerse University of Arizona

---

##### Institutional Problems

<img src="assets/cavemen.jpg" height="400">

###### Credit: http://bjoern.brembs.net/2018/01/why-academic-journals-need-to-go/

---

##### Data are everywhere...

<img src="https://pbs.twimg.com/media/DN5ZyIbVwAA7BLB.png" height="250">
<img src="assets/planet.png" height="250"><img src="http://www.opentopography.org/sites/opentopography.org/files/images/news_items/UNAMcourse_thumb.jpg" height="250">

---

##### The REAL problem: training researchers

"... PIs said the most pressing unmet needs are training in data integration, data management, and scaling analyses for HPC—acknowledging that data science skills will be required to build a deeper understanding of life." - [Barone et al. 2017](http://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1005755)
---

### Option 1: Cloud engines

<img src="https://developers.google.com/earth-engine/images/Playground.png" height="250"><img src="https://pbs.twimg.com/media/C6U9LTQVAAE_j0b.png" height="250">

<img src="http://uwm.edu/software/wp-content/uploads/sites/76/2015/10/Big_ArcGIS_Online_logo.png" height="200">

---

### Option 2: CyVerse CyberInfrastructure

--- 

<img src="assets/data_store.png" height="600">

---

### The Data science workbench

---

<img src="https://www.python.org/static/community_logos/python-logo-inkscape.svg" height="150"> <img src="http://jupyter.org/assets/hublogo.svg" height="150">

<img src="assets/binder_logo.png" height="150">

---

<img src="http://compass.ie/wordpress/media/OSGeo_logo_750_317.png" height="200">
<img src="https://qgisblog.files.wordpress.com/2016/12/qgis-logo_anita02.png" height="200">
<img src="https://grass.osgeo.org/uploads/images/logo_variant_nobg.png" height="200">

---

<img src="https://www.r-project.org/logo/Rlogo.svg" height="150"> <img src="https://www.rstudio.com/wp-content/uploads/2014/07/RStudio-Logo-Blue-Gradient.png" height="150">

---

### A Data Science Workbench allows you to:

- Send your algorithms to the data and compute <!-- .element: class="fragment" -->
- Work in your preferred environment, language, and libraries <!-- .element: class="fragment" -->
  - Python, R, C++, Matlab, Spark, etc. <!-- .element: class="fragment" -->

---

How do we make this all work together?

---

<img src="https://www.vectorlogo.zone/logos/docker/docker-official.svg" height="350">

---

<img src="http://singularity.lbl.gov/images/logo/logo.svg" height="350">

---

## Why Containerize?

- Dependencies can be wicked problems <!-- .element: class="fragment" -->
- Compiling software is slow <!-- .element: class="fragment" -->
- Reproducability is hard <!-- .element: class="fragment" -->

---

Don't have the money to buy time on private cloud?
<img src="assets/aws.png" height="500">

---

#### [Atmosphere](https://cyverse.org/atmosphere)

- Linux (Centos, Ubuntu)
- 1 CPU  to 16 CPU 
- 4 GB to 128GB RAM 
- Attach (swap) TB size storage volumes    
- emulated web shell and desktop 

---


@title[EZ launch of Docker + RStudio]

## <span style="color: #e49436">Docker + RStudio</span>
[http://learning.cyverse.org/](http://learning.cyverse.org/)
<br>

```shell
$ ezd
$ sudo docker pull rocker/geospatial
$ sudo docker run -d -p 8787:8787 rocker/geospatial

Done!

```

@[1](installs Docker with an Ansible Playbook)
@[2](pull the Rocker/Geospatial Rstudio-Server from DockerHub)
@[3](Run the Container in detached mode `-d` on port `-p 8787:8787`)
@[5](Open the Instance's IP address w/ port number in a new browser window)

---

### Hybrid cloud + HPC (with containers)

---

<img src="assets/singularity.png">

---

<img src="assets/singularity_workflow.png">

---

### Contact Me

[http://www.cyverse.org/](http://www.cyverse.org/)

email: tswetnam@cyverse.org

github: tyson-swetnam

twitter: tswetnam

---
