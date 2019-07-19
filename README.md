# Azure Pipelines cross product example

[![Build Status](https://dev.azure.com/mathias0215/mathias/_apis/build/status/nedrebo.parameterized-azure-jobs?branchName=master)](https://dev.azure.com/mathias0215/mathias/_build/latest?definitionId=3&branchName=master)

This repository shows how to use [each expressions](https://docs.microsoft.com/en-us/azure/devops/pipelines/process/expressions?view=azure-devops) and [template files](https://docs.microsoft.com/en-us/azure/devops/pipelines/process/templates?view=azure-devops) in [Azure Pipelines](https://docs.microsoft.com/en-us/azure/devops/pipelines/?view=azure-devops) to simulate a cross product matrix.

Adding the cross product feature to Azure Pipelines is discussed in [Azure Pipelines GitHub feature request issue #20](https://github.com/Microsoft/azure-pipelines-yaml/issues/20).

This example is a quick hack, it contains duplicated code and can probably be improved. Please open a PR if you have suggestions for a better way. This repository serves as a testbed for the CI/CD improvements in [zivid-python](https://github.com/zivid/zivid-python).

The dummy example used here is parameterized over the following values, resulting in 72 jobs.

| OS               | Python version | SW version |
| ---------------- | -------        | ---------- |
| archlinux/base   | 3.5            | 1.0.0      |
| ubuntu:16.04     | 3.6            | 1.1.0      |
| ubuntu:18.04     | 3.7            | 1.2.0      |
| fedora:31        |                | 1.3.0      |
| vs2017-win2016   |                |            |
| windows-2019     |                |            |
