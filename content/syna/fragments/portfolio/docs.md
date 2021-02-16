+++
fragment = "content"
weight = 300

title = "Documentation"

[sidebar]
  sticky = true
+++

This fragment needs a fragment controller file and subitems. You need to create a directory for this fragment and put `index.md` with `fragment = "portfolio"` and subitems next to that file.

### Variables

`index.md` only uses [global varibales]({{< ref "global-variables" >}}). Following variables are for subitems.

#### title
*type: string*

Title of the portfolio item. Will appear in the modal (after clicking the item) as well.

#### subtitle
*type: string*

Subtitle of the portfolio item. Will appear in the modal (after clicking the item) as well.

#### item_url
*type: string*

URL of the portfolio item. If set, then clicking the portfolio item would open the URL and modal will not be opened.

**NOTE:** This variable may be deprecated in the future and be renamed to `url`.

#### background
*type: [asset object]({{< ref "global-variables" >}}#asset)*  
*size: 500x380*

The background image that is shown on the portfolio item.

#### asset
*type: [asset object]({{< ref "global-variables" >}}#asset)*  
*size: 500x380*

The image that is shown on the portfolio item.

[Global variables]({{< ref "global-variables" >}}) are documented as well and have been omitted from this page.
