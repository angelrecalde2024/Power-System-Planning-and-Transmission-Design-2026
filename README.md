# Power-System-Planning-and-Transmission-Design-2026


This is a repository for different exercises in Power System Planning and Transmission Design methods used in Power System Planning and Transmission Design postgrad course. 

The idea of these self-autonomous notebooks is to enhance the learning experience of the 'planner' (postgrad student) so he can analyze different systems with the same algorithms. 

Here a brief description of each one of the notebooks. The notebooks are grouped by topic.  

LOAD DURATION CURVE PRINCIPLES
* INGP1118_LoadCurveAndLDC.ipynb: very simple introductory notebook to draw load and obtain load duration curve. 

LOAD FORECASTS (crucial in planning)
* INGP1118LongTermLF_MLinearReg.ipynb: Load term load forecast with Multiple Linear Regression method. It can be used to forecast load based on historical data and validate the prediction with statistical indexes (confidence intervals).
* INGP1118_ShortTermLFwithANN.ipynb: Performs a shot term load forecast (1-day) with Artificial Neural Network method based on historical data.
* ING1118_TimeSeries_Wind.ipynb: Obtains a time series model with historical wind data to produce wind speed forecast (1 day). The model fitting method is ARMA(p,q). Each ARMA fits is an iterative maximum-likelihood optimization (matrix operations plus repeated likelihood evaluations).  

ENGINEERING ECONOMICS (crucial for economic evaluation of a portfolio)
* INGP1118_EngineeringEconomics_basic.ipynb: Simple engineering economics calculations (money concepts) for power system investments, it includes evaluation of Present Value, Future Value, CRF, Sinking Fund Deposit. The data entry is manual. 

GENERATION EXPANSION PLANNING
* INGP1118_LDCwithGenerationExpansionPlan.ipynb: The objective is to obtain a preliminar generation expansion plan using screening curves, load duration curve, and an optimization to determine the size of the new generation. Screening curves with intersection hours and cheapest-technology bands are obtained based on the data entry described in a .xlsx workbook with specific format including existing generation, new generation, and load profile. Several plots can be obtained: dispatch stack vs load/adequacy, and capacity stack with load and reserve.
* INGP1118_ScreeningCurve_GenPlan.ipynb: Generation plan is performed using screening curve method. It helps in visualizing capital vs fuel trade-off, why nuclear and coal serve as base generation, why gas turbines serves peak, why CCGT sits in the middle. It gives the optimal mix without solving an optimization problem. 
* INGP1118_LeastCost_GenerationPlan.ipynb: This notebook performs generation expansion planning with the method of least cost (levelized bus-bar analysis). It computes annual energy, base-year annual cost, several economic factors and costs. It outputs results as tables. 

TRANSMISSION EXPANSION PLANNING
* INGP1118_PowerFlow_AC_decoupledDC.ipynb: Introductory notebook to evaluate AC power flow and decoupled AC power flow (DC power flow) using 'pypower' and .xlsx workbook data entry in MATPOWER format. This allows introduction to transmission expansion constraints into more complex problems
* INGP1118_TransmissionExpansion_LinearDC-OPF.ipynb: This notebook implements a Linear Decoupled DC Optimal Power Flow. It considers minimization of total cost of generation with the following constraints: decoupled DC power balance on each bus, generators' limits, and slack angle. There are no power limits in the transmission lines yet. Pyomo + HiGHS are used. Pyomo as the optimization language and HiGHS as the solver.
* INGP1118_TransmissionExpansion_LinearDC-OPF-LineLimits.ipynb: Starting with 'INGP1118_TransmissionExpansion_LinearDC-OPF.ipynb', we enforce transmission lines limits. It considers linear cot function for the generators. Locational Marginal Price is introduced to understand what happens in real markets with congestion and high wind penetration.
* INGP1118_TransmissionExpansion_TEP_DC-OPF.ipynb: Here, a classical transmission expansion problem based in DC-OPF is solved. This problem is modeled as a Mixed Integer Linear Programming problem (MILP)
* INGP1118_TransmissionExpansion_SC_TEP_DC-OPF.ipynb: This notebook solves a classical security constrained transmission expansion planning problem. Mathematically, the planning decision is forced to comply to feasibility after each contingency, so that constraints are replicated over several scenarios and depend on binary investment decisions.
* INGP1118_TransmissionExpansion_SecurityConstr_LinearDC-OPF.ipynb: This solves a Linear security-constrained decoupled DC optimal power flow problem. The quadratic cost functions of the generators are approximated by piecewise linear cost functions. Here, differences between preventive SCOPF and corrective SCOPF are evident and helps in the study of the two cases.


TRANSMISSION DESIGN
* INGP1118_Sag_tension_OHL_table.ipynb: This notebook performs mechanical design verificatrion of overhead transmission conductor by computing mechanical tension under several hypothesis, sag, and summarizes results. Results can be downloaded in a predetermined format ready for project presentation. Up to now, there are several contractors that still use Excel or manually calculate transmission line design. This notebook contributes to that lack of automation when legacy software is extremely expensive for small local contractors. 



Class of 2026 - FIEC - ESPOL

Created and generated by: Dr. Angel A. Recalde, with assistance of AI. 

Assistant Professor ESPOL
