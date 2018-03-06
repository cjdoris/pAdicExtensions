# Ramification polygons
{:#ramification-polygons}


A `PadRamifPgon` represents a set of points defining a ramification polygon, which is the Newton polygon of the *ramification polygon* `r(x) = f(pi x + pi) / pi^n` of the Eisenstein polynomial `f(x)` of degree `n`. Some of the points need not be vertices, but can lie on the interior of faces, and therefore this is a more refined invariant than just the polygon itself. The points must be of the form `[<1, J_0>, <p^s_1, J_1>, ..., <p^s_u, 0>, ..., <n, 0>]` where `s_u = v_p(n)`.

To each point, we can also assign a non-zero element of the residue class field, which is the leading p-adic coefficients of the corresponding ramification polygon. These are collectively called the *residues* of the ramification polygon. If we multiply the uniformizer of the corresponding extension by the residue `u`, then the residues are all multplied by `u^n`. This defines an equivalence relation between different sets of residues.

Additionally, we can assign a single non-zero element of the residue class field, which we call the *constant coefficient residue*, abbreviated to *CC-residue*, which is the leading p-adic coefficient of the constant coefficient of the corresponding Eisenstein polynomial `f`.


**Contents**
* [Creation](#creation)
* [Basic properties](#basic-properties)
* [Validity](#validity)
* [Enumeration](#enumeration)

## Creation
{:#creation}

<a id="RamificationPolygon"></a><a id="RamificationPolygon--RngUPolElt_FldPadTmpl"></a>
> **RamificationPolygon** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

The ramification polygon of `f`.

**Parameters**
- `Fine`
- `Res`
- `URes`

<a id="RamificationPolygon-2"></a><a id="RamificationPolygon--FldPadTmpl--etc"></a><a id="RamificationPolygon--FldPadTmpl--any"></a>
> **RamificationPolygon** (F :: *FldPadTmpl*, X)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

A ramification polygon over `F`.

**Parameters**
- `Fine`

<a id="IsCoercibleToRamificationPolygon"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--etc"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--any"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--List"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--seq"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--NwtnPgon"></a>
> **IsCoercibleToRamificationPolygon** (F :: *FldPadTmpl*, X)
> 
> **IsCoercibleToRamificationPolygon** (F :: *FldPadTmpl*, X :: *List*)
> 
> **IsCoercibleToRamificationPolygon** (F :: *FldPadTmpl*, X :: [])
> 
> **IsCoercibleToRamificationPolygon** (F :: *FldPadTmpl*, X :: *NwtnPgon*)
> 
> -> *BoolElt*, Any
> {:.ret}
{:.intrinsic}

True if `X` is coercible to a ramification polygon over `F`.







**Parameters**
- `Fine`

## Basic properties
{:#basic-properties}

## Validity
{:#validity}

<a id="IsValid_Points"></a><a id="IsValid_Points--PadRamifPgon"></a>
> **IsValid_Points** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if the points of `P` are valid.


<a id="IsWeaklyValid_Points"></a><a id="IsWeaklyValid_Points--PadRamifPgon"></a>
> **IsWeaklyValid_Points** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if the points of `P` are weakly valid.


<a id="IsValid_Residues"></a><a id="IsValid_Residues--PadRamifPgon"></a>
> **IsValid_Residues** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*, *Tup*
> {:.ret}
{:.intrinsic}

True if the residues of `P` are valid. If true, also returns `<k,y>` such that the uniformizer residue is a `k`th root of `y`.


<a id="IsValid"></a><a id="IsValid--PadRamifPgon"></a>
> **IsValid** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` is valid.


<a id="IsWeaklyValid"></a><a id="IsWeaklyValid--PadRamifPgon"></a>
> **IsWeaklyValid** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` is weakly valid.


<a id="LowerBoundOnEisensteinCoefficient"></a><a id="LowerBoundOnEisensteinCoefficient--PadRamifPgon--etc"></a><a id="LowerBoundOnEisensteinCoefficient--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **LowerBoundOnEisensteinCoefficient** (P :: *PadRamifPgon*, i :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The lower bound on the `i`th coefficient of an Eisenstein polynomial generating `P` due to the point with exponent `s`.


<a id="LowerBoundOnEisensteinCoefficient-2"></a><a id="LowerBoundOnEisensteinCoefficient--PadRamifPgon--etc-2"></a><a id="LowerBoundOnEisensteinCoefficient--PadRamifPgon--RngIntElt"></a>
> **LowerBoundOnEisensteinCoefficient** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The lower bound on the `i`th coefficient of an Eisenstein polynomial generating `P`.


<a id="EisensteinCoefficientIsCritical"></a><a id="EisensteinCoefficientIsCritical--PadRamifPgon--etc"></a><a id="EisensteinCoefficientIsCritical--PadRamifPgon--RngIntElt"></a>
> **EisensteinCoefficientIsCritical** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

True if the `i`th coefficient of an Eisenstein polynomial is critical in determining `P`.


## Enumeration
{:#enumeration}

<a id="AllRamificationPolygons"></a><a id="AllRamificationPolygons--FldPadTmpl--etc"></a><a id="AllRamificationPolygons--FldPadTmpl--RngIntElt"></a>
> **AllRamificationPolygons** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All valid ramification polygons over `F` of degree `n`.

**Parameters**
- `J0`: When given restrict to polygons with vertex `<1,J0>`, i.e. with discriminant valuation `J0+n-1`.
- `Fine := false`: When true, produce fine ramification polygons, where every point is either in or out. Equivalent to calling `AllRefinements` on the outputs.
- `Res := false`: When true, produce polygons with residues. Equivalent to calling `WithAllResidues` on the outputs. Implies `Fine:=true`.
- `URes := false`: When true, produce polygons with uniformizer residues. Equivalent to calling `WithAllUniformzerResidues` on the outputs.
- `Classes := false`: When true, produce only one representative per equivalence class. Only makes a difference when `Res` or `URes` are set.

<a id="AllRefinements"></a><a id="AllRefinements--PadRamifPgon"></a>
> **AllRefinements** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All fine ramification polygons which refine `P`.

**Parameters**
- `Res := false`: As for `AllRamificationPolygons`
- `URes := false`: As for `AllRamificationPolygons`
- `Classes := false`: As for `AllRamificationPolygons`

<a id="WithAllResidues"></a><a id="WithAllResidues--PadRamifPgon"></a>
> **WithAllResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All valid assignments of residues to `P`.

**Parameters**
- `Classes := false`: When true, only return one representative per equivalence class
- `URes := false`: As for `AllRamificationPolygons`

<a id="WithAllUniformizerResidues"></a><a id="WithAllUniformizerResidues--PadRamifPgon"></a>
> **WithAllUniformizerResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All valid assignments of uniformizer residues to `P`.

**Parameters**
- `Classes`

<a id="CorrectTamePoints"></a><a id="CorrectTamePoints--PadRamifPgon"></a>
> **CorrectTamePoints** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The correct tame points for `P`.


<a id="WithCorrectTamePoints"></a><a id="WithCorrectTamePoints--PadRamifPgon"></a>
> **WithCorrectTamePoints** (P :: *PadRamifPgon*)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

A copy of `P` with the correct tame points.


