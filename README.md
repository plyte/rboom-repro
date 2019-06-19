# rboom-repro
A repro to recreate an issue with the rboom install from install.packages("Boom")

I've encountered an issue installing the "Boom" package from cran using the install.packages("Boom") command in the R shell.

The error is as follows: 

```
> install.packages("Boom")
Installing package into ‘/usr/local/lib/R/site-library’
(as ‘lib’ is unspecified)
also installing the dependency ‘BH’

trying URL 'https://cloud.r-project.org/src/contrib/BH_1.69.0-1.tar.gz'
Content type 'application/x-gzip' length 12378154 bytes (11.8 MB)
==================================================
downloaded 11.8 MB

trying URL 'https://cloud.r-project.org/src/contrib/Boom_0.9.1.tar.gz'
Content type 'application/x-gzip' length 2111294 bytes (2.0 MB)
==================================================
downloaded 2.0 MB

* installing *source* package ‘BH’ ...
** package ‘BH’ successfully unpacked and MD5 sums checked
** inst
** help
*** installing help indices
** building package indices
** testing if installed package can be loaded
* DONE (BH)
* installing *source* package ‘Boom’ ...
** package ‘Boom’ successfully unpacked and MD5 sums checked
** libs
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c boom_r_tools.cpp -o boom_r_tools.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_point_process.cpp -o create_point_process.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_mixture_component.cpp -o create_mixture_component.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c parse_model_formula.cpp -o parse_model_formula.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c extract_mixture_data.cpp -o extract_mixture_data.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c seed_rng_from_R.cpp -o seed_rng_from_R.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_poisson_process.cpp -o create_poisson_process.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c sufstats.cpp -o sufstats.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c handle_exception.cpp -o handle_exception.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c spike_slab_prior.cpp -o spike_slab_prior.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c list_io.cpp -o list_io.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_poisson_cluster_components.cpp -o create_poisson_cluster_components.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c prior_specification.cpp -o prior_specification.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c determine_nthreads.cpp -o determine_nthreads.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c print_R_timestamp.cpp -o print_R_timestamp.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/PoissonBartModel.cpp -o Models/Bart/PoissonBartModel.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/GaussianLinearBartModel.cpp -o Models/Bart/GaussianLinearBartModel.o
g++ -std=gnu++11 -I"/usr/share/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include"    -fpic  -g -O2 -fdebug-prefix-map=/build/r-base-qEYH9x/r-base-3.5.1=. -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/Bart.cpp -o Models/Bart/Bart.o
```

This is where it hangs for about 20 minutes then outputs this message: 
```
g++: fatal error: Killed signal terminated program cc1plus
compilation terminated.
make: *** [/usr/lib/R/etc/Makeconf:168: create_mixture_component.o] Error 1
make: *** Waiting for unfinished jobs....
```

## Recreate the message:
I've had this same issue on debian, ubuntu, and centos os base images with an R environment containing R 3.5.1. I've also tried 3.6 as well. 

Install docker: 

Windows: https://docs.docker.com/docker-for-windows/install/ (windows 10 pro required)

Ubuntu: https://docs.docker.com/install/linux/docker-ce/ubuntu/


Then run:

docker pull r-base:3.5.1 // this is the official base image by rocker that should be a solid base to test off of

docker run -it r-base

```
R version 3.5.1 (2018-07-02) -- "Feather Spray"
Copyright (C) 2018 The R Foundation for Statistical Computing
Platform: x86_64-pc-linux-gnu (64-bit)

R is free software and comes with ABSOLUTELY NO WARRANTY.
You are welcome to redistribute it under certain conditions.
Type 'license()' or 'licence()' for distribution details.

  Natural language support but running in an English locale

R is a collaborative project with many contributors.
Type 'contributors()' for more information and
'citation()' on how to cite R or R packages in publications.

Type 'demo()' for some demos, 'help()' for on-line help, or
'help.start()' for an HTML browser interface to help.
Type 'q()' to quit R.

> install.packages("Boom")
```

## Possible reason:
Found a forum post about a similar issue that looks to have the same error message: https://community.rstudio.com/t/development-version-of-readr-failing-to-compile/17456/13

It looks like this might be a caching issue?

## Added R CMD CHECK 
```
/Boom.Rcheck# cat 00check.log
* using log directory ‘//Boom.Rcheck’
* using R version 3.5.1 (2018-07-02)
* using platform: x86_64-pc-linux-gnu (64-bit)
* using session charset: UTF-8
* checking for file ‘Boom/DESCRIPTION’ ... OK
* this is package ‘Boom’ version ‘0.9.1’
* package encoding: UTF-8
* checking package namespace information ... OK
* checking package dependencies ... OK
* checking if this is a source package ... OK
* checking if there is a namespace ... OK
* checking for executable files ... OK
* checking for hidden files and directories ... OK
* checking for portable file names ... OK
* checking for sufficient/correct file permissions ... OK
* checking whether package ‘Boom’ can be installed ... ERROR
Installation failed.
See ‘//Boom.Rcheck/00install.out’ for details.
* DONE
Status: 1 ERROR
root@c48170387d8b:/Boom.Rcheck# cat 00install.out
* installing *source* package ‘Boom’ ...
** package ‘Boom’ successfully unpacked and MD5 sums checked
** libs
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c boom_r_tools.cpp -o boom_r_tools.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_point_process.cpp -o create_point_process.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_mixture_component.cpp -o create_mixture_component.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c parse_model_formula.cpp -o parse_model_formula.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c extract_mixture_data.cpp -o extract_mixture_data.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c seed_rng_from_R.cpp -o seed_rng_from_R.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_poisson_process.cpp -o create_poisson_process.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c sufstats.cpp -o sufstats.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c handle_exception.cpp -o handle_exception.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c spike_slab_prior.cpp -o spike_slab_prior.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c list_io.cpp -o list_io.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c create_poisson_cluster_components.cpp -o create_poisson_cluster_components.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c prior_specification.cpp -o prior_specification.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c determine_nthreads.cpp -o determine_nthreads.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c print_R_timestamp.cpp -o print_R_timestamp.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/PoissonBartModel.cpp -o Models/Bart/PoissonBartModel.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/GaussianLinearBartModel.cpp -o Models/Bart/GaussianLinearBartModel.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/Bart.cpp -o Models/Bart/Bart.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/GaussianBartModel.cpp -o Models/Bart/GaussianBartModel.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/LogitBartModel.cpp -o Models/Bart/LogitBartModel.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/ProbitBartModel.cpp -o Models/Bart/ProbitBartModel.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/ResidualRegressionData.cpp -o Models/Bart/ResidualRegressionData.o
g++ -std=gnu++11 -I"/usr/local/lib/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes -DADD_ -DR_NO_REMAP -DBOOST_NO_AUTO_PTR -DEIGEN_WARNINGS_DISABLED -I"/usr/local/lib/R/site-library/BH/include" -I/usr/local/include   -fpic  -g -O2 -fstack-protector-strong -Wformat -Werror=format-security -Wdate-time -D_FORTIFY_SOURCE=2 -g -c Models/Bart/PosteriorSamplers/BartPosteriorSampler.cpp -o Models/Bart/PosteriorSamplers/BartPosteriorSampler.o
g++: internal compiler error: Killed (program cc1plus)
Please submit a full bug report,
with preprocessed source if appropriate.
See <file:///usr/share/doc/gcc-6/README.Bugs> for instructions.
/usr/local/lib/R/etc/Makeconf:168: recipe for target 'create_mixture_component.o' failed
make: *** [create_mixture_component.o] Error 4
make: *** Waiting for unfinished jobs....
ERROR: compilation failed for package ‘Boom’
* removing ‘/Boom.Rcheck/Boom’
```

# Update 6/18/19
Updated the CXX11STD flag to -std=c++11 and the CXX11FLAGS to the one used in the original make file for Boom. I was able to get further than before, but the program hangs after spewing a vast number of "warning: ignoring attributes on template argument 'Eigen::internal::packet_traits<double>::type <aka __vector(2) double}' [-Wignored-attributes]" on various parts of the ../inst/include/Eigen/src/Core/...
  
  I'm also getting some "../inst/include/LinAlg/EigenMap.http:31:60: required from here" messages

Once interupted these are the packages yet left to be built: 
```
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'Models/Glm/PosteriorSamplers/BinomialLogitSpikeSlabSampler.o' failed
make: *** [Models/Glm/PosteriorSamplers/BinomialLogitSpikeSlabSampler.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'Models/HMM/HMM2.o' failed
make: *** [Models/HMM/HMM2.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/QR.o' failed
make: *** [LinAlg/QR.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/Cholesky.o' failed
make: *** [LinAlg/Cholesky.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/SVD.o' failed
make: *** [LinAlg/SVD.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/VectorView.o' failed
make: *** [LinAlg/VectorView.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/LU.o' failed
make: *** [LinAlg/LU.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/Matrix.o' failed
make: *** [LinAlg/Matrix.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/Selector.o' failed
make: *** [LinAlg/Selector.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/Eigen.o' failed
make: *** [LinAlg/Eigen.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/Vector.o' failed
make: *** [LinAlg/Vector.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'LinAlg/SpdMatrix.o' failed
make: *** [LinAlg/SpdMatrix.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'math/cephes/spence.o' failed
make: *** [math/cephes/spence.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'math/cephes/ei.o' failed
make: *** [math/cephes/ei.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'math/cephes/sici.o' failed
make: *** [math/cephes/sici.o] Interrupt
/usr/local/lib/R/etc/Makeconf:176: recipe for target 'math/cephes/rgamma.o' failed
make: *** [math/cephes/rgamma.o] Interrupt
ERROR: compilation failed for package ‘Boom’
* removing ‘/usr/local/lib/R/site-library/Boom’
```

# Update 6/19
I was able to get the package built using a source built version of R. 

The make command was as follows: 
```
g++ -std=gnu++11 -I"/usr/local/lib64/R/include" -DNDEBUG -I. -I../inst/include -IBmath -Imath/cephes  -I"/usr/local/lib64/R/library/BH/include" -I"/usr/local/lib64/R/library/RcppEigen/include" -I/usr/local/include   -fpic  -g -O2
```

During this I received a lot of notes detailing that the specific header used is deprecated:
```
/usr/local/lib64/R/library/BH/include/boost/pending/integer_log2.hpp:7:89: note: #pragma message: This header is deprecated. Use <boost/integer/integer_log2.hpp> instead.
BOOST_HEADER_DEPRECATED("<boost/integer/integer_log2.hpp>");
```
