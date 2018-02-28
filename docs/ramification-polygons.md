# Ramification polygons
{:#ramification-polygons}


A `PadRamifPgon` represents a set of points defining a ramification polygon, which is the Newton polygon of the *ramification polygon* `r(x) = f(pi x + pi) / pi^n` of the Eisenstein polynomial `f(x)` of degree `n`. Some of the points need not be vertices, but can lie on the interior of faces, and therefore this is a more refined invariant than just the polygon itself. The points must be of the form `[<1, J_0>, <p^s_1, J_1>, ..., <p^s_u, 0>, ..., <n, 0>]` where `s_u = v_p(n)`.

To each point, we can also assign a non-zero element of the residue class field, which is the leading p-adic coefficients of the corresponding ramification polygon. These are collectively called the *residues* of the ramification polygon. If we multiply the uniformizer of the corresponding extension by the residue `u`, then the residues are all multplied by `u^n`. This defines an equivalence relation between different sets of residues.

Additionally, we can assign a single non-zero element of the residue class field, which we call the *constant coefficient residue*, abbreviated to *CC-residue*, which is the leading p-adic coefficient of the constant coefficient of the corresponding Eisenstein polynomial `f`.


**Contents**
* [Creation](#creation)
* [Basic properties](#basic-properties)
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


<a id="RamificationPolygon-2"></a><a id="RamificationPolygon--RngUPolElt_FldPadTmpl"></a>
> **RamificationPolygon** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

The ramification polygon of `f`, which must be Eisenstein.


<a id="Copy"></a><a id="Copy--PadRamifPgon"></a>
> **Copy** (P :: *PadRamifPgon*)
> 
> -> *PadRamifPgon*
> {:.ret}
{:.intrinsic}

Makes a copy of `P`.


## Basic properties
{:#basic-properties}

<a id="Degree"></a><a id="Degree--PadRamifPgon"></a>
> **Degree** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The degree of `P`.


<a id="WildDegree"></a><a id="WildDegree--PadRamifPgon"></a>
> **WildDegree** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The wild degree of `P`.


<a id="BaseField"></a><a id="BaseField--PadRamifPgon"></a>
> **BaseField** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The base field of `P`.


<a id="NumberOfPoints"></a><a id="NumberOfPoints--PadRamifPgon"></a>
> **NumberOfPoints** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The number of points on `P`.


<a id="NumberOfWildPoints"></a><a id="NumberOfWildPoints--PadRamifPgon"></a>
> **NumberOfWildPoints** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The number of wild points on `P`.


<a id="Point"></a><a id="Point--PadRamifPgon--etc"></a><a id="Point--PadRamifPgon--RngIntElt"></a>
> **Point** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *Tup*
> {:.ret}
{:.intrinsic}

The `i`th point on `P`.


<a id="Points"></a><a id="Points--PadRamifPgon"></a>
> **Points** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The points on `P`.


<a id="WildPoints"></a><a id="WildPoints--PadRamifPgon"></a>
> **WildPoints** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The wild points of `P`.


<a id="TamePoints"></a><a id="TamePoints--PadRamifPgon"></a>
> **TamePoints** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The tame points of `P`.


<a id="Polygon"></a><a id="Polygon--PadRamifPgon"></a>
> **Polygon** (P :: *PadRamifPgon*)
> 
> -> *NwtnPgon*
> {:.ret}
{:.intrinsic}

The polygon of `P`.


<a id="Vertex"></a><a id="Vertex--PadRamifPgon--etc"></a><a id="Vertex--PadRamifPgon--RngIntElt"></a>
> **Vertex** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *Tup*
> {:.ret}
{:.intrinsic}

The `i`th vertex of `P`.


<a id="Vertices"></a><a id="Vertices--PadRamifPgon"></a>
> **Vertices** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The vertices of `P`.


<a id="WildVertices"></a><a id="WildVertices--PadRamifPgon"></a>
> **WildVertices** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The wild vertices of `P`.


<a id="NumberOfFaces"></a><a id="NumberOfFaces--PadRamifPgon"></a>
> **NumberOfFaces** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The number of faces of `P`.


<a id="NumberOfWildFaces"></a><a id="NumberOfWildFaces--PadRamifPgon"></a>
> **NumberOfWildFaces** (P :: *PadRamifPgon*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The number of wild faces of `P`.


<a id="Face"></a><a id="Face--PadRamifPgon--etc"></a><a id="Face--PadRamifPgon--RngIntElt"></a>
> **Face** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *NwtnPgonFace*
> {:.ret}
{:.intrinsic}

The `i`th face of `P`.


<a id="Faces"></a><a id="Faces--PadRamifPgon"></a>
> **Faces** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The faces of `P`.


<a id="WildFaces"></a><a id="WildFaces--PadRamifPgon"></a>
> **WildFaces** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The wild faces of `P`.


<a id="Slope"></a><a id="Slope--PadRamifPgon--etc"></a><a id="Slope--PadRamifPgon--RngIntElt"></a>
> **Slope** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *FldRatElt*
> {:.ret}
{:.intrinsic}

The slope of the `i`th face of `P`.


<a id="Slopes"></a><a id="Slopes--PadRamifPgon"></a>
> **Slopes** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The slopes of faces of `P`.


<a id="SlopeIsIntegral"></a><a id="SlopeIsIntegral--PadRamifPgon--etc"></a><a id="SlopeIsIntegral--PadRamifPgon--RngIntElt"></a>
> **SlopeIsIntegral** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *BoolElt*, *RngIntElt*
> {:.ret}
{:.intrinsic}

True if the slope of the `i`th face is integral.


<a id="Abscissa"></a><a id="Abscissa--PadRamifPgon--etc"></a><a id="Abscissa--PadRamifPgon--RngIntElt"></a>
> **Abscissa** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The abscissa of the `i`th point.


<a id="Abscissas"></a><a id="Abscissas--PadRamifPgon"></a>
> **Abscissas** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The abscissas of points of `P`.


<a id="LogAbscissa"></a><a id="LogAbscissa--PadRamifPgon--etc"></a><a id="LogAbscissa--PadRamifPgon--RngIntElt"></a>
> **LogAbscissa** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The power s where the `i`th (wild) abscissa of `P` is `p^s`.


<a id="LogAbscissas"></a><a id="LogAbscissas--PadRamifPgon"></a>
> **LogAbscissas** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The log abscissas of `P`.


<a id="Ordinate"></a><a id="Ordinate--PadRamifPgon--etc"></a><a id="Ordinate--PadRamifPgon--RngIntElt"></a>
> **Ordinate** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The ordinate of the `i`th point.


<a id="Ordinates"></a><a id="Ordinates--PadRamifPgon"></a>
> **Ordinates** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The ordinates of points of `P`.


<a id="OrdinateModDegree"></a><a id="OrdinateModDegree--PadRamifPgon--etc"></a><a id="OrdinateModDegree--PadRamifPgon--RngIntElt"></a>
> **OrdinateModDegree** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The `i`th ordinate of `P` mod the degree of `P`.


<a id="OrdinatesModDegree"></a><a id="OrdinatesModDegree--PadRamifPgon"></a>
> **OrdinatesModDegree** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The ordinates of `P` mod the degree of `P`.


<a id="OrdinateDivDegree"></a><a id="OrdinateDivDegree--PadRamifPgon--etc"></a><a id="OrdinateDivDegree--PadRamifPgon--RngIntElt"></a>
> **OrdinateDivDegree** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The `i`th ordinate of `P` div the degree of `P`.


<a id="OrdinatesDivDegree"></a><a id="OrdinatesDivDegree--PadRamifPgon"></a>
> **OrdinatesDivDegree** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The ordinates of `P` mod the degree of `P`.


<a id="HasResidues"></a><a id="HasResidues--PadRamifPgon"></a>
> **HasResidues** (P :: *PadRamifPgon*)
> 
> -> *BoolElt*, []
> {:.ret}
{:.intrinsic}

True iff `P` has residues assigned. If so, also returns them.


<a id="Residue"></a><a id="Residue--PadRamifPgon--etc"></a><a id="Residue--PadRamifPgon--RngIntElt"></a>
> **Residue** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *FldFinElt*
> {:.ret}
{:.intrinsic}

The residue of the `i`th point of `P`.


<a id="Residues"></a><a id="Residues--PadRamifPgon"></a>
> **Residues** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The residues of points of `P`.


<a id="ResidualPolynomial"></a><a id="ResidualPolynomial--PadRamifPgon--etc"></a><a id="ResidualPolynomial--PadRamifPgon--RngIntElt"></a>
> **ResidualPolynomial** (P :: *PadRamifPgon*, i :: *RngIntElt*)
> 
> -> *RngUPolElt*
> {:.ret}
{:.intrinsic}

The residual polynomial of the `i`th face of `P`.


<a id="ResidualPolynomials"></a><a id="ResidualPolynomials--PadRamifPgon"></a>
> **ResidualPolynomials** (P :: *PadRamifPgon*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The residual polynomials of each face of `P`.


<a id="SlopePolynomial"></a><a id="SlopePolynomial--PadRamifPgon--etc"></a><a id="SlopePolynomial--PadRamifPgon--RngIntElt"></a>
> **SlopePolynomial** (P :: *PadRamifPgon*, m :: *RngIntElt*)
> 
> -> *RngUPolElt*
> {:.ret}
{:.intrinsic}

Add a slope of `m` to `P` and form a polynomial from the residues of the lowest points. Is an additive polynomial for `m>0`. When `-m` is a slope, it is the corresponding residual polynomial, multiplied by some power of `x`; otherwise it is `x^(p^k)` for some `k`.


<a id="SlopeMap"></a><a id="SlopeMap--PadRamifPgon--etc"></a><a id="SlopeMap--PadRamifPgon--RngIntElt"></a>
> **SlopeMap** (P :: *PadRamifPgon*, m :: *RngIntElt*)
> 
> -> *Map*, *RngUPolElt*, *Map*
> {:.ret}
{:.intrinsic}

For positive `m`, treating the residue class field as a `F_p` vector space `V`, returns the linear map from `V` to `V` defined by the slope polynomial, which is additive. Also returns the slope polynomial and the map from the residue class field to `V`.


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

