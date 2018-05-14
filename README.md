#  CS158 - Computer Simulation final project
## Introduction
Simulates the spread of measles through a grid of 60x56 cells. Cells have a period of virality in which they can pass measles to neighboring cells. To decide whether a cell is infected or not, this period and the probability of infection despite vaccination is calculated. Random values are used to generate new test cases.

Variables that build the environment include **vaccination rate**, **probability of being initially infected** and **probability of being an empty cell**. Once these variables are decided, Current!B1 can be changed into **1** to run the simulation. Refreshing Excel with F9 will increment the number of days (Current!B2).

The simulation will end when there are no more viral cells (Current!E1 lists the number remaining), or when all cells are infected. The environment's end details will be logged to the Result sheet for averaging.

## Sheets
### Current
The visualization of the spread. Has 3 kinds of cells:
- Green cells are uninfected, have a value of -1
- Black cells are obstacles/structures, have a value of 0
- Red cells are infected, have a value of 1

Variables and Details include:
- Viral Remaining, the number of viral cells (cells that can spread infection)
- Vaccination Rate, editable to increase how many cells are vaccinated
- Total Infected, the number of infected cells
- Total people, the number of cells
- Perfect infected
- Vaccined Infected, the number of cells that are infected despite vaccination

### Results
Shows the results of each trial given some vaccination rate. A new trial log starts after setting Current!B2 to 1.
The results can be reset by setting Result!A38 to 1. Don't forget to set it back to 0 to log. 

### Randomized Sheets
Vaccinated, Symptoms Start, Random Values are randomly generated. 

### Other Sheets
Infected Neighbors, Viral, InfectedWVaccine are used for varying purposes, to keep track of infected cells, calculate probablity of being infected despite vaccine, etc

## Trying the simulator
1. Change Current!B1 to 0 to stop the simulation, and change it to 1 to start the simulation
2. Edit Current!G2 to whatever rate, from 0 to 1
3. Current!T2 and Current!V2 are editable as well
4. Start the simulation, and hold F9 until Current!E2 is None
5. You can restart the simulation. Repeated trials will be logged to Result sheet