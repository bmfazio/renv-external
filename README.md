# External libraries for `renv`

When using `renv` in conjunction with VSCode, ìnteractions will the R terminal will not work properly unless `languageserver` and some other libraries are made available.

A smart way to fix this (i.e. avoiding having to install them in every single project) is by creating a "minimal" `renv` project and then linking its library as an external library to every other project via `renv::settings$external.libraries()`.

Credit goes to Grant McDermott for figuring this out. [[source]](https://github.com/rstudio/renv/issues/1129#issuecomment-1499459762)

This repo is my personal version of such a minimal library. Beyond VSCode-related libraries it also holds package development-related libraries that I often use. It is set to `snapshot.type == "explicit"` so the exact list can be found in the `DESCRIPTION` file.
