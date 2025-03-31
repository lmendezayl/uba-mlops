#Machine Learning Operations
## Clase 1
Basicamente hicimos un repaso de Inge 2. Trivial.

Actividad sobre Hidden Technical Debt in Machine Learning Systems.

Entanglement. Machine learning systems mix signals together, entangling them and making iso-
lation of improvements impossible. For instance, consider a system that uses features x1, ...xn in
a model. If we change the input distribution of values in x1, the importance, weights, or use of
the remaining n − 1 features may all change. This is true whether the model is retrained fully in a
batch style or allowed to adapt in an online fashion. Adding a new feature xn+1 can cause similar
changes, as can removing any feature xj .

Correction Cascades. There are often situations in which model ma for problem A exists, but a
solution for a slightly different problem A′ is required. In this case, it can be tempting to learn a
model m′
a that takes ma as input and learns a small correction as a fast way to solve the problem.
However, this correction model has created a new system dependency on ma, making it significantly
more expensive to analyze improvements to that model in the future. The cost increases when
correction models are cascaded, with a model for problem A′′ learned on top of m′
a, and so on,
for several slightly different test distributions. Once in place, a correction cascade can create an
improvement deadlock, as improving the accuracy of any individual component actually leads to
system-level detriments.

Buscar sobre:

- Pipeline
- REST API
- Random Forest
- Red Neuronal
- CI/CD

Leer para la semana::
- Huyen, Designing Machine Learning, Capitulo 1.