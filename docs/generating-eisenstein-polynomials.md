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
> -> *EisenTmpl*
> {:.ret}
{:.intrinsic}

Template for Eisenstein polynomials of degree `n`, discriminant valuation `n+J-1` over `F`.


<a id="TemplateForEisensteinPolynomials"></a><a id="TemplateForEisensteinPolynomials--PadRamifPts"></a>
> **TemplateForEisensteinPolynomials** (P :: *PadRamifPts*)
> 
> -> *EisenTmpl*
> {:.ret}
{:.intrinsic}

A template for Eisenstein polynomials with this ramification polygon.


## Creation of polynomials
{:#creation-of-polynomials}

<a id="#--EisenTmpl"></a><a id="#"></a><a id="#--EisenTmplCoeff"></a>
> **\'#\'** (C :: *EisenTmplCoeff*)
> 
> **\'#\'** (T :: *EisenTmpl*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

Size of the template.




<a id="Random"></a><a id="Random--EisenTmplCoeff--FldPad"></a><a id="Random--EisenTmplCoeff--etc"></a>
> **Random** (T :: *EisenTmplCoeff*, K :: *FldPad*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

A random element of `K` satisfying the template.


<a id="Random-2"></a><a id="Random--EisenTmpl--FldPad"></a><a id="Random--EisenTmpl--etc"></a>
> **Random** (T :: *EisenTmpl*, K :: *FldPad*)
> 
> -> *RngIntElt*
> {:.ret}
{:.intrinsic}

A random polynomial from `T` over the field `K`.


