# Template p-adic fields
{:#template-p-adic-fields}



**Contents**
* [Creation](#creation)
* [Extensions](#extensions)
* [Invariants](#invariants)
* [Actual field](#actual-field)
* [Ore's conditions](#ores-conditions)

## Creation
{:#creation}

<a id="TemplatepAdicField"></a><a id="TemplatepAdicField--RngIntElt--RngIntElt--RngIntElt"></a><a id="TemplatepAdicField--RngIntElt--etc"></a>
> **TemplatepAdicField** (p :: *RngIntElt*, f :: *RngIntElt*, e :: *RngIntElt*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}

A "template" `p`-adic field with residue degree `f` and ramification degree `e`.


<a id="TemplatepAdicField-2"></a><a id="TemplatepAdicField--RngIntElt"></a>
> **TemplatepAdicField** (p :: *RngIntElt*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}

A "template" `p`-adic field.


<a id="TemplatepAdicField-3"></a><a id="TemplatepAdicField--FldPad"></a>
> **TemplatepAdicField** (K :: *FldPad*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}

A "template" version of `K`.


## Extensions
{:#extensions}

<a id="UnramifiedExtension"></a><a id="UnramifiedExtension--FldPadTmpl--RngIntElt"></a><a id="UnramifiedExtension--FldPadTmpl--etc"></a>
> **UnramifiedExtension** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}

An unramified extension of `F` of degree `n`.


<a id="TotallyRamifiedExtension--FldPadTmpl--RngIntElt"></a><a id="TotallyRamifiedExtension"></a><a id="TotallyRamifiedExtension--FldPadTmpl--etc"></a>
> **TotallyRamifiedExtension** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> *FldPadTmpl*
> {:.ret}
{:.intrinsic}

A totally ramified extension of `F` of degree `n`.


## Invariants
{:#invariants}

<a id="Prime--FldPadTmpl"></a><a id="Prime"></a>
> **Prime** (F :: *FldPadTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

The prime `p`.


<a id="AbsoluteDegree"></a><a id="AbsoluteRamificationDegree"></a><a id="AbsoluteInertiaDegree--FldPadTmpl"></a><a id="AbsoluteInertiaDegree"></a><a id="AbsoluteRamificationDegree--FldPadTmpl"></a><a id="AbsoluteDegree--FldPadTmpl"></a>
> **AbsoluteDegree** (F :: *FldPadTmpl*)
> 
> **AbsoluteInertiaDegree** (F :: *FldPadTmpl*)
> 
> **AbsoluteRamificationDegree** (F :: *FldPadTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Absolute degree, inertia degree and ramification degree






<a id="ResidueClassField"></a><a id="ResidueClassField--FldPadTmpl"></a>
> **ResidueClassField** (F :: *FldPadTmpl*)
> 
> -> *FldFin*, *Map*
> {:.ret}
{:.intrinsic}

Residue class field. If `F` was created from an actual field, also returns the residue map.


## Actual field
{:#actual-field}


If a template field was created from an actual field ([such as this](#TemplatepAdicField--FldPad)) then that field is remembered.

<a id="HasActualField"></a><a id="HasActualField--FldPadTmpl"></a>
> **HasActualField** (F :: *FldPadTmpl*)
> 
> -> *BoolElt*, *FldPad*
> {:.ret}
{:.intrinsic}

True if `F` is associated to an actual field. If so, also returns the field.


<a id="ActualField--FldPadTmpl"></a><a id="ActualField"></a>
> **ActualField** (F :: *FldPadTmpl*)
> 
> -> *FldPad*
> {:.ret}
{:.intrinsic}

The actual field associated to `F`, if there is one.


## Ore's conditions
{:#ores-conditions}

<a id="OreConditions"></a><a id="OreConditions--FldPadTmpl--etc"></a><a id="OreConditions--FldPadTmpl--RngIntElt--RngIntElt--RngIntElt"></a>
> **OreConditions** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if there exists an extension of degree `n` of `F` whose ramification polygon has a point `(p^s, J)`.


<a id="OreConditions-2"></a><a id="OreConditions--FldPadTmpl--etc-2"></a><a id="OreConditions--FldPadTmpl--RngIntElt--RngIntElt"></a>
> **OreConditions** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if there exists an extension of degree `n` and discriminant valuation `n+J-1` of `F`.


<a id="OrePossibilities--FldPadTmpl--RngIntElt--RngIntElt"></a><a id="OrePossibilities--FldPadTmpl--etc"></a><a id="OrePossibilities"></a>
> **OrePossibilities** (F :: *FldPadTmpl*, n :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

The possible J such that `(F,n,J,s)` satisfy Ore'`s` conditions.


<a id="OrePossibilities--FldPadTmpl--etc-2"></a><a id="OrePossibilities-2"></a><a id="OrePossibilities--FldPadTmpl--RngIntElt"></a>
> **OrePossibilities** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The possible J such that `(F,n,J)` satisfy Ore's conditions.


