# CARROTS MMC

This is the firmware repository used in the CARROTS project
("Cooperative modulAr multilevel conveRter: a poweR, cOntrol and daTa collaborative Study").

The repository contains the embedded software used to run a modular multilevel converter (MMC) arm on OwnTech SPIN boards. 

The software stack is designed to be used with VS Code and PlatformIO.
[Installing VS Code with PlatformIO](https://platformio.org/install/ide?install=vscode).


## Downloading CARROTS MMC

You first need to download the repository using the following command:

`git clone https://github.com/owntech-foundation/MMC.git carrots_mmc`

Then, open VS Code and, if not already done, install the PlatformIO plugin.

Finally, open the `software` folder from the cloned repository using menu `File > Open Folder...`


### Structure of the project

The full hierarchy of the project is as follows:

```text
carrots_mmc
|-- docs
|-- schematics
|-- software
|   |-- owntech
|   |-- src
|   |   `-- main.cpp
|   |-- zephyr
|   |   |-- boards
|   |   |-- dts
|   |   |-- modules
|   |   |-- CMakeLists.txt
|   |   `-- prj.conf
|   |-- platformio.ini
|   `-- west.yml
|-- LICENSE
`-- README.md
```

The `software/owntech` folder contains PlatformIO helper scripts and board integration, while the `software/zephyr` folder contains board descriptions, Zephyr configuration and the communication modules used by the project.
By default, most project work happens in `software/src/main.cpp` and `software/platformio.ini`.

Advanced Zephyr configuration can be tweaked by editing `software/zephyr/prj.conf`.
