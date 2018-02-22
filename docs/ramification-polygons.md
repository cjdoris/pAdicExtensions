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

<a id="IsCoercible_RamificationPoints"></a><a id="IsCoercible_RamificationPoints--FldPadTmpl--etc"></a><a id="IsCoercible_RamificationPoints--FldPadTmpl--seq"></a>
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

<a id="u"></a><a id="p--PadRamifPts"></a><a id="e--PadRamifPts"></a><a id="su--PadRamifPts"></a><a id="n--PadRamifPts"></a><a id="u--PadRamifPts"></a><a id="p"></a><a id="n"></a><a id="su"></a><a id="e"></a>
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
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

n (degree), p (prime), e (absolute ramification degree), u (number of wild faces), s_u (p^s_u is the wild degree)










<a id="J--PadRamifPts--RngIntElt"></a><a id="J--PadRamifPts--etc"></a><a id="x--PadRamifPts--etc"></a><a id="J"></a><a id="s--PadRamifPts--RngIntElt"></a><a id="a--PadRamifPts--RngIntElt"></a><a id="s--PadRamifPts--etc"></a><a id="b--PadRamifPts--etc"></a><a id="s"></a><a id="x"></a><a id="a"></a><a id="x--PadRamifPts--RngIntElt"></a><a id="b"></a><a id="a--PadRamifPts--etc"></a><a id="b--PadRamifPts--RngIntElt"></a>
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

<a id="vbin"></a><a id="vbin--PadRamifPts--etc"></a><a id="vbin--PadRamifPts--RngIntElt--RngIntElt"></a>
> **vbin** (P :: *PadRamifPts*, n :: *RngIntElt*, k :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `n` choose `k`.


<a id="vbinp"></a><a id="vbinp--PadRamifPts--etc"></a><a id="vbinp--PadRamifPts--RngIntElt--RngIntElt"></a>
> **vbinp** (P :: *PadRamifPts*, n :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of `n` choose p^`i`.


<a id="vbinbp--PadRamifPts--etc"></a><a id="vbinbp"></a><a id="vbinbp--PadRamifPts--RngIntElt--RngIntElt"></a>
> **vbinbp** (P :: *PadRamifPts*, j :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Valuation of b_j choose p^`i`.


<a id="vbinps--PadRamifPts--etc"></a><a id="vbinps--PadRamifPts--RngIntElt--RngIntElt"></a><a id="vbinps"></a>
> **vbinps** (P :: *PadRamifPts*, n :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of `n` choose p^s_i.


<a id="vbinnps--PadRamifPts--etc"></a><a id="vbinnps--PadRamifPts--RngIntElt"></a><a id="vbinnps"></a>
> **vbinnps** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of n choose p^s_i.


<a id="vbinbps--PadRamifPts--etc"></a><a id="vbinbps--PadRamifPts--RngIntElt--RngIntElt"></a><a id="vbinbps"></a>
> **vbinbps** (P :: *PadRamifPts*, j :: *RngIntElt*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of b_j choose p^s_i.


<a id="vbinbps--PadRamifPts--RngIntElt"></a><a id="vbinbps--PadRamifPts--etc-2"></a><a id="vbinbps-2"></a>
> **vbinbps** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The valuation of b_i choose p^s_i.


## Validity
{:#validity}


Proposition 3.9 tells us if a given set of points is the ramification polygon for some extension, and if so we say it is *valid*. If the set of points satisfies cases (a), (b) and (c) of the proposition, we say it is *semivalid*; a semivalid set of points remains semivalid if we remove points (except for the critical points at 1, p^s_u and n) and so in particular if a set of points is not semivalid, then adding points to it cannot make it valid. This fact may be used to efficiently enumerate all possible ramification points of a given degree.

<a id="SatisfiesPropertyA--PadRamifPts"></a><a id="SatisfiesPropertyA"></a><a id="_SatisfiesPropertyA"></a><a id="_SatisfiesPropertyA--PadRamifPts"></a>
> **_SatisfiesPropertyA** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any
> {:.ret}
> 
> **SatisfiesPropertyA** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies case (a) of Proposition 3.9.




<a id="_SatisfiesPropertyB--PadRamifPts"></a><a id="SatisfiesPropertyB--PadRamifPts"></a><a id="_SatisfiesPropertyB"></a><a id="SatisfiesPropertyB"></a>
> **_SatisfiesPropertyB** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any, Any
> {:.ret}
> 
> **SatisfiesPropertyB** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies case (b) of Proposition 3.9.




<a id="_SatisfiesPropertyC"></a><a id="_SatisfiesPropertyC--PadRamifPts"></a><a id="SatisfiesPropertyC"></a><a id="SatisfiesPropertyC--PadRamifPts"></a>
> **_SatisfiesPropertyC** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any, Any
> {:.ret}
> 
> **SatisfiesPropertyC** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies case (c) of Proposition 3.9.




<a id="SatisfiesPropertyD"></a><a id="SatisfiesPropertyD--PadRamifPts"></a><a id="_SatisfiesPropertyD"></a><a id="_SatisfiesPropertyD--PadRamifPts"></a>
> **_SatisfiesPropertyD** (P :: *PadRamifPts*)
> 
> -> *BoolElt*, Any, Any, Any
> {:.ret}
> 
> **SatisfiesPropertyD** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies property (d) of Proposition 3.9.




<a id="_LittleEll"></a><a id="LittleEll--PadRamifPts--RngIntElt--RngIntElt"></a><a id="_LittleEll--PadRamifPts--etc"></a><a id="LittleEll"></a><a id="_LittleEll--PadRamifPts--RngIntElt--RngIntElt"></a><a id="LittleEll--PadRamifPts--etc"></a>
> **_LittleEll** (P :: *PadRamifPts*, i :: *RngIntElt*, S :: *RngIntElt*)
> 
> **LittleEll** (P :: *PadRamifPts*, i :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The "little ell" bound of Definition 3.8.




<a id="BigEll--PadRamifPts--RngIntElt"></a><a id="_BigEll--PadRamifPts--etc"></a><a id="BigEll--PadRamifPts--etc"></a><a id="_BigEll--PadRamifPts--RngIntElt"></a><a id="_BigEll"></a><a id="BigEll"></a>
> **_BigEll** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> **BigEll** (P :: *PadRamifPts*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The "big ell" bound of Definition 3.8.



**Parameters**
- `Cache`

<a id="_SatisfiesPropertyE"></a><a id="_SatisfiesPropertyE--PadRamifPts"></a><a id="SatisfiesPropertyE"></a><a id="SatisfiesPropertyE--PadRamifPts"></a>
> **_SatisfiesPropertyE** (P :: *PadRamifPts*)
> 
> **SatisfiesPropertyE** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies property (e) of Proposition 3.9.




<a id="FixPropertyE--PadRamifPts"></a><a id="FixPropertyE"></a>
> **FixPropertyE** (P :: *PadRamifPts*)
> 
> -> *PadRamifPts*
> {:.ret}
{:.intrinsic}

A copy of `P` with the tame part corrected to satisfy case (e) of Proposition 3.9.


<a id="IsSemivalid--PadRamifPts"></a><a id="_IsSemivalid"></a><a id="_IsSemivalid--PadRamifPts"></a><a id="IsSemivalid"></a>
> **_IsSemivalid** (P :: *PadRamifPts*)
> 
> **IsSemivalid** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies properties (a)--(c) of Proposition 3.9.




<a id="_IsValid--PadRamifPts"></a><a id="IsValid"></a><a id="_IsValid"></a><a id="IsValid--PadRamifPts"></a>
> **_IsValid** (P :: *PadRamifPts*)
> 
> **IsValid** (P :: *PadRamifPts*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True iff `P` satisfies Proposition 3.9.




## Enumeration
{:#enumeration}

<a id="AllRamificationPoints--FldPadTmpl--RngIntElt"></a><a id="AllRamificationPoints--FldPadTmpl--etc"></a><a id="AllRamificationPoints"></a>
> **AllRamificationPoints** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}

**Parameters**
- `J0 := false`: When given, just produce the points with discriminant valuation J0+n-1

