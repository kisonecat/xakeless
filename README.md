# the xake is a lie

Xake is the Ximera build tool. This repository demonstrates how to use GitHub Actions to automatically build Ximera `.tex` files into both PDF and HTML formats, and then to deploy the resulting HTML files to GitHub Pages.

Xake was originally [written in Go](https://github.com/XimeraProject/xake) and is being refactored into a LuaTeX‑based system to provide all the functionality of the original version of xake. For that Docker‑powered workflow, see https://github.com/XimeraProject/ximeraFirstSteps/blob/main/xmScripts/xmlatex

## Overview

This repo contains a some sample Ximera content and a [GitHub Actions workflow](https://github.com/kisonecat/xakeless/blob/main/.github/workflows/static.yml) that:

- Checks out your content
- Sets up TeX Live with the required packages
- Compiles each .tex file to PDF (via pdflatex) and HTML (via make4ht)
- Configures GitHub Pages
- Uploads and deploys the generated site

Once the workflow finishes, your course is live and you can use [unxloud](https://github.com/kisonecat/unxloud) to view the content.

