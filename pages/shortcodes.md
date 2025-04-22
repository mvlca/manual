# Shortcodes List

## 1. Carousel01

Image carousel for **global resources**.

### Usage

    {{< carousel01 src="/path/to/image.jpg" title="link_title" link="target_link" >}}

## 2. carousel02

Image carousel for **local resources**.

### Usage

    {{ carousel02 >}}

## cushtml

To insert HTML in markdown file.

### Usage

    {{< cushtml >}}
    <div>your html here.</div>
    {{< /cushtml >}}

## faqans
## faqgroup
## faqpair
## faqques

## gstyle01

Gallery for **global resources** and **matching all**.

### Usage

    {{< gstyle01 src="path/to/*" tsize="250x" vsize="450x" >}}

## gstyle02

Gallery for **local resources** and **matching all**.

### Usage

    {{< gstyle02 >}}

## gstyle03

Gallery for **global resources** and **selected images**.

### Usage

    {{< gstyle03 tsize="250x" vsize="450x" >}}
    images/imgname01.jpg
    images/imgname02.jpg
    images/imgname03.jpg
    images/imgname04.jpg
    {{< /gstyle03 >}}

## gstyle04

Gallery for **local resources** and **selected images**.

### Usage

    {{< gstyle04 tsize="250x" vsize="450x" >}}
    imgname01.jpg
    imgname02.jpg
    imgname03.jpg
    imgname04.jpg
    {{< /gstyle04 >}}
