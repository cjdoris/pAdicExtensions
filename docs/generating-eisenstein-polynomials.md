# Generating Eisenstein polynomials
{:#generating-eisenstein-polynomials}



**Contents**
* [Creation of templates](#creation-of-templates)
* [Creation of polynomials](#creation-of-polynomials)

## Creation of templates
{:#creation-of-templates}

<a id="TemplateForEisensteinPolynomialsByDegreeAndDisciminant"></a><a id="TemplateForEisensteinPolynomialsByDegreeAndDisciminant--FldPadTmpl--etc"></a><a id="TemplateForEisensteinPolynomialsByDegreeAndDisciminant--FldPadTmpl--RngIntElt--RngIntElt"></a>
> **TemplateForEisensteinPolynomialsByDegreeAndDisciminant** (F :: *FldPadTmpl*, n :: *RngIntElt*, J :: *RngIntElt*)
> 
> -> *Tmpl_RngUPolElt_FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="TemplateForEisensteinPolynomials"></a><a id="TemplateForEisensteinPolynomials--PadRamifPgon"></a>
> **TemplateForEisensteinPolynomials** (P :: *PadRamifPgon*)
> 
> -> *Tmpl_RngUPolElt_FldPadTmpl*
> {:.ret}
{:.intrinsic}

**Parameters**
- `Residues`: When given, use these residues instead of the ones attached to P.
- `CCResidue`: When given, use this CC-residue instead of the one attached to P.
- `Shrink := true`: When true, returns the smallest template possible; when false, just uses the discriminant to bound the template.

## Creation of polynomials
{:#creation-of-polynomials}

<a id="#"></a><a id="#--Tmpl_FldPadTmplElt"></a>
> **\'#\'** (T :: *Tmpl_FldPadTmplElt*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}


<a id="#-2"></a><a id="#--Tmpl_RngUPolElt_FldPadTmpl"></a>
> **\'#\'** (T :: *Tmpl_RngUPolElt_FldPadTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}


<a id="ToSequence"></a><a id="ToSequence--Tmpl_FldPadTmplElt"></a>
> **ToSequence** (T :: *Tmpl_FldPadTmplElt*)
> 
> -> []
> {:.ret}
{:.intrinsic}


<a id="ToSequence-2"></a><a id="ToSequence--Tmpl_RngUPolElt_FldPadTmpl"></a>
> **ToSequence** (T :: *Tmpl_RngUPolElt_FldPadTmpl*)
> 
> -> []
> {:.ret}
{:.intrinsic}


<a id="Random"></a><a id="Random--Tmpl_FldPadTmplElt"></a>
> **Random** (T :: *Tmpl_FldPadTmplElt*)
> 
> -> *FldPadTmplElt*
> {:.ret}
{:.intrinsic}


<a id="Random-2"></a><a id="Random--Tmpl_RngUPolElt_FldPadTmpl"></a>
> **Random** (T :: *Tmpl_RngUPolElt_FldPadTmpl*)
> 
> -> *RngUPolElt_FldPadTmpl*
> {:.ret}
{:.intrinsic}


<a id="IndexSet"></a><a id="IndexSet--Tmpl_FldPadTmplElt"></a>
> **IndexSet** (T :: *Tmpl_FldPadTmplElt*)
> 
> -> Any
> {:.ret}
{:.intrinsic}


<a id="IndexSet-2"></a><a id="IndexSet--Tmpl_RngUPolElt_FldPadTmpl"></a>
> **IndexSet** (T :: *Tmpl_RngUPolElt_FldPadTmpl*)
> 
> -> Any
> {:.ret}
{:.intrinsic}


<a id="GetIndex"></a><a id="GetIndex--Tmpl_FldPadTmplElt--etc"></a><a id="GetIndex--Tmpl_FldPadTmplElt--any"></a>
> **GetIndex** (T :: *Tmpl_FldPadTmplElt*, idx)
> 
> -> *FldPadTmplElt*
> {:.ret}
{:.intrinsic}


<a id="GetIndex-2"></a><a id="GetIndex--Tmpl_RngUPolElt_FldPadTmpl--etc"></a><a id="GetIndex--Tmpl_RngUPolElt_FldPadTmpl--any"></a>
> **GetIndex** (T :: *Tmpl_RngUPolElt_FldPadTmpl*, idx)
> 
> -> *RngUPolElt_FldPadTmpl*
> {:.ret}
{:.intrinsic}


