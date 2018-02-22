# Template p-adic fields
{:#template-p-adic-fields}



**Contents**
* [Creation](#creation)
* [Extensions](#extensions)
* [Ore's conditions](#ores-conditions)

## Creation
{:#creation}

<a id="TemplatepAdicField--RngIntElt--RngIntElt--RngIntElt"></a><a id="TemplatepAdicField--RngIntElt--etc"></a><a id="TemplatepAdicField"></a>
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

<a id="UnramifiedExtension"></a><a id="UnramifiedExtension--FldPadTmpl--etc"></a><a id="UnramifiedExtension--FldPadTmpl--RngIntElt"></a>
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


## Ore's conditions
{:#ores-conditions}

<a id="OreConditions--FldPadTmpl--RngIntElt--RngIntElt--RngIntElt"></a><a id="OreConditions"></a><a id="OreConditions--FldPadTmpl--etc"></a>
> **OreConditions** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if there exists an extension of degree `n` of `F` whose ramification polygon has a point `(p^s, J)`.


<a id="OreConditions-2"></a><a id="OreConditions--FldPadTmpl--RngIntElt--RngIntElt"></a><a id="OreConditions--FldPadTmpl--etc-2"></a>
> **OreConditions** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

True if there exists an extension of degree `n` and discriminant valuation `n+J-1` of `F`.


<a id="OrePossibilities"></a><a id="OrePossibilities--FldPadTmpl--RngIntElt--RngIntElt"></a><a id="OrePossibilities--FldPadTmpl--etc"></a>
> **OrePossibilities** (F :: *FldPadTmpl*, n :: *RngIntElt*, s :: *RngIntElt*)
> 
> -> *BoolElt*
> {:.ret}
{:.intrinsic}

The possible J such that `(F,n,J,s)` satisfy Ore'`s` conditions.


<a id="OrePossibilities--FldPadTmpl--RngIntElt"></a><a id="OrePossibilities-2"></a><a id="OrePossibilities--FldPadTmpl--etc-2"></a>
> **OrePossibilities** (F :: *FldPadTmpl*, n :: *RngIntElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}

The possible J such that `(F,n,J)` satisfy Ore's conditions.


