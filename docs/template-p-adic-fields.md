# Template p-adic fields
{:#template-p-adic-fields}


A "template" p-adic field represents a p-adic field K with only partial information known, such as its prime and absolute degree. For example, the number of extensions of K of a given degree d only depends on d, p, and the absolute inertia and ramification degrees, and so it is useful to have a representation of a field with such limited information.

Currently, the partial information we support is:
- The prime, `p`
- The absolute degree, `(K:Q_p)`
- The absolute inertia degree, `f(K:Q_p)`
- The absolute ramification degree, `e(K:Q_p)`
- The "uniformizer residue class", which is `pi^e/p` where `pi` is a uniformizer; this is well-defined up to a multiple by a `e`th power
- The actual field `K`, as a standard `FldPad` such as is returned by `pAdicField`.


**Contents**
* [Creation](#creation)
* [Invariants](#invariants)
* [Ore's conditions](#ores-conditions)
* [Elements](#elements)
* [Polynomial rings](#polynomial-rings)
* [Polynomials](#polynomials)

## Creation
{:#creation}

<a id="TemplatepAdicField"></a><a id="TemplatepAdicField--noargs"></a>
> **TemplatepAdicField** ()
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}

**Parameters**
- `Prime`
- `Degree`
- `InertiaDegree`
- `RamificationDegree`
- `UniformizerResidue`
- `Actual`

<a id="TemplatepAdicField-2"></a><a id="TemplatepAdicField--RngIntElt"></a>
> **TemplatepAdicField** (p :: *RngIntElt*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="TemplatepAdicField-3"></a><a id="TemplatepAdicField--FldPad"></a>
> **TemplatepAdicField** (K :: *FldPad*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}


## Invariants
{:#invariants}

<a id="HasPrime"></a><a id="HasPrime--FldPadTmpl"></a>
> **HasPrime** (F :: *FldPadTmpl*)
> 
> -> *BoolElt*, *RngIntElt*
> {:.ret}
{:.intrinsic}


<a id="Prime"></a><a id="Prime--FldPadTmpl"></a>
> **Prime** (F :: *FldPadTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}


<a id="HasAbsoluteDegree"></a><a id="HasAbsoluteDegree--FldPadTmpl"></a><a id="HasAbsoluteInertiaDegree"></a><a id="HasAbsoluteInertiaDegree--FldPadTmpl"></a><a id="HasAbsoluteRamificationDegree"></a><a id="HasAbsoluteRamificationDegree--FldPadTmpl"></a>
> **HasAbsoluteDegree** (F :: *FldPadTmpl*)
> 
> **HasAbsoluteInertiaDegree** (F :: *FldPadTmpl*)
> 
> **HasAbsoluteRamificationDegree** (F :: *FldPadTmpl*)
> 
> -> *BoolElt*, *RngIntElt*
> {:.ret}
{:.intrinsic}

True if the absolute degree/inertia degree/ramification degree is known.






<a id="AbsoluteDegree"></a><a id="AbsoluteDegree--FldPadTmpl"></a><a id="AbsoluteInertiaDegree"></a><a id="AbsoluteInertiaDegree--FldPadTmpl"></a><a id="AbsoluteRamificationDegree"></a><a id="AbsoluteRamificationDegree--FldPadTmpl"></a>
> **AbsoluteDegree** (F :: *FldPadTmpl*)
> 
> **AbsoluteInertiaDegree** (F :: *FldPadTmpl*)
> 
> **AbsoluteRamificationDegree** (F :: *FldPadTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Absolute degree, inertia degree and ramification degree.






<a id="HasUniformizerResidue"></a><a id="HasUniformizerResidue--FldPadTmpl"></a>
> **HasUniformizerResidue** (F :: *FldPadTmpl*)
> 
> -> *BoolElt*, *FldFinElt*
> {:.ret}
{:.intrinsic}


<a id="UniformizerResidue"></a><a id="UniformizerResidue--FldPadTmpl"></a>
> **UniformizerResidue** (F :: *FldPadTmpl*)
> 
> -> *FldFinElt*
> {:.ret}
{:.intrinsic}


<a id="HasResidueClassField"></a><a id="HasResidueClassField--FldPadTmpl"></a>
> **HasResidueClassField** (F :: *FldPadTmpl*)
> 
> -> *BoolElt*, *FldFin*, *Map*
> {:.ret}
{:.intrinsic}


<a id="ResidueClassField"></a><a id="ResidueClassField--FldPadTmpl"></a>
> **ResidueClassField** (F :: *FldPadTmpl*)
> 
> -> *FldFin*, *Map*
> {:.ret}
{:.intrinsic}


<a id="HasActual"></a><a id="HasActual--FldPadTmpl"></a>
> **HasActual** (F :: *FldPadTmpl*)
> 
> -> *BoolElt*, *FldPad*, *Map*
> {:.ret}
{:.intrinsic}


<a id="Actual"></a><a id="Actual--FldPadTmpl"></a>
> **Actual** (F :: *FldPadTmpl*)
> 
> -> *FldPad*, *Map*
> {:.ret}
{:.intrinsic}


<a id="Embedding"></a><a id="Embedding--FldPadTmpl--etc"></a><a id="Embedding--FldPadTmpl--FldPad"></a>
> **Embedding** (F :: *FldPadTmpl*, A :: *FldPad*)
> 
> -> *Map*
> {:.ret}
{:.intrinsic}


## Ore's conditions
{:#ores-conditions}

<a id="OreConditions"></a><a id="OreConditions--FldPadTmpl--etc"></a><a id="OreConditions--FldPadTmpl--RngIntElt--RngIntElt--RngIntElt"></a>
> **OreConditions** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}


<a id="OreConditions-2"></a><a id="OreConditions--FldPadTmpl--etc-2"></a><a id="OreConditions--FldPadTmpl--RngIntElt--RngIntElt"></a>
> **OreConditions** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}


<a id="OrePossibilities"></a><a id="OrePossibilities--FldPadTmpl--etc"></a><a id="OrePossibilities--FldPadTmpl--RngIntElt--RngIntElt"></a>
> **OrePossibilities** (F :: *FldPadTmpl*, n :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}


<a id="OrePossibilities-2"></a><a id="OrePossibilities--FldPadTmpl--etc-2"></a><a id="OrePossibilities--FldPadTmpl--RngIntElt"></a>
> **OrePossibilities** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}


## Elements
{:#elements}


Elements of a template p-adic field are represented by their valuation and a finite sequence of p-adic coefficients, which are elements of the residue class field.

When the actual field is known, we provide maps between the template and actual field (accessible by the `Actual` intrinsic). For each element of the residue class field, we choose a representative in the actual field (specifically, we use the inverse of the map returned by `ResidueClassField` on the actual field). If `R` is the set of representatives, then the sequence of p-adic coefficients may be interpreted as a polynomial with coefficients in `R`. Evaluating this at the uniformizer of the actual field gives an integral element, which is then shifted by the valuation.

<a id="IsCoercible"></a><a id="IsCoercible--FldPadTmpl--etc"></a><a id="IsCoercible--FldPadTmpl--any"></a>
> **IsCoercible** (F :: *FldPadTmpl*, X)
> 
> -> *BoolElt*, Any
> {:.ret}
{:.intrinsic}

Allows coercion into `F` any of the following:
- An element of `F`
- An element of the actual field of `F` (if defined)
- A sequence [c0,c1,...] of p-adic coefficients
- A tuple <v,[c0,c1,...]> of valuation and p-adic coefficients
- The integer 0


<a id="Parent"></a><a id="Parent--FldPadTmplElt"></a>
> **Parent** (x :: *FldPadTmplElt*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="IsZero"></a><a id="IsZero--FldPadTmplElt"></a>
> **IsZero** (x :: *FldPadTmplElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}


<a id="Valuation"></a><a id="Valuation--FldPadTmplElt"></a>
> **Valuation** (x :: *FldPadTmplElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}


<a id="Actual-2"></a><a id="Actual--FldPadTmplElt"></a>
> **Actual** (x :: *FldPadTmplElt*)
> 
> -> *FldPadElt*
> {:.ret}
{:.intrinsic}


## Polynomial rings
{:#polynomial-rings}

<a id="PolynomialRing"></a><a id="PolynomialRing--FldPadTmpl"></a>
> **PolynomialRing** (F :: *FldPadTmpl*)
> 
> -> *RngUPol_FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="BaseRing"></a><a id="BaseRing--RngUPol_FldPadTmpl"></a>
> **BaseRing** (R :: *RngUPol_FldPadTmpl*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="HasActual-2"></a><a id="HasActual--RngUPol_FldPadTmpl"></a>
> **HasActual** (R :: *RngUPol_FldPadTmpl*)
> 
> -> *BoolElt*, *RngUPol*, *Map*
> {:.ret}
{:.intrinsic}


<a id="Actual-3"></a><a id="Actual--RngUPol_FldPadTmpl"></a>
> **Actual** (R :: *RngUPol_FldPadTmpl*)
> 
> -> *RngUPol*, *Map*
> {:.ret}
{:.intrinsic}


<a id="Embedding-2"></a><a id="Embedding--RngUPol_FldPadTmpl--etc"></a><a id="Embedding--RngUPol_FldPadTmpl--RngUPol-FldPad--Map"></a>
> **Embedding** (R :: *RngUPol_FldPadTmpl*, A :: *RngUPol*[*FldPad*], m :: *Map*)
> 
> -> *Map*
> {:.ret}
{:.intrinsic}


<a id="Embedding-3"></a><a id="Embedding--RngUPol_FldPadTmpl--etc-2"></a><a id="Embedding--RngUPol_FldPadTmpl--RngUPol-FldPad"></a>
> **Embedding** (R :: *RngUPol_FldPadTmpl*, A :: *RngUPol*[*FldPad*])
> 
> -> *Map*
> {:.ret}
{:.intrinsic}


## Polynomials
{:#polynomials}

<a id="IsCoercible-2"></a><a id="IsCoercible--RngUPol_FldPadTmpl--etc"></a><a id="IsCoercible--RngUPol_FldPadTmpl--any"></a>
> **IsCoercible** (R :: *RngUPol_FldPadTmpl*, X)
> 
> -> *BoolElt*, Any
> {:.ret}
{:.intrinsic}

We can coerce the following into `R`:
- Elements of `R`
- Elements of the actual ring of `R` (if defined)
- Polynomials over anything coercible to the base ring of `R`
- Sequences of anything coercible to the base ring of `R`


<a id="Parent-2"></a><a id="Parent--RngUPolElt_FldPadTmpl"></a>
> **Parent** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *RngUPol_FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="BaseRing-2"></a><a id="BaseRing--RngUPolElt_FldPadTmpl"></a>
> **BaseRing** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="Coefficients"></a><a id="Coefficients--RngUPolElt_FldPadTmpl"></a>
> **Coefficients** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> []
> {:.ret}
{:.intrinsic}


<a id="Degree"></a><a id="Degree--RngUPolElt_FldPadTmpl"></a>
> **Degree** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}


<a id="IsZero-2"></a><a id="IsZero--RngUPolElt_FldPadTmpl"></a>
> **IsZero** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}


<a id="Actual-4"></a><a id="Actual--RngUPolElt_FldPadTmpl"></a>
> **Actual** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *RngUPolElt*
> {:.ret}
{:.intrinsic}


<a id="Extension"></a><a id="Extension--FldPad--etc"></a><a id="Extension--FldPad--RngUPolElt_FldPadTmpl--Map"></a>
> **Extension** (K :: *FldPad*, f :: *RngUPolElt_FldPadTmpl*, m :: *Map*)
> 
> -> *FldPad*
> {:.ret}
{:.intrinsic}


<a id="Extension-2"></a><a id="Extension--FldPad--etc-2"></a><a id="Extension--FldPad--RngUPolElt_FldPadTmpl"></a>
> **Extension** (K :: *FldPad*, f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *FldPad*
> {:.ret}
{:.intrinsic}


<a id="ActualExtension"></a><a id="ActualExtension--RngUPolElt_FldPadTmpl"></a>
> **ActualExtension** (f :: *RngUPolElt_FldPadTmpl*)
> 
> -> *FldPad*
> {:.ret}
{:.intrinsic}


