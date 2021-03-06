# olca-updates
This project provides the update functionality for [openLCA](http://openlca.org). 
Since version version 1.6 the [openLCA application](https://github.com/GreenDelta/olca-app) 
is using this component to update existing databases. The updates are Python
scripts that are executed using [Jython](http://www.jython.org/). Each update
script is located in a folder under [update-src](./update-src) which contains
the script and a meta-data file `meta-info.json` respectively. The name of such
a folder follows the following pattern:

```
<update number>_<short name>_<uuid[0:2]>_<uuid[33:36]>
``` 

with:
* `update number`: a three digit number that order the folders
* `short name`: a short description of the update
* `uuid[0:2]`: the first two characters of the update UUID (together with the 
  field below, useful to identify dependencies)
* `uuid[33:36]`: the last two characters of the update UUID

## Installation
In order to install the update module, you need to have a 
[JDK 8](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
and [Maven 3](https://maven.apache.org/install.html) installed.
[Download](https://github.com/GreenDelta/olca-updates/archive/master.zip) 
the repository (or get it via git), navigate to the root folder and type the 
following command in your console:

```bash
cd  olca-updates
mvn install
```

This will build the module from source and install it into your local 
Maven repository. 

## License
Unless stated otherwise, all source code of the openLCA project is licensed 
under the [Mozilla Public License, v. 2.0](http://mozilla.org/MPL/2.0/). Please 
see the LICENSE.txt file in the root directory of the source code.
 
