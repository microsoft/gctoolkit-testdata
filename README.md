# gctoolkit-testdata

# Introduction
Test assets for [GCToolKit](https://github.com/microsoft/gctoolkit). These files are unlikely to change, other than an occasional
addition. The child packages are deployed as zip files. 

# Getting Started
In the top-level pom file, you will see that the project has a dependency on several other test data projects, 
each of which is contained in a subdirectory of the gctoolkit-testdata project.
The pom file of the [gctoolkit](https://github.com/microsoft/gctoolkit) project contains the following dependency:
```xml
            <dependency>
                <groupId>com.microsoft.gctoolkit</groupId>
                <artifactId>gctoolkit-testdata</artifactId>
                <version>1.0.0</version>
                <type>zip</type>
                <scope>test</scope>
            </dependency>
```
When the Maven test phase is run, the dependencies of gctoolkit-testdata are downloaded. The test data assets are downloaded as 
zip files, which must then be unzipped to be used in the GCToolKitunit tests. This is done in the build with the
maven-dependency-plugin:
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
                                    <version>1.0.0</version>
                                    <type>zip</type>
                                </artifactItem>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-gclogs-rolling</artifactId>
                                    <version>1.0.0</version>
                                    <type>zip</type>
                                </artifactItem>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-shenandoah-logs</artifactId>
                                    <version>1.0.0</version>
                                    <type>zip</type>
                                </artifactItem>
                                <artifactItem>
                                    <groupId>com.microsoft.gctoolkit</groupId>
                                    <artifactId>gctoolkit-zgc-logs</artifactId>
                                    <version>1.0.0</version>
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
If one of the test data dependencies changes versions, then the pom file in the GCToolKitproject will need to be updated.

# Build and Test
Because the top-level pom file treats each set of logs as a dependency, each set of log files &mdash; gctoolkit-gclogs, gctoolkit-gclogs-rolling, 
gctoolkit-shenandoah-logs, gctoolkit-zgc-logs &mdash; must be in its own package. About all one can do with these log files
is release them to github packages. For each package, 

`mvn package deploy`

# Contribute

Please note that his project uses [Git Large File Storage (LFS)](https://git-lfs.github.com/) to store log files that exceed the 
github file size limit. 

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

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
