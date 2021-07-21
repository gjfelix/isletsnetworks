# Compara􏰁tiv􏰂e anal􏰃ysis of reconst􏰁ru􏰄ct􏰁ed archi􏰁tec􏰁􏰄tures from mice and h􏰄uman isle􏰁ts
## Datasets, visualizations, contact files and reconstruction logs

### Gerardo J. Félix-Martínez and J. Rafael Godínez Fernández

**Basic description**

- Datasets, visualizations and additional files from human and mouse islets can be found in the corresponding folder.
- Within the Human and Mouse folders you will find a folder for each islet analyzed.
- Folders for human and mouse islets are identified by the letters **H** and **M**, respectively. 
- Islets numbering is the same than that used by Hoang et al. in their datasets.

**Files description**

Within each islet folder you will find the following files (using islet H01 as example):

1. **H01_Experimental_Arch.txt**.- The experimental architecture as provided by Hoang et al. with the following structure:

| Cell type  | x coordinate | y coordinate | z coordinate |
| ----------- | ----------- | ----------- | ----------- |

Cell types are coded as 

- 12: beta 
- 11: alpha 
- 13: delta 

2. **H01_Reconstructed_Arch.txt**: Reconstructed architecture with the following structure:

| Cell radius  | Cell color | Cell type | x coordinate | y coordinate | z coordinate |
| ----------- | ----------- | ----------- | ----------- | ----------- | ----------- |

Note that cell types are coded as described above. The reconstruction algorithm gives as a result the radius and coordinates of the optimized islet.

3. **H01_ReconstructionLog.txt**.- Log file describing the reconstruction process describing the evolution of the optimization algorithm. Parameters included are:

  - **Temperature**: parameter related to the acceptance of islets with a higher number of overlapped cells as a way to prevent getting traped in a local minimum (as the temperature decreases this probability decreases accordingly).
  - **E**: The number of overlapped cells for the current value of Temp.
  - **minE**: minimum number of overlaped cells for the current value of Temp.
  - **maxE**: maximum number of overlapped cells for the current value of Temp.
  - **AcceptN**: Count of accepted islets for the current value of Temp.
  - **TrialN**: Total number of islets generated for the current value of Temp.
  - **Time**: Date and time of completion of the corresponding Temp step. 


