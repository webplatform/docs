{{Page_Title}}
{{Flags
|State=Ready to Use
|Editorial notes=
|Checked_Out=No
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The '''srcset''' attribute is an extension of the [[html/elements/img|image element]]. It provides  additional image related information to the browser to help decide the most appropriate image to load. Most commonly used for delivering the best image for high device pixel ratio and responsive images.}}
{{Markup_Attribute
|Applies_to=dom/HTMLImageElement
|Property_applies_to=dom/HTMLImageElement
|Content=As attribute of the [[html/elements/img|image element]] element, '''srcset''' provides webpages the ability to inform the browser on size and pixel density information about the image before it begins the prefetch process.

'''srcset''' submits the preferred size of the image with the corresponding viewport '''[[html/attributes/sizes|sizes]]''' informing the browser the best image to use for the best viewport. Alternatively you can also omit the '''[[html/attributes/sizes|sizes]]''' attribute and just use the '''srcset''' attribute to target images for specific device pixel ratios.

Targeting images based on device pixel ratio only can be accomplished by using the <code>x</code> descriptor.

The standard '''[[html/attributes/src_(input,_img)|src]]''' attribute is always used to provide a fallback for all browsers that do not support '''srcset'''
    <img srcset="small.jpg 1x, large.jpg 2x"
    src="small.jpg" />

The '''srcset''' attribute can also take a comma separated list of URL's for each of the available image sizes. The image widths are defined using '''w''' descriptor. If you save out three different sizes of your image at 300px, 600px, 1024px this is what your code would look like.

    <img srcset="large.jpg 1024w,
            medium.jpg 600w,
            small.jpg 300w"
            src="small.jpg"
            alt="A picture of a small thing" />
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Example of srcset using only device pixel ratio
|Code=<img 
      srcset="http://placehold.it/600x250&text=1x+Medium.jpg 1x, 
              http://placehold.it/1024x500&text=2x+Large.jpg 2x"
      src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
      alt="Picture SRCSET" />
|LiveURL=http://codepen.io/justincavery/pen/tliGE
}}{{Single Example
|Language=HTML
|Description=Example of the SRCSET and SIZES attributes
|Code=<img 
      srcset="http://placehold.it/1024x500&text=1024+Large.jpg 1024w, 
              http://placehold.it/600x250&text=600+Medium.jpg 600w, 
          http://placehold.it/300x150&text=500+Small.jpg 500w" 
      sizes="(min-width:500px) 33.3vw,
             (min-width:1000px) 50vw, 
             100vw" 
      src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
      alt="Picture SRCSET" />
|LiveURL=http://codepen.io/justincavery/full/osDGt/
}}
}}
{{Notes_Section
|Usage=When using '''srcset''' with the '''w''' descriptor you must also include the '''[[html/attributes/sizes|sizes]]''' attribute.
|Notes=
|Import_Notes=
}}
{{Related_Specifications_Section
|Specifications={{Related Specification
|Name=HTML5 APIs
|URL=http://www.w3.org/html/wg/drafts/srcset/w3c-srcset/
|Status=Editor’s Draft
|Relevant_changes=
}}
}}
{{See_Also_Section
|Manual_links=
|External_links=
|Manual_sections=
}}
{{Topics|HTML}}
{{External_Attribution
|Is_CC-BY-SA=No
|MDN_link=
|MSDN_link=
|HTML5Rocks_link=
}}
{{Compatibility_Section
|Not_required=No
|Imported_tables=
|Desktop_rows=
|Mobile_rows=
|Notes_rows={{Compatibility Notes Row
|Browser=Chrome
|Version=34
}}{{Compatibility Notes Row
|Browser=Safari
|Version=8
}}{{Compatibility Notes Row
|Browser=Opera
|Version=21
}}
}}