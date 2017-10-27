# teo-simox-models

## Sumary

This repository cointains the necesary files for working with TEO in the ArmarX enviroment. 

## Instructions

TEO files are located in /simox/teo, the main file is "TEOSimox.xml"

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

They have been added and can be found in /simox/teo/xmlfiles/collisionModels. It is a expaded 3D model over the normal of each plane. The hands need to be more precise model.

## EndEffectors

For grasping capabilities one EndEffector for each hand was added: **RightHandEEF** and **LeftHandEEF**

## Dynamics

The masses and the COM are being calculated.

### Creator

Created by Alvaro Martinez for his bachelor thesis (100317213[at]alumnos.uc3m.es, amrobled[at]ing.uc3m.es), 2017
