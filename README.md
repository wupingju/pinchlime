# Pinchlime Site

This repository contains the source for a static site built with [Zola](https://www.getzola.org/).

## Continuous Integration

A GitHub Actions workflow is provided at `.github/workflows/build.yml` to verify that the site builds successfully. The job installs Zola version 0.19.2 and runs `zola build`. Any build failures will cause the workflow to fail.

