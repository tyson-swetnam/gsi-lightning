---

<span style="font: fsmall-caps bold 24px/1 sans-serif; font-size: 150%">Cyberinfrastructure for scientific reproducibility in data-intensive geospatial research and education</span>

###### January 29, 2018 
###### Tyson Lee Swetnam
###### CyVerse

---

### Contact

[http://www.cyverse.org/](http://www.cyverse.org/)

email: tswetnam@cyverse.org

github: tyson-swetnam

twitter: tswetnam

---

Cloud-based engines already offer compute on massive, long term, data archives

<img src="https://developers.google.com/earth-engine/images/Playground.png" height="250"><img src="https://pbs.twimg.com/media/C6U9LTQVAAE_j0b.png" height="250">

<img src="http://uwm.edu/software/wp-content/uploads/sites/76/2015/10/Big_ArcGIS_Online_logo.png" height="200">

---

More data all the time

<img src="https://pbs.twimg.com/media/DN5ZyIbVwAA7BLB.png" height="250"><img src="http://www.opentopography.org/sites/opentopography.org/files/images/news_items/UNAMcourse_thumb.jpg" height="250">

Planet Labs: daily 3m global coverage; sub meter lidar and sfm at local scale from national repositories.

---

Wow! That's a lot of data and computing power! 

but...

---

How do I utilize those platforms and data at scale?

---

### Option 1: Use a GIS data science workbench

---

Sounds great, what is a data science workbench?

---

<img src="https://www.python.org/static/community_logos/python-logo-inkscape.svg" height="150"> <img src="http://jupyter.org/assets/hublogo.svg" height="150">

---

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
<img src="assets/imagery/aws.png" height="500">

---

## CyVerse [Atmosphere](https://cyverse.org/atmosphere)

+++

- Linux (Centos, Ubuntu)
- 1 CPU  to 16 CPU 
- 4 GB to 128GB RAM 
- Attach (swap) TB size storage volumes    
- emulated web shell and desktop 

---

Disclaimer: Being awesome with cloud and HPC doesn't just happen out of the box. 

<img src="https://consequenceofsound.files.wordpress.com/2016/04/screen-shot-2016-04-08-at-10-33-51-am.png" width="500">

---

@title[Docker RStudio]

## <span style="color: #e49436">Docker + RStudio</span>
[http://learning.cyverse.org/](http://learning.cyverse.org/)
<br>

```shell
$ ezd
$ sudo usermod -aG docker $USER
$ exit
$ docker pull rocker/geospatial
$ docker run -d -p 8787:8787 rocker/geospatial

Done!

```

@[1](install Docker)
@[2](change `sudo` privileges)
@[3](exit and restart terminal window)
@[4](pull the Rocker/Geospatial Rstudio-Server from DockerHub)
@[5](Run the Container in detached mode `-d` on port `-p 8787:8787`)
@[7](Open the Instance's IP address w/ port number in a new browser window)

---

@title[QGIS-GRASS-RStudio native build]

## <span style="color: #e49436">QGIS + GRASS + RStudio</span>
<br>

```shell
$ git clone https://github.com/cyverse-gis/focus-forum.git
$ cd focus-forum/atmo
$ . install_qgis.sh
$ . build_grass.sh
$ . install_rstudio.sh

```

@[1](Clone a public Github Repo)
@[2](Change into the directory with the installation scripts)
@[3](Install QGIS)
@[4](Build GRASS 7.2 from source)
@[5](Install RStudio)
@[6](Open the Instance's IP address w/ port number in a new browser window)
@[7](Launch Web Desktop with Apache Guacamole)

---

<img src="assets/imagery/cyverse.png" height="600">

---