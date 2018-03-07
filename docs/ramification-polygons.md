# Ramification polygons
{:#ramification-polygons}


A `PadRamifPgon` represents a set of points defining a ramification polygon, which is the Newton polygon of the *ramification polygon* `r(x) = f(pi x + pi) / pi^n` of the Eisenstein polynomial `f(x)` of degree `n`. Some of the points need not be vertices, but can lie on the interior of faces, and therefore this is a more refined invariant than just the polygon itself. The points must be of the form `[<1, J_0>, <p^s_1, J_1>, ..., <p^s_u, 0>, ..., <n, 0>]` where `s_u = v_p(n)`.

To each point, we can also assign a non-zero element of the residue class field, which is the leading p-adic coefficient of the corresponding ramification polygon. These are collectively called the *residues* of the ramification polygon. If we multiply the uniformizer of the corresponding extension by the residue `u`, then the residues are all multplied by `u^n`. This defines an equivalence relation between different sets of residues.

Additionally, we can assign a single non-zero element of the residue class field, which is the *uniformizer residue* (as defined [here]({{site.baseurl}}/template-p-adic-fields)) of an extension defined by `f`. That is, it is the leading p-adic coefficient of the constant coefficient of `f`.


**Contents**
* [Creation](#creation)
* [Validity](#validity)
* [Equivalence](#equivalence)
* [Counting extensions](#counting-extensions)
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
- `Fine := false`: When true, creates the fine ramification polygon
- `Res := false`: When true, creates the fine ramification polygon with residues (implies Fine)
- `URes := false`: When true, assigns the uniformizer residue

<a id="RamificationPolygon-2"></a><a id="RamificationPolygon--FldPadTmpl--etc"></a><a id="RamificationPolygon--FldPadTmpl--any"></a>
> **RamificationPolygon** (F :: *FldPadTmpl*, X)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

A ramification polygon over `F`, defined by `X`, which must be one of:
- A sequence or list of points (defined below)
- A Newton polygon

A point is a tuple `<j,R_j,ord,res>` where:
- `j` and `R_j` have the meaning defined at the top of this section
- `ord` (optional) when given it must be one of:
  - `"eq"` meaning the point is present
  - `"gt"` meaning the point is not present
  - `"ge"` meaning the point may or may not be present
  At vertices, it is assumed to be `"eq"`, and otherwise `"ge"`.
- `res` (optional) when given is the residue to attach to the point. If it is zero, then `ord` must be consistent with `"gt"` and otherwise it must be consistent with `"eq"`.


**Parameters**
- `Fine := false`: When true, creates a fine ramification polygon. In particular, `ord` is assumed to be `"gt"` for any points not specified, whereas the default behaviour is to assume `"ge"`.

<a id="IsCoercibleToRamificationPolygon"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--etc"></a><a id="IsCoercibleToRamificationPolygon--FldPadTmpl--any"></a>
> **IsCoercibleToRamificationPolygon** (F :: *FldPadTmpl*, X)
> 
> -> *BoolElt*, Any
> {:.ret}
{:.intrinsic}

True if `X` is coercible to a ramification polygon.

The inputs and parameters are as in `RamificationPolygon` above.



## Validity
{:#validity}

<a id="IsValid"></a><a id="IsValid--PadRamifPgon"></a>
> **IsValid** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` is valid. That is, if there exists an Eisenstein polynomial with this ramification polygon.


<a id="IsWeaklyValid"></a><a id="IsWeaklyValid--PadRamifPgon"></a>
> **IsWeaklyValid** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` is weakly valid. This is weaker than validity, but is preserved under removing points from `P`. Useful for enumerating all valid polygons.


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


## Equivalence
{:#equivalence}


We say two ramification polygons are *equivalent* if the corresponding set of Eisenstein polynomials generates the same set of extensions (up to isomorphism).

Without any residual information, ramification polygons are already an invariant, and therefore are equivalent if and only if they are equal.

If there is residual information, then two polygons `P1` and `P2` are equivalent if they have residual information at the same points, and if there is a unit `u` such that `rho1_j = rho2_j u^R_j` for all `(j,R_j,rho1_j)` in `P1` and `(j,R_j,rho2_j)` in `P2`, and `rho1_0 = rho2_0 u^n` where `rho*_0` are the uniformizer residues.

<a id="IsEquivalent"></a><a id="IsEquivalent--PadRamifPgon--etc"></a><a id="IsEquivalent--PadRamifPgon--PadRamifPgon"></a>
> **IsEquivalent** (P1 :: *PadRamifPgon*, P2 :: *PadRamifPgon*)
> 
> -> *BoolElt*, Any
> {:.ret}
{:.intrinsic}

True iff `P1` and `P2` are equivalent, that is, their corresponding Eisenstein polynomials generate the same extensions. If true, also returns `<k,y>` such that any solution to `x^k=y` conjugates one to the other. If false, also returns a reason.


<a id="EquivalenceClass"></a><a id="EquivalenceClass--PadRamifPgon"></a>
> **EquivalenceClass** (P :: *PadRamifPgon*)
> 
> -> {}
> {:.ret}
{:.intrinsic}

The elements of the equivalence class of `P`.


<a id="EquivalenceClassSize"></a><a id="EquivalenceClassSize--PadRamifPgon"></a>
> **EquivalenceClassSize** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The size of the equivalence class of `P`.


## Counting extensions
{:#counting-extensions}


From Lemma 4.4 of Sinclair, "Counting extensions of p-adic fields with given invariants", we can count the number of extensions (inside an algebraic closure) with the given invariant based on the size of a template for the invariant. Note that this is different to counting the number of isomorphism classes: if an extension `L/K` has no automorphisms, then it has `(L:K)` conjugates in the algebraic closure, which are counted as distinct even though they are isomorphic.

<a id="NumberOfExtensions"></a><a id="NumberOfExtensions--PadRamifPgon"></a>
> **NumberOfExtensions** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The number of extensions (inside an algebraic closure) with this invariant.


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
- `URes := false`: When true, produce polygons with uniformizer residues. Equivalent to calling `WithAllUniformizerResidues` on the outputs.
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
- `Classes := false`: When true, returns one per equivalence class

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


