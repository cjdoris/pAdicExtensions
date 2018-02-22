# Getting Started

## Installation

- Download a copy of the repository [here](https://github.com/cjdoris/pAdicExtensions).
- In Magma, attach the `spec` file (see the example below).

## Example

```
> // Do this once in the session
> AttachSpec("/path/to/package/spec");
>
> // This package avoids working with explicit fields, and
> // instead uses "template" fields which contain just enough
> // information, such as the prime and ramification degree
> F := TemplatepAdicField(3);
>
> // Find the ramification polygons of degree 9 over Q_3
> // with dicriminant valuation 10+9-1=18
> AllRamificationPoints(F, 9 : J0:=10);
[
  Ramification Points [10 . 0; 9],
  Ramification Points [10 3 0; 9],
  Ramification Points [10 6 0; 9]
]
>
> // Pick one
> P := RamificationPoints(F, [<1,10>,<3,3>,<9,0>]);
> P;
Ramification Points [10 3 0; 9]
>
> // Make a template
> T := TemplateForEisensteinPolynomials(P);
> T;
Eisenstein polynomial template over
  Template 3-adic field (f=1, e=1)
with coefficients
   0 min_val=1 (sharp) max_val=3
   1 min_val=2 (sharp) max_val=3
   2 min_val=2 max_val=3
   3 min_val=1 (sharp) max_val=3
   4 min_val=2 max_val=3
   5 min_val=2 max_val=3
   6 min_val=1 max_val=3
   7 min_val=2 max_val=3
   8 min_val=2 max_val=3
   9 1
> // It has a lot of possible outputs!
> #T;
3099363912
> // Generate one of them at random, note that this requires an actual field to work in
> K := pAdicField(3,20);
> f := Random(T, pAdicField(3));
> f;
(1 + O(3^20))*$.1^9 + (5*3^2 + O(3^22))*$.1^8 + (8*3^2 + O(3^22))*$.1^6 + (2*3^3
  + O(3^23))*$.1^5 + (7*3^2 + O(3^22))*$.1^4 + (11*3 + O(3^21))*$.1^3 + (3^2 + 
  O(3^22))*$.1 + 10*3 + O(3^21)
> // Check the ramification polygon
> L<pi> := ext<K | f>;
> Vertices(NewtonPolygon(Evaluate(ChangeRing(f,L), PolynomialRing(L).1 * pi + pi)/pi^9));
[ <0, 179>, <1, 10>, <3, 3>, <9, 0> ]
```