[![Open in GitHub Codespaces](
  https://img.shields.io/badge/Open%20in%20GitHub%20Codespaces-333?logo=github)](
  https://codespaces.new/dwave-examples/3d-bin-packing?quickstart=1)


# MV-22B Load Plan
## 3D Modeling
Given cargo dimensions and weights, MV-22B load plans can be created by scanning the cargos. Here, cargos were scanned using iPhone 13 lidar with Polycam application, which coverts the collected data into CAD file. 3D modeling software such as Sketchup can be used to visualize the CAD files in 3D. This allows you to test out optimal distribution of cargos and determine the number of aircraft required to transport given cargos without physically moving them. This reduces the workload of the crewchiefs and increases the accuracy of the load plans.

![3D Load Plans](https://github.com/user-attachments/assets/322288d6-e563-4a50-87a1-6edb19f58ca8)



## D-Wave 3D Bin Packing
The load planning process can also be automated using D-Wave 3D Bin Packing application which uses hybrid quantum-classical framework to optimize the problem.

Source: https://github.com/dwave-examples/3d-bin-packing

Three files are edited to include the center of gravity constraints.
1. Input file includes weights
2. utils file read_instance includes case weights
3. packing3d file includes an additional objective to minimize the longitudinal center of gravity. Center of gravity is set to x=0 in this case. 

Below is the demonstration of D-Wave 3D Bin Packing application with typical cargos of MV-22B, such as JMICs, Pelican cases, and toolboxex.

<img width="825" alt="D_wave_Demo" src="https://github.com/user-attachments/assets/99043f92-45f6-4b73-a1c9-61c8e1ae0af4">

Further improvement is needed for an arbitrary center of gravity.