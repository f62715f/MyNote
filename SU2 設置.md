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
% Total Physical Time for dual time stepping simulations (s)
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


```