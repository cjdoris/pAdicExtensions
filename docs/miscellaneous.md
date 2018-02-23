# Miscellaneous
{:#miscellaneous}

<a id="FloorLog"></a><a id="FloorLog--RngIntElt--RngIntElt"></a><a id="FloorLog--RngIntElt--etc"></a>
> **FloorLog** (b :: *RngIntElt*, x :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Equivalent to `Floor(Log(b,x))` but avoids any floating point arithmetic.


<a id="Evaluate--NwtnPgon--RngIntElt"></a><a id="Evaluate--NwtnPgon--FldRatElt"></a><a id="Evaluate--NwtnPgon--etc"></a><a id="Evaluate"></a>
> **Evaluate** (P :: *NwtnPgon*, x :: *FldRatElt*)
> 
> **Evaluate** (P :: *NwtnPgon*, x :: *RngIntElt*)
> 
> -> *FldRatElt*
> {:.ret}
{:.intrinsic}

Treating `P` as a piecewise-linear function, evaluates it at `x`.




<a id="FactorialValuation"></a><a id="FactorialValuation--RngIntElt--etc"></a><a id="FactorialValuation--RngIntElt--RngIntElt"></a>
> **FactorialValuation** (n :: *RngIntElt*, p :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The `p`-adic valuation of `n!` (equivalent to `Valuation(Factorial(n),p)` but more efficient).


<a id="BinomialValuation"></a><a id="BinomialValuation--RngIntElt--RngIntElt--RngIntElt"></a><a id="BinomialValuation--RngIntElt--etc"></a>
> **BinomialValuation** (n :: *RngIntElt*, k :: *RngIntElt*, p :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The `p`-adic valuation of `n` choose `k`.


<a id="UnitFactorial"></a><a id="UnitFactorial--FldFin--etc"></a><a id="UnitFactorial--FldFin--RngIntElt"></a>
> **UnitFactorial** (F :: *FldFin*, n :: *RngIntElt*)
> 
> -> *FldFinElt*
> {:.ret}
{:.intrinsic}

The product of the integers up to `n` which are units in `F`. By Wilson's formula, if `n`=kn+r this is (-1)^k * r!.


<a id="ShiftedFactorial--FldFin--RngIntElt"></a><a id="ShiftedFactorial--FldFin--etc"></a><a id="ShiftedFactorial"></a>
> **ShiftedFactorial** (F :: *FldFin*, n :: *RngIntElt*)
> 
> -> *FldFinElt*
> {:.ret}
{:.intrinsic}

The product of the integers up to `n` shifted down to be units of `F`. This is the product of UnitFactorial(`n` div p^i) for all i.


<a id="ShiftedBinomial--FldFin--etc"></a><a id="ShiftedBinomial--FldFin--RngIntElt--RngIntElt"></a><a id="ShiftedBinomial"></a>
> **ShiftedBinomial** (F :: *FldFin*, n :: *RngIntElt*, k :: *RngIntElt*)
> 
> -> *FldFinElt*
> {:.ret}
{:.intrinsic}

The binomial coefficient `n` choose `k` shifted down to be a unit of `F`.


