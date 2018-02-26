# Ramification polygons
{:#ramification-polygons}


A `PadRamifPgon` represents a set of points defining a ramification polygon, which is the Newton polygon of the *ramification polygon* `r(x) = f(pi x + pi) / pi^n` of the Eisenstein polynomial `f(x)` of degree `n`. Some of the points need not be vertices, but can lie on the interior of faces, and therefore this is a more refined invariant than just the polygon itself. The points must be of the form `[<1, J_0>, <p^s_1, J_1>, ..., <p^s_u, 0>, ..., <n, 0>]` where `s_u = v_p(n)`.

To each point, we can also assign a non-zero element of the residue class field, which is the leading p-adic coefficients of the corresponding ramification polygon. These are collectively called the *residues* of the ramification polygon. If we multiply the uniformizer of the corresponding extension by the residue `u`, then the residues are all multplied by `u^n`. This defines an equivalence relation between different sets of residues.

Additionally, we can assign a single non-zero element of the residue class field, which we call the *constant coefficient residue*, abbreviated to *CC-residue*, which is the leading p-adic coefficient of the constant coefficient of the corresponding Eisenstein polynomial `f`.


**Contents**
* [Creation](#creation)
* [Invariants](#invariants)
* [Valuations of binomials](#valuations-of-binomials)
* [Validity](#validity)
* [Residues](#residues)
* [Enumeration](#enumeration)

## Creation
{:#creation}

<a id="IsCoercible_RamificationPolygon"></a><a id="IsCoercible_RamificationPolygon--FldPadTmpl--etc"></a><a id="IsCoercible_RamificationPolygon--FldPadTmpl--seq"></a>
> **IsCoercible_RamificationPolygon** (F :: *FldPadTmpl*, vs :: [])
> 
> -> *BoolElt*, *PadRamifPgon*
> {:.ret}
{:.intrinsic}

True if `vs` can be made into a ramification polygon over `F`. `vs` must be a list of `<x,y>` pairs of integers defining the points.


<a id="RamificationPolygon"></a><a id="RamificationPolygon--FldPadTmpl--etc"></a><a id="RamificationPolygon--FldPadTmpl--seq"></a>
> **RamificationPolygon** (F :: *FldPadTmpl*, vs :: [])
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

A ramification polygon over `F`.


<a id="Copy"></a><a id="Copy--PadRamifPgon"></a>
> **Copy** (P :: *PadRamifPgon*)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

Makes a copy of `P`.


## Invariants
{:#invariants}

<a id="n"></a><a id="n--PadRamifPgon"></a><a id="p"></a><a id="p--PadRamifPgon"></a><a id="e"></a><a id="e--PadRamifPgon"></a><a id="u"></a><a id="u--PadRamifPgon"></a><a id="su"></a><a id="su--PadRamifPgon"></a><a id="xu"></a><a id="xu--PadRamifPgon"></a>
> **n** (P :: *PadRamifPgon*)
> 
> **p** (P :: *PadRamifPgon*)
> 
> **e** (P :: *PadRamifPgon*)
> 
> **u** (P :: *PadRamifPgon*)
> 
> **su** (P :: *PadRamifPgon*)
> 
> **xu** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

n (degree), p (prime), e (absolute ramification degree), u (number of wild faces), x_u=p^s_u (wild degree)












<a id="J"></a><a id="J--PadRamifPgon--etc"></a><a id="J--PadRamifPgon--RngIntElt"></a><a id="a"></a><a id="a--PadRamifPgon--etc"></a><a id="a--PadRamifPgon--RngIntElt"></a><a id="b"></a><a id="b--PadRamifPgon--etc"></a><a id="b--PadRamifPgon--RngIntElt"></a><a id="s"></a><a id="s--PadRamifPgon--etc"></a><a id="s--PadRamifPgon--RngIntElt"></a><a id="x"></a><a id="x--PadRamifPgon--etc"></a><a id="x--PadRamifPgon--RngIntElt"></a>
> **J** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> **a** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> **b** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> **s** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> **x** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

J_i = n a_i + b_i (heights of vertices), x_i = p^s_i (abscissas)










## Valuations of binomials
{:#valuations-of-binomials}

<a id="vbin"></a><a id="vbin--PadRamifPgon--etc"></a><a id="vbin--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **vbin** (P :: *PadRamifPgon*, n :: *RngIntElt*, k :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `n` choose `k`.


<a id="vbinp"></a><a id="vbinp--PadRamifPgon--etc"></a><a id="vbinp--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **vbinp** (P :: *PadRamifPgon*, n :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `n` choose `p^i`.


<a id="vbinbp"></a><a id="vbinbp--PadRamifPgon--etc"></a><a id="vbinbp--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **vbinbp** (P :: *PadRamifPgon*, j :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `b_j` choose `p^i`.


<a id="vbinps"></a><a id="vbinps--PadRamifPgon--etc"></a><a id="vbinps--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **vbinps** (P :: *PadRamifPgon*, n :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `n` choose `p^s_i`.


<a id="vbinnps"></a><a id="vbinnps--PadRamifPgon--etc"></a><a id="vbinnps--PadRamifPgon--RngIntElt"></a>
> **vbinnps** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `n` choose p^s_i.


<a id="vbinbps"></a><a id="vbinbps--PadRamifPgon--etc"></a><a id="vbinbps--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **vbinbps** (P :: *PadRamifPgon*, j :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `b_j` choose `p^s_i`.


<a id="vbinbps-2"></a><a id="vbinbps--PadRamifPgon--etc-2"></a><a id="vbinbps--PadRamifPgon--RngIntElt"></a>
> **vbinbps** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `b_i choose p^s_i`.


<a id="sbinres"></a><a id="sbinres--PadRamifPgon--etc"></a><a id="sbinres--PadRamifPgon--RngIntElt--RngIntElt"></a>
> **sbinres** (P :: *PadRamifPgon*, n :: *RngIntElt*, k :: *RngIntElt*)
> 
> -> *FldFinElt*
> {:.ret}
{:.intrinsic}

The residue class of `n` choose `k` shifted down to a unit.


## Validity
{:#validity}


Some polygons correspond to ramification polygons of actual extensions, and some do not. The ones which do we refer to as *valid*, and there are 5 conditions (which we call "Ore", "Tame", "Congruence", "Bounding" and "Missing") which together are necessary and sufficient for validity.

A polygon which satisfies the Ore, Congruence and Bounding conditions is called *semivalid*, and so semivalidity is necessary for validity. A polygon which is semivalid remains semivalid if we remove some of its points, and so this is useful when enumerating all possibilities by introducing one point at a time.

We provide intrinsics to check for validity, semivalidity, and the 5 individual conditions. Each intrinsic also has a version with a leading underscore; this version does not cache its answer, but does provide more information in the case of failure.

<a id="IsValid"></a><a id="IsValid--PadRamifPgon"></a>
> **IsValid** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` corresponds to an actual extension.

**Parameters**
- `Residues := true`: Only checks the residues (if they are assigned) when this is true

<a id="IsSemivalid"></a><a id="IsSemivalid--PadRamifPgon"></a>
> **IsSemivalid** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the Ore, congruence and bounding conditions, which are necessary (but not sufficient) for being valid.


<a id="SatisfiesOreCondition"></a><a id="SatisfiesOreCondition--PadRamifPgon"></a>
> **SatisfiesOreCondition** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies the Ore conditions: `b_t=0 => a_t eq vB(n,p^s_t)`, `b_t>0 => B(b_t,p^s_t) le a_t le B(n,p^s_t)-1`.


<a id="SatisfiesTameCondition"></a><a id="SatisfiesTameCondition--PadRamifPgon"></a>
> **SatisfiesTameCondition** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies the tame conditions: `p^s_u le j le n => (j,0) in P iff B(n,j)=0`.


<a id="CorrectTamePoints"></a><a id="CorrectTamePoints--PadRamifPgon"></a>
> **CorrectTamePoints** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The correct tame points for a valid `P` of this degree.


<a id="WithCorrectTamePoints"></a><a id="WithCorrectTamePoints--PadRamifPgon"></a>
> **WithCorrectTamePoints** (P :: *PadRamifPgon*)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

A copy of `P` with the correct tame points.


<a id="SatisfiesCongruenceCondition"></a><a id="SatisfiesCongruenceCondition--PadRamifPgon"></a>
> **SatisfiesCongruenceCondition** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the congruence conditions: `b_t = b_r => a_t - B(b_t,p^s_t) = a_r - B(b_r,p^s_r)`.


<a id="SatisfiesBoundingCondition"></a><a id="SatisfiesBoundingCondition--PadRamifPgon"></a>
> **SatisfiesBoundingCondition** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the bounding conditions: `b_r eq 0, p^s_r le b_t => a_t ge B(n,p^s_r) - B(b_t,p^s_r) + B(b_t,p^s_t)` and `b_r ne 0, p^s_r le b_t => a_t ge a_r - B(b_t,p^s_r) + B(b_t,p^s_t) + 1[b_t lt b_r]`.


<a id="SatisfiesMissingCondition"></a><a id="SatisfiesMissingCondition--PadRamifPgon"></a>
> **SatisfiesMissingCondition** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the "missing" conditions: `s_t lt s lt s_(t+1) => Floor(X/n) le B(n,p^s) - 1` and `s_t lt s_(t+1), p^s le b_r => a_r ge Floor((X-b_r)/n) + B(b_r,p^s_r) - B(b_r,p^s) + 1` where `X = J_t + (J_(t+1)-J_t)*(x_(t+1)-x_t)/(p^s-x_t)`.


## Residues
{:#residues}

<a id="IsValidResidues"></a><a id="IsValidResidues--PadRamifPgon--etc"></a><a id="IsValidResidues--PadRamifPgon--seq-FldFinElt"></a>
> **IsValidResidues** (P :: *PadRamifPgon*, rs :: [*FldFinElt*])
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `rs` is a valid assignment of residues to `P`, i.e. if there exists an Eisenstein polynomial with these residues. When true, also returns a polynomial whose roots are the possible leading p-adic coefficients of the constant coefficient.

**Parameters**
- `Partial := false`: When true, rs may be a partial assignment (i.e. have some undefined entries) and the check becomes necessary but not sufficient for exisence.

<a id="CorrectTameResidues"></a><a id="CorrectTameResidues--PadRamifPgon"></a>
> **CorrectTameResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The correct tame residues of `P`, between `x_u` and `n`.


## Enumeration
{:#enumeration}

<a id="AllRamificationPolygons"></a><a id="AllRamificationPolygons--FldPadTmpl--etc"></a><a id="AllRamificationPolygons--FldPadTmpl--RngIntElt"></a>
> **AllRamificationPolygons** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All possible ramification polygons of extensions of `F` of degree `n`.

**Parameters**
- `J0 := false`: When given, just produce the polygons with discriminant valuation `J0+n-1`.
- `WithResidues := false`: When true, also enumerates over all possible residues (equivalent to calling `WithAllResidues` on each output).
- `WithCCResidues := false`: When true, also enumerates over all possible CC-residues (implies `WithResidues`; equivalent to calling `WithCCResidues` on each output).
- `Classes := false`: When true, limits the residues and CC-residues to representatives of equivalence classes (so that they still generate all extensions among them).

<a id="AllValidResidues"></a><a id="AllValidResidues--PadRamifPgon"></a>
> **AllValidResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All the residues which are valid for `P`, paired with the leading coefficient polynomial.

**Parameters**
- `Classes := false`: When true, only return one per equivalence class.

<a id="WithAllResidues"></a><a id="WithAllResidues--PadRamifPgon"></a>
> **WithAllResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

Copies of `P` with valid residues attached.

**Parameters**
- `Classes := false`: When true, only return one per equivalence class.

<a id="AllCCResidues"></a><a id="AllCCResidues--PadRamifPgon"></a>
> **AllCCResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All valid CC-residues for `P`.

**Parameters**
- `Residues`: When given, use these residues instead of the ones attached to P.
- `Classes := false`: When true, only return one per equivalence class.

<a id="WithAllCCResidues"></a><a id="WithAllCCResidues--PadRamifPgon"></a>
> **WithAllCCResidues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

Copies of `P` with valid CC-residues attached.

**Parameters**
- `Classes := false`: When true, only return one per equivalence class.

