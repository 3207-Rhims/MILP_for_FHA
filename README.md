MILP models for FHA (linear trails and XOR-differential trails)

This repository provides the MILP formulations used in the paper to search for:
  (i) low-weight linear trails (Fu-style modular addition constraints + exact mask propagation),
  (ii) low-weight XOR-differential trails (bit-level model).

Dependencies
- Python 3.x
- Gurobi Optimizer (with gurobipy)

Files
- linear_milp.ipynb : linear-trail MILP (objective: minimize total linear weight W_L)
- differntial_milp.ipynb   : XOR-differential MILP (objective/feasibility on weight W)


Notes
- Round constants are omitted in the linear MILP since constant addition is an affine shift and does not
  affect linear mask feasibility/weight.
- Bit-level MILP instances grow quickly; timeouts for r>=4 are expected under moderate time limits.
