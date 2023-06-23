```
% ------------------------- Solver definition ---------------------------
%
% Type of solver 
SOLVER = EULER
%
% Restart solution (NO, YES)
RESTART_SOL = NO
%
% Iteration number to begin unsteady restarts (used if RESTART_SOL= YES)
RESTART_ITER = 0
%
```

---

```
% ------------------------- Time-dependent Simulation -------------------
% To enable a time-dependent simulation set the option `TIME_DOMAIN` to `YES` (default is `NO`)
%
TIME_DOMAIN = YES
%
% Time Step for dual time stepping simulations (s)
TIME_STEP = 1.0
%
% Total Physical Time for dual time stepping simulations (s) ------ 不會
MAX_TIME = 50.0
%
% Number of internal iterations ---- 每個時間步內的迭代次數使用 `INNER_ITER` 選項進行控制
%
INNER_ITER = 200
%
% Number of time steps
TIME_ITER = 200
%
```

---
```
% ------------------------- Steady-state Simulation ----------------------
TIME_DOMAIN = NO 
% 也可不寫
%
% 以下作用一樣，二選一，若都存在，su2會以INNER_ITER優先
INNER_ITER = 200
ITER = 200

```

---
```
% ------------------ Coefficient-based Convergence Criteria --------------
% e.g. CONV_FIELD= RMS_PRESSURE, RMS_VELOCITY-X, RMS_VELOCITY-Y, RMS_TKE, RMS_SPECIES
CONV_FIELD= DRAG
%
% Number of elements to apply the criteria
CONV_CAUCHY_ELEMS= 100
%
% Epsilon to control the series convergence
CONV_CAUCHY_EPS= 1E-10
%
% `CONV_STARTITER` defines when the solver should start monitoring the criterion.
CONV_STARTITER= 0
```

---

```
% 暫態
% ------------------ Coefficient-based Windowed Time Convergence Criteria 
% Activate the windowed cauchy criterion
WINDOW_CAUCHY_CRIT = YES
%
% Specify convergence field(s)
CONV_WINDOW_FIELD= (TAVG_DRAG, TAVG_LIFT)
%
% Number of elements to apply the criteria
CONV_WINDOW_CAUCHY_ELEMS= 100
%
% Epsilon to control the series convergence
CONV_WINDOW_CAUCHY_EPS= 1E-3
%
% Number of iterations to wait after the iteration specified in  WINDOW_START_ITER.
CONV_WINDOW_STARTITER = 10
%
% Iteration to start the windowed time average
WINDOW_START_ITER = 500
%
% Window-function to weight the time average. Options (SQUARE, HANN, HANN_SQUARE, BUMP), SQUARE is default.
WINDOW_FUNCTION = HANN_SQUARE
```

---
[Solver Setup](https://su2code.github.io/docs_v7/Solver-Setup/)