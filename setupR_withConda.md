
## Setting up R + RStudio with conda

Conda provides virtualenv for python, and also R. It's great to have everything in one virtualenv in order to build 
pipelines using snakemake.

R set up with conda can be used with jupyter, but I prefer RStudio ofcourse.

This is how we setup conda, R and Rstudio.

+ [Download and install Anaconda](https://www.continuum.io/downloads). No need to worry about python 2 or 3 since we can 
always [create a new environment](http://conda.pydata.org/docs/py2or3.html) with another python version.

+ [Install R within conda](https://www.continuum.io/blog/developer/jupyter-and-conda-r).

+ [Install RStudio](https://support.rstudio.com/hc/en-us/community/posts/209074748-Installing-RStudio-Desktop-on-Ubuntu-16-04-LTS), this is only where I had to use sudo.

+ Finally, make RStudio recognize the R installed in conda. This is done by setting this Environment variable in 
`~/.profile` (or `~/.bash_profile` if present) :

```
RSTUDIO_WHICH_R=/home/user/path/to/anaconda/bin/R
```

Putting this in ~/.bashrc doesn't work since this makes R only accessible within terminal, 
as I learnt [here](http://stackoverflow.com/questions/38534383/how-to-set-up-conda-installed-r-for-use-with-rstudio).

[This solution](https://support.rstudio.com/hc/en-us/community/posts/207830688-Using-RStudio-with-conda) apparantly works 
for mac. Although I don't see myself using mac in near future.

