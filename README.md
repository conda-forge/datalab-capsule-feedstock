About datalab-capsule-feedstock
===============================

Feedstock license: [BSD-3-Clause](https://github.com/conda-forge/datalab-capsule-feedstock/blob/main/LICENSE.txt)

Home: https://github.com/DataLab-Platform/DataLab-Capsule

Package license: BSD-3-Clause

Summary: Exchange and verify scientific workspace provenance as open RO-Crate capsules (library and CLI, no DataLab required).

Development: https://github.com/DataLab-Platform/DataLab-Capsule

DataLab-Capsule is the neutral provenance and exchange layer of the DataLab open-source platform.
It records, packages and verifies the processing history of scientific workspaces as capsules
(`.dlcapsule`): ZIP archives holding the HDF5 workspace and an RO-Crate 1.3 manifest conforming to
Process Run Crate 0.6 and to the DataLab capsule profile. It provides integrity primitives (canonical
JSON, SHA-256 digests, signal and image state fingerprints), semantic diff, verification without
computation, revisions and reviews, and a `workspace-capsule` command line. The core needs only
`jsonschema`: install NumPy and h5py to create capsules or check stored states, and FastAPI and
uvicorn to run a capsule registry. It never imports DataLab, Sigima or Qt.

Current build status
====================


<table><tr>
    <td>All platforms:</td>
    <td>
      <a href="https://github.com/conda-forge/datalab-capsule-feedstock/actions/workflows/conda-build.yml">
        <img src="https://github.com/conda-forge/datalab-capsule-feedstock/actions/workflows/conda-build.yml/badge.svg?event=push&branch=main">
      </a>
    </td>
  </tr>
</table>

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-datalab--capsule-green.svg)](https://anaconda.org/conda-forge/datalab-capsule) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/datalab-capsule.svg)](https://anaconda.org/conda-forge/datalab-capsule) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/datalab-capsule.svg)](https://anaconda.org/conda-forge/datalab-capsule) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/datalab-capsule.svg)](https://anaconda.org/conda-forge/datalab-capsule) |

Installing datalab-capsule
==========================

Installing `datalab-capsule` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
conda config --set channel_priority strict
```

How to use
----------

<details>
<summary>With conda</summary>

```
conda install datalab-capsule
```

</details>

<details>
<summary>With mamba</summary>

```
mamba install datalab-capsule
```

</details>

<details>
<summary>With pixi</summary>

```
# for adding to your local project
pixi add datalab-capsule
# for installing globally
pixi global install datalab-capsule
```

</details>

Search package versions
-----------------------

It is possible to list all of the versions of `datalab-capsule` available on your platform:

<details>
<summary>With conda</summary>

```
conda search datalab-capsule --channel conda-forge
```

</details>

<details>
<summary>With mamba</summary>

```
mamba search datalab-capsule --channel conda-forge
```

</details>

<details>
<summary>With pixi</summary>

```
pixi search datalab-capsule --channel conda-forge
```

</details>

<details>
<summary>With mamba repoquery, which may provide more information</summary>

```
# Search all versions available on your platform:
mamba repoquery search datalab-capsule --channel conda-forge

# List packages depending on `datalab-capsule`:
mamba repoquery whoneeds datalab-capsule --channel conda-forge

# List dependencies of `datalab-capsule`:
mamba repoquery depends datalab-capsule --channel conda-forge
```

</details>



About conda-forge
=================

[![Powered by
NumFOCUS](https://img.shields.io/badge/powered%20by-NumFOCUS-orange.svg?style=flat&colorA=E1523D&colorB=007D8A)](https://numfocus.org)

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[Azure](https://azure.microsoft.com/en-us/services/devops/) and [GitHub](https://github.com/)
it is possible to build and upload installable packages to the
[conda-forge](https://anaconda.org/conda-forge) [anaconda.org](https://anaconda.org/)
channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance,
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information, please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating datalab-capsule-feedstock
==================================

If you would like to improve the datalab-capsule recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/datalab-capsule-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks, and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://docs.conda.io/projects/conda-build/en/latest/resources/define-metadata.html#build-number-and-string)
   back to 0.

Feedstock Maintainers
=====================

* [@PierreRaybaut](https://github.com/PierreRaybaut/)

