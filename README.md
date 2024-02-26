Deeply virtual meson production (DVMP) with the EpIC generator

The EpIC generator is used to generate Monte Carlo events for exclusive processes (author: Paweł Sznajder).
https://github.com/pawelsznajder/epic

1. Installation: https://pawelsznajder.github.io/epic/instalation.html

   git clone https://github.com/pawelsznajder/epic.git

   It requires the following external libraries:
   PARTONS
   Qt (version 4 or 5)
   GSL
   ROOT
   HepMC3

   cd build

   cmake ..

   make

   Local installations of external libraries may indicated to CMake with -D option. For instance:
   
   cmake -DHepMC3_DIR=ABSOLUTE_PATH ..

2. Usage: https://pawelsznajder.github.io/epic/usage.html

   ./bin/epic --seed=SEED --scenario=SCENARIO_PATH

   where SEED is the random seed (unsigned integer) to be used in the initialisation of modules that deal with random numbers, and SCENARIO_PATH is the relative or absolute path to the scenario containing all options used in the generation.

   The EpIC scenario (input) file in XML format: https://github.com/eic/DVMPdataset/tree/main/xml

4. Afterburn the output (available in eic-shell):

   abconv -p ip6_hiacc_100x10 10_100_DVMP.txt
