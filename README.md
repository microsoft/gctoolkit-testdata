# gctoolkit-testdata

## Introduction

Test assets for [GCToolKit](https://github.com/microsoft/gctoolkit). This collection of files is unlikely to change other than an occasional
addition.

---
NOTE

This project relies on [Git Large File Storage (LFS)](https://git-lfs.github.com/) to store log files that
exceed the GitHub file size limit. Please make sure you have this installed for your local system before working
with this repository (including cloning it).

---

## Getting Started

This test data is used by [gctoolkit](https://github.com/microsoft/gctoolkit).

When the Maven test phase is run in GCToolkit, the test data assets are downloaded as a zip file, which is then unzipped and used in the GCToolKit unit tests.

## Cloning the Repository

To add test artifacts (GC logs) to this repository you should first clone it. *WARNING* Please note that it relies on [Git Large File Storage (LFS)](https://git-lfs.github.com/). 

Consider cloning with a `--depth=1` to reduce the size. This will only clone the last commit.
Make sure you have `git-lfs` installed, and then perform the following commands after a successful `git clone`.

```bash
cd gctoolkit-data
git reset --hard
git lfs install
git lfs pull
```
## Adding Test Data

The GC logs sit in directories who's path helps identify and categorize the data contained in the log. For example, the gc1gc_details_adaptivesizing_reset.log is a JDK 8 G1GC log that contains adaptive sizing and RSet information. It resides in the gclogs/preunified/details/adaptivesize/rset directory.
This convention should be used when adding a new GC log. Additionally, please choose a name that annonimizes the source of the data and ensure that the log file contains no data that would allow one to trace it back to its source.


## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit [https://cla.opensource.microsoft.com](https://cla.opensource.microsoft.com).

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft
trademarks or logos is subject to and must follow
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
