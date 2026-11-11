# Access Control Lists

`Model_Access_Register.csv` preserves 2,577 model-access declarations. Operation evidence totals are: {'c': 1652, 'r': 2468, 'u': 1678, 'd': 1392}. The clone must evaluate create/read/update/delete permissions before model operations, resolve group inheritance, and return explicit authorization failures.

Effective access must be tested after module installation and group assignment because static rows do not establish the final runtime matrix.
