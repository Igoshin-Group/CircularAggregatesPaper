# Circular Aggregates Paper Simulation Code
Uses Maven based project infrastructure

Source code is in Java language

## Build instructions

- Use an IDE (e.g. Intellij Idea or Netbeans) and setup a maven based project
- (or) in command window run: 
<code>mvn package</code>
- Maven compiles and packages simulation code to <code>CAPaperCode-1.0-SNAPSHOT.jar</code> and all the required dependencies are copied to <code>lib/</code>. Compiled packages are available in <code>target/</code> directory.

## Run instructions

 Copy following files and folders to a separate folder for simulation run:
  * <code>CAPaperCode-1.0-SNAPSHOT.jar</code>
  * <code>lib/</code>
  * <code>Flexicell19_Parameters.xml</code>
  * <code>GlobalParameters_NonGUI.txt</code>

Run simulation using the command in OS command window: <code>java -jar CAPaperCode-1.0-SNAPSHOT.jar</code>

## Simulation run files

 While simulation is running snapshots of current simulation status are stored in <code>images/</code> folder and simulation information is written to files in <code>runData/</code> folder. 

## Precompiled packages

 Precompiled jar packages are available in <code>packages/</code> folder of the github repository 
 
# Simulation parameters used in Circular Aggregates Paper results
Some of the simulation parameters described in Table 2 of the paper correspond to the following parameter names in simulation parameter file <code>Flexicell19_Parameters.xml</code>. Specific parameter values used in each of the result figures are also listed below:

<html>
 <table>
  <thead>
   <tr>
    <th>Parameter name</th>
    <th>Parameter name in simulation file</th>
   </tr>
  </thead>
  <tr>
   <td>Reversal period ($\tau_r$)</td>
   <td>reversalTimeMean</td>
  </tr>
  <tr>
   <td>Adhesion force factor ($\k_{adh}$)</td>
   <td>attractionForceFactor</td>
  </tr>
 </table>
</html>

Due to numerical stability issues in Box2D physics engine at cellular scale (micro.meter length, pico.Newton force etc.), the following conversion factors are used to perform simulation at regular scale (e.g. meter, Newton etc.)

1 micro.meter in cell scale = 1 meter in simulation

$10^-15$ kg in cell scale = 1 kg in simulation

1 min in cell scale = 1 sec in simulation

Correspondingly simulation parameter values indicated in Table 2 of the paper are converted to simulation scale. Converted simulation parameter values are shown below:

## Figure 2
**2A:** cellReversalsFlag = true, reverseTimeMean = 8.0, applySlimeAttractionFlag = true, attractionForceFactor = ??

**2B:** cellReversalsFlag = true, reverseTimeMean = 8.0, applySlimeAttractionFlag = true, attractionForceFactor = ??

**2C:** cellReversalsFlag = false, applySlimeAttractionFlag = true, attractionForceFactor = ??

**2D:** cellReversalsFlag = false, applySlimeAttractionFlag = true, attractionForceFactor = ??

**2E:** cellReversalsFlag = true, reverseTimeMean = 70.0, applySlimeAttractionFlag = true

**2F:** cellReversalsFlag = false, applySlimeAttractionFlag = false

## Figure 3
**3A:** cellReversalsFlag = true, reverseTimeMean = 8.0, applySlimeAttractionFlag = true, attractionForceFactor = ??

**3B:** Data available at the following URL: https://github.com/Igoshin-Group/CA_paper_data/tree/main/Fig%203

## Figure 4
**4A:** cellReversalsFlag = true, reverseTimeMean = 8.0, applySlimeAttractionFlag = true, attractionForceFactor = ??

**4B:** cellReversalsFlag = true, reverseTimeMean = 8.0, applySlimeAttractionFlag = true, attractionForceFactor = ??

**4C&D:** Data available at the following URL: https://github.com/Igoshin-Group/CA_paper_data/tree/main/Fig4
