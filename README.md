# A Ros Multi Ontology References (aRMOR)
The complete ARMOR service: its direct dependencies, and a python client example.
This repository contains four ROS packages:
 - [multi ontology reference](https://github.com/EmaroLab/multi_ontology_reference) (AMOR)
 - [armor](https://github.com/EmaroLab/armor)
 - [armor_msgs](https://github.com/EmaroLab/armor_msgs) 
 - [armor_py_api](https://github.com/EmaroLab/armor_py_api)

**aRMOR** is a ROS service depending on *AMOR* (a OWLAPI-based library), and *armor_msgs*, which contains the ROSjava-based input and output interfaces of aRMOR.
The project contains also an example of a Python service's client that uses our *api* to perform some simple manipulations and queries to a [test](https://github.com/EmaroLab/armor_py_api/blob/master/test/test.owl) OWL ontology.

# Gettint Started
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

You can further test the server by using for instance
```
rosservice call /armor_interface_srv "armor_request:
    client_name: ''
    reference_name: 'reference'
    command: 'QUERY'
    primary_command_spec: 'CLASS'
    secondary_command_spec: 'RESTRICTIONS'
    args: ['Class_4']" 
```
Check here the complete list of requests thet the service can digest.
For more **documentation** about each modules and the **last** releases, refer to the links of the four repositories above.

# Known issues

aRMOR gives an elementary interface to SPARQL ([issue](https://github.com/EmaroLab/armor/issues/5#issuecomment-479956294)).
We made aMOR in order to accommodate a better support for SPARQL, but we are not planning to support them soon.
If you want to contribute and share your idea or findings, we are happy to help.

Also, it is recommended to use ontology with entities having a common IRI root.
For importing entities with different IRIs and convert them to a common root we use the ontology editor [Protege](https://protege.stanford.edu/).

We use such an editor also for designing ontological structures that do not change at run-time.
Indeed aMOR does not support the whole OWL operators, but it focus only on the once that most often are needed in robotic applications.
Therefore, it is common to design complex but static semantic off-line, and load them through file at run-time with manipulation and querying purposes.

### Contacts
For comment, discussions or support git **issues** are welcome.
For other notices you can contact us at:
 - [luca.buoncompagni@edu.unige.it](mailto:luca.buoncompagni@edu.unige.it),
 - [alessio.capitanelli@dibris.unige.it](mailto:alessio.capitanelli@dibris.unige.it).

### Related Publication
If aMOR is usefull for your applications, please **cite** our related work:
 - Buoncompagni, Luca, and Capitanelli, Alessio, and Mastrogiovanni, Fulvio: "[A ROS multi-ontology references service: OWL reasoners and application prototyping issues](http://ceur-ws.org/Vol-2352/short7.pdf)". In: Proceedings of the 5th Italian Workshop on Artificial Intelligence and Robotics (AIRO) A workshop of the XVII International Conference of the Italian Association for Artificial Intelligence. CEUR-WS, Trento, Italy (2018).

Scenarios in which we used aRMOR are:
 - Buoncompagni, Luca, and Fulvio Mastrogiovanni. "[Dialogue-based supervision and explanation of robot spatial beliefs: a software architecture perspective](Buoncompagni, Luca, and Fulvio Mastrogiovanni. "Dialogue-based supervision and explanation of robot spatial beliefs: a software architecture perspective." 2018 27th IEEE International Symposium on Robot and Human Interactive Communication (RO-MAN)". IEEE, 2018.) 2018 27th IEEE International Symposium on Robot and Human Interactive Communication (RO-MAN). IEEE, 2018.
 - Capitanelli, Alessio, and Maratea, Marco, and Mastrogiovanni, Fulvio, and Vallati, Mauro (2018). "[On the manipulation of articulated objects in human–robot cooperation scenarios](https://arxiv.org/pdf/1801.01757.pdf)". Robotics and Autonomous Systems, 109, 139-155.
