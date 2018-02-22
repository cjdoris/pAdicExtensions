# Miscellaneous
{:#miscellaneous}

<a id="FloorLog"></a><a id="FloorLog--RngIntElt--RngIntElt"></a><a id="FloorLog--RngIntElt--etc"></a>
> **FloorLog** (b :: *RngIntElt*, x :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Equivalent to `Floor(Log(b,x))` but avoids any floating point arithmetic.


<a id="Evaluate"></a><a id="Evaluate--NwtnPgon--etc"></a><a id="Evaluate--NwtnPgon--FldRatElt"></a><a id="Evaluate--NwtnPgon--RngIntElt"></a>
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


<a id="BinomialValuation"></a><a id="BinomialValuation--RngIntElt--etc"></a><a id="BinomialValuation--RngIntElt--RngIntElt--RngIntElt"></a>
> **BinomialValuation** (n :: *RngIntElt*, k :: *RngIntElt*, p :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The `p`-adic valuation of `n` choose `k`.


