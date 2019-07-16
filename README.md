# ros_multi_ontology_references
The complete ARMOR service: its direct dependencies, and a python client example.
This repository contains four ROS packages:
 - [multi ontology reference](https://github.com/EmaroLab/multi_ontology_reference) library (AMOR)
 - [ARMOR](https://github.com/EmaroLab/armor) (ros_multi_ontology_reference) service package
 - [armor_msgs](https://github.com/EmaroLab/armor_msgs) package
 - [armor_py_api](https://github.com/EmaroLab/armor_py_api)

**aRMOR** is a ROS service depending on *AMOR* (a OWLAPI-based library), and *armor_msgs*, which contains the ROSjava-based input and output interfaces of aRMOR.
The project contains also an example of a Python service's client that uses our *api* to perform some simple manipulation and query to a [test](https://github.com/EmaroLab/armor_py_api/blob/master/test/test.owl) OWL ontology.

Each package is a Git sub-module (i.e., a repository, see [here](https://github.com/EmaroLab/docs/wiki/GitHub-Tutorial-to-Manage-Project-with-SubRepositories#clone-the-project) for a simple guide).
For installing the progect use:
 - `cd your_caktnig_ws/src`
 - `git clone git clone https://github.com/EmaroLab/ros_multi_ontology_references.git`
 - `cd ros_multi_ontology_references/`
 - `git submodule update --init --recursive --remote`
 - `cd ..`
 - `catkin_make`

For runnig the project use in different terminals:
 - `rosrun armor execute it.emarolab.armor.ARMORMainService`
 - `rosrun armor_py_api client_test.py`

For **documentation** of each module and **last** releases, refer to the single repository above.

# Related Pubblications

Buoncompagni, L., Capitanelli, A., Mastrogiovanni, F.: [A ROS multi-ontology references service: OWL reasoners and application prototyping issues](http://ceur-ws.org/Vol-2352/short7.pdf). In: Proceedings of the 5th Italian Workshop on Artificial Intelligence and Robotics (AIRO) A workshop of the XVII International Conference of the Italian Association for Artificial Intelligence. CEUR-WS, Trento, Italy (2018).

### Contacts
For comment, discussions or support refer to this git repository or contact us at:
 - [luca.buoncompagni@edu.unige.it](mailto:luca.buoncompagni@edu.unige.it),
 - [alessio.capitanelli@dibris.unige.it](mailto:alessio.capitanelli@dibris.unige.it).
