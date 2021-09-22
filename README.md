# gctoolkit-testdata

## Introduction

Test assets for [GCToolKit](https://github.com/microsoft/gctoolkit). These files are unlikely to change, other than an occasional
addition. The child packages are deployed as zip files.

---
NOTE

This project relies on [Git Large File Storage (LFS)](https://git-lfs.github.com/) to store log files that
exceed the GitHub file size limit. Please make sure you have this installed for your local system before working
with this repository (including cloning it).

---

## Getting Started

This test data is used by [gctoolkit](https://github.com/microsoft/gctoolkit). To build gctoolkit, you need to
[authenticate to GitHub packages with a personal access token (PAT)](https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-apache-maven-registry#authenticating-with-a-personal-access-token).

If your organization uses Single Sign-On (SSO), also follow the directions under [Authorizing a personal access token for use with SAML single sign-on](https://docs.github.com/en/github/authenticating-to-github/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on).
You must also add github as a server in your `~/.m2/settings.xml` file. Replace USERNAME with your GitHub user name and TOKEN with your PAT.

```xml
    <server>
      <id>github</id>
      <username>USERNAME</username>
      <password>TOKEN</password>
    </server>
```

The [gctoolkit pom file](https://github.com/microsoft/gctoolkit/blob/main/pom.xml) contains the following dependency:

```xml
            <dependency>
                <groupId>com.microsoft.gctoolkit</groupId>
                <artifactId>gctoolkit-testdata</artifactId>
                <version>1.0.2</version>
                <type>zip</type>
                <scope>test</scope>
            </dependency>
```

When the Maven test phase is run, the test data assets are downloaded as zip files, which are then unzipped and used in the GCToolKit unit tests.
This is done in the GCToolKit build with the maven-dependency-plugin:

```xml
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-dependency-plugin</artifactId>
                <version>3.1.1</version>
                <inherited>false</inherited>
                <executions>
                    <execution>
                        <id>download-test-logs</id>
                        <phase>process-test-resources</phase>
                        <goals>
                            <goal>unpack</goal>
                        </goals>
                        <configuration>
                            <skip>${skipUnpack}</skip>
                            <artifactItems>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-gclogs</artifactId>
                                    <version>1.0.2</version>
                                    <type>zip</type>
                                </artifactItem>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-gclogs-rolling</artifactId>
                                    <version>1.0.2</version>
                                    <type>zip</type>
                                </artifactItem>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-shenandoah-logs</artifactId>
                                    <version>1.0.2</version>
                                    <type>zip</type>
                                </artifactItem>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-zgc-logs</artifactId>
                                    <version>1.0.2</version>
                                    <type>zip</type>
                                </artifactItem>
                            </artifactItems>
                            <includes>**/*</includes>
                            <outputDirectory>${project.basedir}/gclogs
                            </outputDirectory>
                        </configuration>
                    </execution>
                </executions>
            </plugin>

```

## Build and Test

About all one can do with these log files is release them to GitHub packages, or install a local copy.
A GitHub action has been created to deploy the assets to GitHub packages.

If you choose to clone this repository, please note that it relies on [Git Large File Storage (LFS)](https://git-lfs.github.com/). 

Consider cloning with a `--depth=1` to reduce the size. This will only clone the last commit.
Make sure you have `git-lfs` installed, and then perform the following commands after a successful `git clone`.

```bash
cd gctoolkit-data
git reset --hard
git lfs install
git lfs pull
```

## Contribute

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
