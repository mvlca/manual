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

### For Single Image

#### istyle01 (Global Resource)

    {{< istyle01 src="images/imgname.jpg" size="350x" link="/path/target" alt="something" class="style-one" >}}

*size*, *link*, *alt* and *class* can be omitted but *src*. see below:

    {{< istyle01 src="images/imgname.jpg" >}}

#### istyle02 (Local Resource)

    {{< istyle02 src="images/imgname.jpg" size="350x" link="/path/target" alt="something" class="style-one" >}}

*size*, *link*, *alt* and *class* can be omitted but *src*. see below:

    {{< istyle02 src="images/imgname.jpg" >}}

===

### Multiple Images

#### Global Resource

    {{< gstyle03 tsize="250x" vsize="450x" >}}
    images/imgname01.jpg
    images/imgname02.jpg
    images/imgname03.jpg
    images/imgname04.jpg
    {{< /gstyle03 >}}

*tsize* and *vsize* can be omitted.

#### Global Resource

    {{< gstyle04 tsize="250x" vsize="450x" >}}
    imgname01.jpg
    imgname02.jpg
    imgname03.jpg
    imgname04.jpg
    {{< /gstyle04 >}}

*tsize* and *vsize* can be omitted.