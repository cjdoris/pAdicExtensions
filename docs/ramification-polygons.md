# Ramification polygons
{:#ramification-polygons}


A `PadRamifPts` represents a set of points defining a ramification polygon. Some of the points need not be vertices, but can line on the interior of faces, and therefore this is a more refined invariant than ramification polygon.


**Contents**
* [Creation](#creation)
* [Invariants](#invariants)
* [Valuations of binomials](#valuations-of-binomials)
* [Validity](#validity)
* [Enumeration](#enumeration)

## Creation
{:#creation}

<a id="IsCoercible_RamificationPoints--FldPadTmpl--etc"></a><a id="IsCoercible_RamificationPoints"></a><a id="IsCoercible_RamificationPoints--FldPadTmpl--seq"></a>
> **IsCoercible_RamificationPoints** (F :: *FldPadTmpl*, vs :: [])
> 
> -> *BoolElt*, *PadRamifPts*
> {:.ret}
{:.intrinsic}

True if `vs` can be made into a potential set of ramification points over `F`. `vs` must be a list of `<x,y>` pairs of integers defining the points.


<a id="RamificationPoints"></a><a id="RamificationPoints--FldPadTmpl--etc"></a><a id="RamificationPoints--FldPadTmpl--seq"></a>
> **RamificationPoints** (F :: *FldPadTmpl*, vs :: [])
> 
> -> *PadRamifPts*
> {:.ret}
{:.intrinsic}

A potential set of ramification points over `F`.


<a id="Copy"></a><a id="Copy--PadRamifPts"></a>
> **Copy** (P :: *PadRamifPts*)
> 
> -> *PadRamifPts*
> {:.ret}
{:.intrinsic}

Makes a copy of `P`.


## Invariants
{:#invariants}

<a id="e"></a><a id="su--PadRamifPts"></a><a id="u"></a><a id="p"></a><a id="su"></a><a id="n--PadRamifPts"></a><a id="xu--PadRamifPts"></a><a id="n"></a><a id="p--PadRamifPts"></a><a id="e--PadRamifPts"></a><a id="xu"></a><a id="u--PadRamifPts"></a>
> **n** (P :: *PadRamifPts*)
> 
> **p** (P :: *PadRamifPts*)
> 
> **e** (P :: *PadRamifPts*)
> 
> **u** (P :: *PadRamifPts*)
> 
> **su** (P :: *PadRamifPts*)
> 
> **xu** (P :: *PadRamifPts*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

n (degree), p (prime), e (absolute ramification degree), u (number of wild faces), x_u=p^s_u (wild degree)












<a id="J--PadRamifPts--etc"></a><a id="a"></a><a id="b--PadRamifPts--RngIntElt"></a><a id="b--PadRamifPts--etc"></a><a id="b"></a><a id="s"></a><a id="x--PadRamifPts--RngIntElt"></a><a id="J--PadRamifPts--RngIntElt"></a><a id="x--PadRamifPts--etc"></a><a id="x"></a><a id="a--PadRamifPts--etc"></a><a id="a--PadRamifPts--RngIntElt"></a><a id="s--PadRamifPts--etc"></a><a id="J"></a><a id="s--PadRamifPts--RngIntElt"></a>
> **J** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> **a** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> **b** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> **s** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> **x** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

J_i = n a_i + b_i (heights of vertices), x_i = p^s_i (abscissas)










## Valuations of binomials
{:#valuations-of-binomials}

<a id="vbin--PadRamifPts--etc"></a><a id="vbin"></a><a id="vbin--PadRamifPts--RngIntElt--RngIntElt"></a>
> **vbin** (P :: *PadRamifPts*, n :: *RngIntElt*, k :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `n` choose `k`.


<a id="vbinp--PadRamifPts--RngIntElt--RngIntElt"></a><a id="vbinp"></a><a id="vbinp--PadRamifPts--etc"></a>
> **vbinp** (P :: *PadRamifPts*, n :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `n` choose `p^i`.


<a id="vbinbp--PadRamifPts--etc"></a><a id="vbinbp--PadRamifPts--RngIntElt--RngIntElt"></a><a id="vbinbp"></a>
> **vbinbp** (P :: *PadRamifPts*, j :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `b_j` choose `p^i`.


<a id="vbinps--PadRamifPts--etc"></a><a id="vbinps"></a><a id="vbinps--PadRamifPts--RngIntElt--RngIntElt"></a>
> **vbinps** (P :: *PadRamifPts*, n :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `n` choose `p^s_i`.


<a id="vbinnps"></a><a id="vbinnps--PadRamifPts--RngIntElt"></a><a id="vbinnps--PadRamifPts--etc"></a>
> **vbinnps** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `n` choose p^s_i.


<a id="vbinbps--PadRamifPts--etc"></a><a id="vbinbps"></a><a id="vbinbps--PadRamifPts--RngIntElt--RngIntElt"></a>
> **vbinbps** (P :: *PadRamifPts*, j :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `b_j` choose `p^s_i`.


<a id="vbinbps--PadRamifPts--etc-2"></a><a id="vbinbps-2"></a><a id="vbinbps--PadRamifPts--RngIntElt"></a>
> **vbinbps** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `b_i choose p^s_i`.


## Validity
{:#validity}

<a id="_SatisfiesOreCondition"></a><a id="SatisfiesOreCondition"></a><a id="_SatisfiesOreCondition--PadRamifPts"></a><a id="SatisfiesOreCondition--PadRamifPts"></a>
> **_SatisfiesOreCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any
> {:.ret}
> 
> **SatisfiesOreCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies the Ore conditions: `b_t=0 => a_t eq vB(n,p^s_t)`, `b_t>0 => B(b_t,p^s_t) le a_t le B(n,p^s_t)-1`.




<a id="_SatisfiesTameCondition"></a><a id="SatisfiesTameCondition"></a><a id="_SatisfiesTameCondition--PadRamifPts"></a><a id="SatisfiesTameCondition--PadRamifPts"></a>
> **_SatisfiesTameCondition** (P :: *PadRamifPts*)
> 
> **SatisfiesTameCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies the tame conditions: `p^s_u le j le n => (j,0) in P iff B(n,j)=0`.




<a id="CorrectTamePoints--PadRamifPts"></a><a id="CorrectTamePoints"></a>
> **CorrectTamePoints** (P :: *PadRamifPts*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The correct tame points for a valid `P` of this degree.


<a id="WithCorrectTamePoints--PadRamifPts"></a><a id="WithCorrectTamePoints"></a>
> **WithCorrectTamePoints** (P :: *PadRamifPts*)
> 
> -> *PadRamifPts*
> {:.ret}
{:.intrinsic}

A copy of `P` with the correct tame points.


<a id="_SatisfiesCongruenceCondition"></a><a id="_SatisfiesCongruenceCondition--PadRamifPts"></a><a id="SatisfiesCongruenceCondition"></a><a id="SatisfiesCongruenceCondition--PadRamifPts"></a>
> **_SatisfiesCongruenceCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any, Any
> {:.ret}
> 
> **SatisfiesCongruenceCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the congruence conditions: `b_t = b_r => a_t - B(b_t,p^s_t) = a_r - B(b_r,p^s_r)`.




<a id="_SatisfiesBoundingCondition"></a><a id="SatisfiesBoundingCondition--PadRamifPts"></a><a id="SatisfiesBoundingCondition"></a><a id="_SatisfiesBoundingCondition--PadRamifPts"></a>
> **_SatisfiesBoundingCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any, Any
> {:.ret}
> 
> **SatisfiesBoundingCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the bounding conditions: `b_r eq 0, p^s_r le b_t => a_t ge B(n,p^s_r) - B(b_t,p^s_r) + B(b_t,p^s_t)` and `b_r ne 0, p^s_r le b_t => a_t ge a_r - B(b_t,p^s_r) + B(b_t,p^s_t) + 1[b_t lt b_r]`.




<a id="SatisfiesMissingCondition--PadRamifPts"></a><a id="_SatisfiesMissingCondition--PadRamifPts"></a><a id="SatisfiesMissingCondition"></a><a id="_SatisfiesMissingCondition"></a>
> **_SatisfiesMissingCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any, Any
> {:.ret}
> 
> **SatisfiesMissingCondition** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the "missing" conditions: `s_t lt s lt s_(t+1) => Floor(X/n) le B(n,p^s) - 1` and `s_t lt s_(t+1), p^s le b_r => a_r ge Floor((X-b_r)/n) + B(b_r,p^s_r) - B(b_r,p^s) + 1` where `X = J_t + (J_(t+1)-J_t)*(x_(t+1)-x_t)/(p^s-x_t)`.




<a id="_IsSemivalid--PadRamifPts"></a><a id="_IsSemivalid"></a>
> **_IsSemivalid** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the Ore, congruence and bounding conditions, which are necessary (but not sufficient) for being valid.


<a id="IsSemivalid--PadRamifPts"></a><a id="IsSemivalid"></a>
> **IsSemivalid** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` satisfies the Ore, congruence and bounding conditions, which are necessary (but not sufficient) for being valid.


<a id="_IsValid--PadRamifPts"></a><a id="_IsValid"></a>
> **_IsValid** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` corresponds to an actual extension.


<a id="IsValid"></a><a id="IsValid--PadRamifPts"></a>
> **IsValid** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if `P` corresponds to an actual extension.


## Enumeration
{:#enumeration}

<a id="AllRamificationPoints"></a><a id="AllRamificationPoints--FldPadTmpl--etc"></a><a id="AllRamificationPoints--FldPadTmpl--RngIntElt"></a>
> **AllRamificationPoints** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}

All possible ramification points of extensions of `F` of degree `n`.

**Parameters**
- `J0 := false`: When given, just produce the points with discriminant valuation `J0+n-1`

