{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Needs Review
|Content=Incomplete, Examples Needed, Examples Best Practices, Needs Summary
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|'srcset' can be included along with the [[src_(input,_img)|src]] attribute and provides information to the browser to help decide the most appropriate image to load.}}
{{Markup_Attribute
|Applies_to=dom/HTMLImageElement
|Property_applies_to=dom/HTMLImageElement
|Content=An attribute of the image element 'srcset' allows you to inform the browser information about the image before it begins to prefetch the image.

The `srcset` sytax works by submitting the preferred size of the image with the corresponding viewport `sizes` informing the browser when to show them, or by just submitting the target device pixel ratio .

## SRCSET with device pixel ration only

Targeting images based on device pixel ratio only can be accomplished by using the `x` descriptor.

    <img srcset="small.jpg 1x, large.jpg 2x"
    src="small.jpg" />

## SRCSET with SIZES

The standard `src` attribute is used to allow for all browsers that do not support `srcset`

    srcset="small.jpg 300w,
            medium.jpg 600w,
            large.jpg 1024w"`

The `srcset` attribute takes a comma separate list of URL's for each of the available image sizes. The image widths are defined using `w` descriptor. If you save out 3 different sizes of your image at 300px, 600px, 1024px you would include
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Example of the SRCSET and SIZES attributes
|Code=<img 
 srcset="http://placehold.it/300x150&text=500+Small.jpg 500w, http://placehold.it/600x250&text=600+Medium.jpg 600w, http://placehold.it/1024x500&text=1024+Large.jpg 1024w" 
 sizes="(min-width:500px) 33.3vw,(min-widthh:1000px) 50vw, 100vw" src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
     
     alt="Picture SRCSET" />
|LiveURL=http://codepen.io/justincavery/full/osDGt/
}}{{Single Example
|Language=HTML
|Description=Example of srcset using only device pixel ration (not with sizes)
|Code=<img srcset="http://placehold.it/600x250&text=1x+Medium.jpg 1x, http://placehold.it/1024x500&text=2x+Large.jpg 2x"
src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
     alt="Picture SRCSET" />
|LiveURL=http://codepen.io/justincavery/pen/tliGE
}}{{Single Example
|Language=HTML
|Description=Picture Element
|Code=<picture>
<source media="(max-width: 479px)" src="test_landscape_1@1x.jpg">
<source media="(min-width: 480px) and (max-width: 639px)" src="test_landscape_1@2x.jpg">
<source media="(min-width: 640px)" src="test_landscape_1@4x.jpg">
<source media="monochrome" src="test_landscape_1@monochrome.jpg">
<source media="print" src="test_landscape_1@monochrome.jpg">
<!-- fallback img if picture is not supported -->
<img src="test_landscape_1@2x.jpg">
<!-- alternate text -->
<p>Nymphenburg Castle in Munich during sunset</p>
</picture>
|LiveURL=http://responsiveimages.org/demos/basic-implementation/index.html
}}
}}
{{Notes_Section}}
{{Related_Specifications_Section
|Specifications=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows=
}}
{{See_Also_Section
|Topic_clusters=Media Queries, Responsive Web Design
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}