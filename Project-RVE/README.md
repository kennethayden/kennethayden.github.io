Simulating how a metal part deforms means accounting for its internal grain structure, but simulating a full component at grain scale is computationally impossible. The standard approach is the
representative volume element: a small synthetic cube, statistically equivalent to the real material, used as the building block for larger simulations. It is what a finite element model
draws on when it needs to know how the material itself behaves. Everything downstream depends on that equivalence holding, yet checking it thoroughly is laborious enough that evaluation frequently
stops at the simpler descriptors.

This project built an automated pipeline that generates synthetic microstructures from electron backscatter diffraction scans and quantifies how representative each one is.
Statistical descriptors are extracted from the scan, passed to specialized generation software, and the resulting volume is compared back against the source data using quantitative distribution metrics.
The entire pipeline runs unattended in a supercomputing environment, generating and evaluating hundreds of candidate structures in batches.

Turning structural quality into a number made systematic optimization possible. Generation parameters could be swept and ranked on evidence instead of intuition,
which exposed both which parameters actually drive fidelity and where the underlying software hits its representational limits.


### Pipeline
<img alt="workflow" src="https://github.com/user-attachments/assets/56eb66c3-1c70-4a58-aef1-d6d81b3adf64" width="100%" />


### Measured vs. Generated Microstructure
The synthetic volume is built to match the real material statistically, reproducing the distribution of grain sizes, morphology, and crystallographic texture found in the scan.

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h4>EBSD scan of 316L stainless steel:</h4>
      <img alt="ebsd-grain-map" src="https://github.com/user-attachments/assets/ee66491e-2112-41b2-8bc3-921553177d12" width="100%" />
    </td>
  <td width="50%" valign="top">
      <h4>Generated 316L RVE:</h4>
      <img alt="generated-rve" src="https://github.com/user-attachments/assets/f00d936c-94eb-4695-84fd-8b26b40645cb" width="100%" />
    </td>
  </tr>
</table>


### Evaluation
The comparison below shows the texture measured from the real material against that of the generated structure, one of several properties from which a numerical error value is calculated.

Measured:
<img alt="measured texture" src="https://github.com/user-attachments/assets/2281d053-72f4-41b9-9b2e-7f6977b0fce6" width="100%" />

Generated:
<img alt="generated texture" src="https://github.com/user-attachments/assets/a6a8ab24-32f3-473c-baea-d05d25b485ee" width="100%" />
