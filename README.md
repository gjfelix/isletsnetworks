# Comparative analysis of reconstructed architectures from mice and human islets
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

4. **H01_aa_contacts.txt**
5. **H01_ab_contacts.txt**
6. **H01_bb_contacts.txt** 
7. **H01_global_contacts.txt**

These files contain the cell-to-cell contacts identified by the reconstruction algorithm. Contact files are N x N matrices (where N is the number of cells in the islet). The file name indicate the type of cell-to-cell contacts included (aa = alpha-alpha contacts, bb = beta-beta contacts, ab = alpha-beta contacts, global = all the cell-to-cell contacts).
 
8. **H01_ab_network.png**
9. **H01_bb_network.png**

These files are a graphical representation of the alpha-beta and beta-beta networks formed, respectively. 

10. **H01_vis.png**.- Visualization of the reconstructed islet.
