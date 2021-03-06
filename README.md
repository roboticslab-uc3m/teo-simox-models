# teo-simox-models

## Sumary

This repository cointains the necesary files for working with TEO in the ArmarX enviroment. 

## Instructions

TEO files are located in /teo, the main file is `TEOSimox.xml`.
Names used correspond to those documented [here](https://github.com/roboticslab-uc3m/teo-developer-manual/blob/master/assets/teo-link-names.pdf).
## Kinematic Chains (RobotNodeSets)

**TEO**: All robot joints.

**TrunkChain**: Upper body joints.

**HeadChain**: Head joints.

**RightArmChain**: Right arm joints.

**LeftArmChain**: Left arm joints.

**RightLegChain**: Right leg joints.

**LeftLegChain**: Left leg joints.

**RightHandChain**: Right hand joints

**LeftHandChain**: Left hand joints

## Collision models

They have been added and can be found in /teo/xmlfiles/collisionModels. It is a expanded 3D model over the normal of each plane. They were made with `convexdecomposition` from [OpenRave](https://github.com/roboticslab-uc3m/openrave-yarp-plugins#tutorials-how-to-extract-a-pp-model-from-convexdecomposition). In order to give precision to the hands, they have a `padding` of 0. After they were converted to `.stl` using [this](https://github.com/roboticslab-uc3m/tools/tree/develop/programs/openraveppToSTL).

## EndEffectors

For grasping capabilities one EndEffector for each hand was added: **RightHandEEF** and **LeftHandEEF**

## Dynamics

The robot model has the masses, [centers of mass]( https://github.com/roboticslab-uc3m/teo-simox-models/blob/master/doc/teo-center-of-masses.csv ) and [inertias]( https://github.com/roboticslab-uc3m/teo-developer-manual/blob/master/appendix/b-teo-dynamic-information.md ) of each part.

### Creator

Created by Alvaro Martinez for his bachelor thesis (100317213[at]alumnos.uc3m.es, amrobled[at]ing.uc3m.es), 2017
