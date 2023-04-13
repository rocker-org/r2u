
## Rocker: Brief Overview of Versioned and Base

The Rocker Project provides two key sets (or "stacks") of containers which
are non-overlapping by a combination of design, focus, and historical
evolution. See the [discussion of images](https://rocker-project.org/images/)
for a more complete description beyond the brief sketch here.

The rocker-versioned stack provides versioned and time-stamped builds; these
are also the basis for builds providing images with the tidyverse, with
RStudio and Shiny, with a geospatial focus as well as with a machine-learning
focus. 

The r-base stack contains the r-base image as well as builds using r-devel or
specific configuration. The r-base image is based on Debian and takes
advantage of its broad and generally current 'testing' distribution.  Images
based on Ubuntu ("r-ubuntu") have also been added to take advantage of the
c2d4u repo; on top of this image with bspm support ("r-bspm") were added. The
initial r2u container builds are on top of these containers. While some of
the Ubuntu containers are still updated at each Ubuntu releases, a focus on
the two most-recent LTS releases has also been helpful.

We considered streamlining and altering some of these r-base containers but
found that removing features may affect some users. So at least for the time
being the existing containers remain.

## rocker/r2u: Fresh Start 

Since its start in May 2022, the r2u Project has proven to be both useful and
popular. Making it part of Rocker is a natural next step. 

The initial eddelbuettel/r2u containers have been layered on top of r-bspm
and r-ubuntu. For r2u in Rocker we have decided to start directly from Ubuntu
LTS containers. We used this opportunity to rewrite the Dockerfile with fewer
layers resulting in builds that are faster (and simpler) to run, and also
result in smaller containers. These rocker/r2u can be used where the existing
eddelbuettel/r2u containers are, and will likely be uploaded under the
existing tags.



