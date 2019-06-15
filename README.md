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
