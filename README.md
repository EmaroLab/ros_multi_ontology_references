# ros_multi_ontology_references
The complete ARMOR service: its direct dependencies, and a python client example.
This repository contains four ROS packages:
 - [multi ontology reference](https://github.com/EmaroLab/multi_ontology_reference) library (AMOR)
 - [ARMOR](https://github.com/EmaroLab/armor) (ros_multi_ontology_reference) service package
 - [armor_msgs](https://github.com/EmaroLab/armor_msgs) package
 - [armor_py_api](https://github.com/EmaroLab/armor_py_api)
Each package is a repository connected here via Git [submodule](https://github.com/EmaroLab/docs/wiki/GitHub-Tutorial-to-Manage-Project-with-SubRepositories#clone-the-project).
For **documentation** of each module and **last** releases, refer to the single repository above.

**aRMOR** is a ROS service depending on *AMOR* (a OWLAPI-based library), and *armor_msgs*, which contains the ROSjava-based input and output interfaces of aRMOR.
The project contains also an example of a service's client based on Python based on ROS *api*.

### Contacts
For comment, discussions or support refer to this git repository or contact us at:
 - [luca.buoncompagni@edu.unige.it](mailto:luca.buoncompagni@edu.unige.it),
 - [alessio.capitanelli@dibris.unige.it](mailto:alessio.capitanelli@dibris.unige.it).
