# User Manual of mgmamm Hugo

## New Page

A new page can also be created by normal way (Windows way) of going into desired folder, right-click and select *New File*. But the way is not recommended in favour of doing [Hugo](https://gohugo.io) way. It is much more preferable because the bare-bone `front matter` structure wil be included by the followings.

    [user@hostname root]$ hugo new content about/_index.md
    [user@hostname root]$ hugo new content content/en/about/_index.md

OR

    [user@hostname root]$ hugo new content about/index.md
    [user@hostname root]$ hugo new content content/en/about/index.md

The each two commands above are same. Second is preferable if directory structure is long and hitting `Tab` for autocompletion is helpful. The filename `_index.md` and `index.md` indicate *branch bundle* and *leaf bundle*.

**Note**: Normal user will usually need to use the following command examples.

    [user@hostname root]$ hugo new content about/newpage.md
    [user@hostname root]$ hugo new content content/en/about/newpage.md

The two commands above are same. Second is preferable if directory structure is long and hitting `Tab` for autocompletion is helpful. The filename `newpage.md` indicates `single` or *normal page*.

## Front Matter

Front matter is to define metadata of the document such as `date` (timestamp of the document's creation), `draft`, `draft`, `categories`, `tags`, `params`, `menu` and much more. An example of `front matter`:

    +++
    date = '2025-04-12T13:19:41+06:30'
    draft = false
    title = 'Helping Hands to Earthquake Affected Area'
    categories = 'CSR'
    tags = 'Misc'
    [params]
        [params.pagestyle]
            define = 'gallery'
    [menus.main]
        parent = 'CSR'
        name = 'Earthquake 2025'
        weight = 10
    +++

## Images

There are two `shortcodes` to insert image in page. The following two `shortcodes` can insert at a time. Simply repeat the process to insert multiple images.

1. istyle01 (Global Resource)
2. istyle02 (Local Resource)

#### istyle01 (Global Resource)

    {{< istyle01 src="images/imgname.jpg" size="350x" link="/path/target" alt="something" class="image-style-one" >}}

*size*, *link*, *alt* and *class* can be omitted but *src*. see below:

    {{< istyle01 src="images/imgname.jpg" >}}

*class* is set to `image-style-one` if *class* is omitted.

#### istyle02 (Local Resource)

    {{< istyle02 src="imgname.jpg" size="350x" link="/path/target" alt="something" class="image-style-one" >}}

*size*, *link*, *alt* and *class* can be omitted but *src*. see below:

    {{< istyle02 src="imgname.jpg" >}}

*class* is set to `image-style-one` if *class* is omitted.

### Gallery

There are four `shortcodes` to display gallery in a page as follows:

1. gstyle01 (Global Resource) using `resources.Match` and `.ResourceType "image"`
2. gstyle03 (Global Resource) using `resources.Get`
3. gstyle02 (Local Resource) using `.Page.Resources.ByType "image"`
4. gstyle04 (Local Resource) using `.Page.Resources.Get`

#### gstyle01 & gstyle03 (Global Resource)

    {{< gstyle01 src="images/photo-collection/*" tsize="250x" vsize="450x" >}}

In above, *tsize* and *vsize* can be omitted except *src*. Put images in a directory under the `assets` directory and match all photo in the directory (named `photo-collection` in above example) with `src="images/photo-collection/*"`.

To be able to control over which images is inserted, use `gstyle03` as follow:

    {{< gstyle03 tsize="250x" vsize="450x" >}}
    images/imgname01.jpg
    images/imgname02.jpg
    images/imgname03.jpg
    images/imgname04.jpg
    {{< /gstyle03 >}}

*tsize* and *vsize* can be omitted.

#### gstyle02 & gstyle04 (Local Resource)

    {{< gstyle02 >}}

Among the four `shortcodes` for gallery, `gstyle02` is simplest and most preferable. The key point to be able to use `gstyle02` is creation of page. The page must be `page bundle` which constitutes `branch bundle` and `leaf bundle`. The following example shows creation of `leaf bundle`:

1. create new page `content/en/about/executives/index.md`
2. put images in `content/en/about/executives` directory
3. the `{{< gstyle02 >}}` in `index.md` will access *all images* in above directory


To be able to control over which images is inserted, with the same directory structure, use `gstyle04` as follow:

    {{< gstyle04 tsize="250x" vsize="450x" >}}
    imgname01.jpg
    imgname02.jpg
    imgname03.jpg
    imgname04.jpg
    {{< /gstyle04 >}}

*tsize* and *vsize* can be omitted.

#### Defining Gallery Page (#333 background-color)

Page style can also be changed by defining `params` in `front matter` as follow:

    +++
    ...
    [params]
        [params.pagestyle]
            define = 'gallery'
    ...
    +++

**Note**: `section page` can NOT be defined as `gallery` because `gallery.css` contains `.singlepage-container`.
