# mdm-plugin-template

## How to use

* Clone this repository to a new folder

```bash
$ git clone git@github.com:MauroDataMapper-Plugins/mdm-plugin-template.git mdm-plugin-NAME_OF_PLUGIN
```

* Remove this section of the README and update `NAME_OF_PLUGIN` in the markdown template below
* Set `rootProject.name` in `settings.gradle` to `mdm-plugin-NAME_OF_PLUGIN`

TODO write about grails plugins

### Markdown Template

# mdm-plugin-NAME_OF_PLUGIN

| Branch | Build Status |
| ------ | ------------ |
| master | [![Build Status](https://jenkins.cs.ox.ac.uk/buildStatus/icon?job=Mauro+Data+Mapper+Plugins%2Fmdm-plugin-NAME_OF_PLUGIN%2Fmain)](https://jenkins.cs.ox.ac.uk/blue/organizations/jenkins/Mauro%20Data%20Mapper%20Plugins%2Fmdm-plugin-NAME_OF_PLUGIN/branches) |
| develop | [![Build Status](https://jenkins.cs.ox.ac.uk/buildStatus/icon?job=Mauro+Data+Mapper+Plugins%2Fmdm-plugin-NAME_OF_PLUGIN%2Fdevelop)](https://jenkins.cs.ox.ac.uk/blue/organizations/jenkins/Mauro%20Data%20Mapper%20Plugins%2Fmdm-plugin-NAME_OF_PLUGIN/branches) |

## Requirements

* Java 17 (Temurin)
* Grails 5.1.2+
* Gradle 7.3.3+

All of the above can be installed and easily maintained by using [SDKMAN!](https://sdkman.io/install).

## Applying the Plugin

The preferred way of running Mauro Data Mapper is using the [mdm-docker](https://github.com/MauroDataMapper/mdm-docker) deployment. However you can
also run the backend on its own from [mdm-application-build](https://github.com/MauroDataMapper/mdm-application-build).

### mdm-docker

In the `docker-compose.yml` file add:

```yml
mauro-data-mapper:
    build:
        args:
            ADDITIONAL_PLUGINS: "uk.ac.ox.softeng.maurodatamapper.plugins:mdm-plugin-NAME_OF_PLUGIN:1.0.0-SNAPSHOT"
```

Please note, if adding more than one plugin, this is a semicolon-separated list

### mdm-application-build

In the `build.gradle` file add:

```groovy
grails {
    plugins {
        runtimeOnly 'uk.ac.ox.softeng.maurodatamapper.plugins:mdm-plugin-NAME_OF_PLUGIN:1.0.0-SNAPSHOT'
    }
}
```
