{{Page_Title}}
{{Flags
|High-level issues=Needs Topics, Missing Relevant Sections, Needs Review
|Content=Incomplete, Examples Needed, Examples Best Practices, Needs Summary
|Checked_Out=Yes
}}
{{Standardization_Status|W3C Editor's Draft}}
{{API_Name}}
{{Summary_Section|The '''srcset''' attribute is an extension of the [[html/elements/img|image element]]. It provides  additional image related information to the browser to help decide the most appropriate image to load. Most commonly used for delivering the best image for high device pixel ratio and responsive images.}}
{{Markup_Attribute
|Applies_to=dom/HTMLImageElement
|Property_applies_to=dom/HTMLImageElement
|Content=An attribute of the [[html/elements/img|image element]] element, '''srcset''' provides webpages the ability to inform the browser on size and pixel density information about the image before it begins the prefetch process.

'''srcset''' submits the preferred size of the image with the corresponding viewport '''[[html/attributes/sizes|sizes]]''' informing the browser the best image to use for the best viewport. Alternatively you can also omit the '''[[html/attributes/sizes|sizes]]''' attribute and just use the '''srcset''' attribute to target images for specific device pixel ratios .

Targeting images based on device pixel ratio only can be accomplished by using the <code>x</code> descriptor.

The standard '''[[html/attributes/src_(input,_img)|src]]''' attribute is always used to provide a fallback for all browsers that do not support '''srcset'''
    <img srcset="small.jpg 1x, large.jpg 2x"
    src="small.jpg" />

The '''srcset''' attribute can also take a comma separated list of URL's for each of the available image sizes. The image widths are defined using '''w''' descriptor. If you save out 3 different sizes of your image at 300px, 600px, 1024px this is what your code would look like.

    <img srcset="small.jpg 300w,
            medium.jpg 600w,
            large.jpg 1024w"
            src="small.jpg"
            alt="A picture of a small thing" />
}}
{{Examples_Section
|Not_required=No
|Examples={{Single Example
|Language=HTML
|Description=Example of srcset using only device pixel ration (not with sizes)
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
      srcset="http://placehold.it/300x150&text=500+Small.jpg 500w, 
              http://placehold.it/600x250&text=600+Medium.jpg 600w, 
              http://placehold.it/1024x500&text=1024+Large.jpg 1024w" 
      sizes="(min-width:500px) 33.3vw,
             (min-widthh:1000px) 50vw, 
             100vw" 
      src="http://placehold.it/300x150&text=Small.jpg+No+Picture+Support"
      alt="Picture SRCSET" />
|LiveURL=http://codepen.io/justincavery/full/osDGt/
}}
}}
{{Notes_Section
|Usage=When using '''srcset''' with the '''w''' descriptor you must also include the '''[[/html/attributes/sizes|sizes]]''' attribute.
}}
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