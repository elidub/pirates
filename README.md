# _Pirates_

With PIxel RATio ESimation (_pirates_), solves the problems when determining posteriors of an arbitrary number of interchangable objects. It is built upon [swyft](https://github.com/undark-lab/swyft) using Truncated Marginal Neural Ratio Estimation (TMNRE).

Do you want to **estimate the posterior of an unknown number of interchangeable objects**? Then *pirates* might help you, because it:
- determines the *pixel posterior probability* of an object being in a user-defined pixel.
- let the user define the number of input and output dimensions.
- performs likelihood-free inference by estimating the likelihood-to-evidence ratio using TMNRE.
- validates the results.

<img src="docs/figures/propaganda.PNG">

### Setup
```bash
pip install pirates
```

### Tutorial
Imagine you have a simulator that produces 3 dimensional data `data` representing the intensity in space <img src="https://render.githubusercontent.com/render/math?math=(x, y)"> with objects that are described by <img src="https://render.githubusercontent.com/render/math?math=(x, y, M)">. One can let *Pirates* estimate the posterior of an object in a pixel <img src="https://render.githubusercontent.com/render/math?math=(x, y, M)">.
```python
pir.train(data, theta, data_dims = [0, 1], theta_dims = [0, 1, 2], dims = dict('x'=80, 'y'=80, 'M'=12)
pir.plot2D(['x', 'y']) # 2D plot of pixel posterior probabilities marginalizing over M
pir.plot3D(['x', 'y', 'M']) # interacitve 3D plot of pixel posterior probabilities
```

### Links
* **Documentation & installation**: https://pires.readthedocs.io/en/latest/
* **Example usage**: https://pires.readthedocs.io/en/latest/tutorial-notebooks.html
* **Source code**: https://github.com/elidub/pires
* **Support & discussion**: https://github.com/elidub/pires/discussions
* **Bug reports**: https://github.com/elidub/pires/issues
* **Contributing**: https://pires.readthedocs.io/en/latest/contributing-link.html
* **Citation**: https://pires.readthedocs.io/en/latest/citation.html


