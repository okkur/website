+++
fragment = "content"
title = "Global Variables"
weight = 100

[sidebar]
  sticky = true
+++

There are a few frontmatter variables that can be used for all fragments. The
variables are as follows:

#### fragment
*type: string*  
**Required for every fragment**

Specifies what fragment the current file controls. Checkout [Fragment Implementation]({{< ref "fragments-implementation" >}}) for more info.

#### weight
*type: number*  
**Required for every fragment**

This variable is used for ordering fragments in a page. It can be empty but it would cause the fragment to be sorted in an unexpected manner.

#### background
Set the background of the fragment.

Background also affects the text color of the fragment's content.
For the background colors of `white`, `light`, `secondary` and `primary` we use Bootstrap's `text_dark` class on content and for other backgrounds, we use `text_light`.

List of all supported colors can be found in [supported colors]({{< ref "styling" >}}#supported-colors) section of the docs.

#### title
*type: string*

Set title of the fragment

#### subtitle
*type: string*

Set subtitle of the fragment

#### title_align
*type: string*  
*accepted values: right, left, center*

Change alignment of fragment's header

#### padding
*type: string*  
*Experimental* 

Changes the padding of fragment's container

#### asset
*type: asset object*

This variable is not a global variable but a variable type that is used in a lot of fragments.

Any fragment that uses this variable type would show either an image or an icon.

The type is introduced to make configuring images and icons same between different fragments.

Some fragments automatically resize images to better fit the layout. For the best result use the documented size of each fragment's asset object.
*To disable image resizing use assets stored within `static/` as these are excluded from auto resizing.*
Please make sure to provide the correct size as documented for each fragment's asset object.

##### asset.image
*type: string*

Link to an image file. `asset.image` supports the build in [image fallthrough mechanism]({{< ref "image-fallthrough" >}}).
If `asset.image` is set, `asset.icon` will be ignored.

##### asset.icon
*type: string*

Icon class powered by FontAwesome such as `fab fab-github`.

##### asset.url
*type: string*

Action/clickable URL of the image or the icon.

##### asset.text
*type: string*

If `asset.image` is set, `text` will be used as alternative text (alt-text) of the image.

#### disable
*type: boolean*

If set to `true`, Syna will not register the fragment. This is useful for drafting fragments.

**NOTE:** `disable` doesn't register the fragment at all. This means you can not remove a global fragment in a specific page by a duplicate disabled fragment. In order to hide a global fragment in a page, use [`hide`](#hide).

#### hide
*type: boolean*

If set to `true`, Syna will not call the fragment and will hide it. Useful for hiding a global fragment in the page. For more information, please checkout [global fragments]({{< ref "syna/docs/fragments">}}/#global-fragments).
